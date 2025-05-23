---
title: DG
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 80%

---

# DG {#dg}

Diretriz do desenvolvedor

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="Diretrizes do desenvolvedor"
>abstract="O código DG identifica desvios das orientações de desenvolvimento selecionadas para o AEM 6.5 e AEM as a Cloud Service. Seguir as práticas recomendadas pode melhorar a capacidade de manutenção e o desempenho do seu sistema. Embora alguns desses desvios possam não ser um problema em outros contextos de aplicativo, incluindo em versões anteriores do AEM, eles podem causar problemas quando usados com o AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="Desenvolvimento do AEM – Diretrizes e práticas recomendadas"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Diretrizes de desenvolvimento do AEM as a Cloud Service"


`DG` identifica desvios das diretrizes de desenvolvimento selecionadas para o [AEM 6.5](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices) e o [AEM as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines). Seguir as práticas recomendadas pode melhorar a capacidade de manutenção e o desempenho do seu sistema. Embora alguns desses desvios possam não ser um problema em outros contextos de aplicativo, incluindo em versões anteriores do AEM, eles podem causar problemas quando usados com o AEM as a Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de violações detectadas:

* `java.io.inputstream`: O uso de `java.io.InputStream` no código do aplicativo.
* `maintenance.task.configuration`: a configuração de uma determinada atividade de manutenção periódica.
* `sling.commons.scheduler`: o uso da API do Sling Commons Scheduler para uma tarefa agendada.
* `unsupported.asset.api`: o uso de APIs incompatíveis do Asset Manager no código do aplicativo.
* `javax.jcr.observation.EventListener`: O uso de um ouvinte de eventos no código do aplicativo.
* `custom.guava.cache`: o uso de cache do Guava no código do aplicativo.
* `java.api`: Algumas APIs Java foram removidas do Java 11 para o Java 17.
* `configuration.admin`: o código personalizado que está acessando configurações será sinalizado.
* `guava.api`: Guava não é suportado prontamente no AEM 6.5 LTS.
* `com.day.cq.dam.scene7.api.model`: Há uma alteração principal na versão para `package com.day.cq.dam.scene7.api.model`.

## Possíveis implicações e riscos {#implications-and-risks}

* `java.io.inputstream`
   * A transmissão de dados binários com o `java.io.InputStream` pode consumir recursos de memória a ponto de afetar o desempenho. Esse problema deve-se à memória limitada disponível em containers usados no AEM as a Cloud Service.

* `maintenance.task.configuration`
   * Algumas tarefas de manutenção que anteriormente exigiam configuração explícita agora são automaticamente configuradas e gerenciadas dentro do AEM as a Cloud Service.
   * A configuração da tarefa de manutenção no AEM as a Cloud Service deve ser movida para o controle de origem.

* `sling.commons.scheduler`
   * Aplicativos dependentes de tarefas em segundo plano usando o [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) podem não funcionar como esperado porque a execução não pode ser garantida no AEM as a Cloud Service.
   * As diretrizes de desenvolvimento para [tarefas em segundo plano e tarefas de longa duração](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#background-tasks-and-long-running-jobs) sugerem que o código executado como uma tarefa agendada também deve pressupor que a instância na qual está sendo executado pode ser desativada a qualquer momento. Portanto, o código deve ser resiliente e retomável.

* `unsupported.asset.api`
   * As seguintes APIs do AssetManager são incompatíveis com o AEM as a Cloud Service.
      * createAssetForBinary
      * getAssetForBinary
      * removeAssetForBinary
      * createAsset

* `javax.jcr.observation.EventListener`
   * Aplicativos dependentes do ouvinte de eventos podem não funcionar conforme esperado, porque a execução não pode ser garantida.

* `custom.guava.cache`
   * O uso de cache do Guava pode causar problemas de desempenho no AEM.

* `java.api`
   * Com o AEM 6.5 LTS no JRE17, essas APIs do Java removidas não estarão disponíveis e seu uso falhará.

* `configuration.admin`
   * Você deve verificar seu uso para garantir que não esteja usando configurações não compatíveis, como o Social.

* `guava.api`
   * Como o Guava não é compatível com o AEM 6.5 LTS, o código personalizado que está usando o guava não estará ativo.

* `com.day.cq.dam.scene7.api.model`
   * O pacote importado `com.day.cq.dam.scene7.api.model` em pacotes personalizados não será resolvido devido a uma alteração importante na versão.


## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="Diretrizes de implementação"
>abstract="Revise suas implementações sobre o uso do Sling Commons Scheduler. Reestruture-os para tarefas do Sling, reestruture suas tarefas de manutenção do sistema, revise a transmissão de qualquer dado binário e refatore seu código para ficar em conformidade com o AEM as a Cloud Service."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Sling Jobs"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/operations/maintenance" text="Tarefas de manutenção no AEM as a Cloud Service"

* `java.io.inputstream`
   * Use uma abordagem de upload binário direto na qual o binário seja adicionado diretamente ao armazenamento de dados.
   * Para casos de uso de ativos, consulte [Upload no AEM](https://github.com/adobe/aem-upload). Para outros tipos de binários, a lógica de upload personalizada pode ser modelada seguindo esse mesmo padrão.

* `maintenance.task.configuration`
   * Revise a documentação de [Tarefa de manutenção](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/operations/maintenance) do AEM as a Cloud Service.
   * Certifique-se de que a [Configuração da tarefa de manutenção](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/deploying/overview#maintenance-tasks-configuration-in-source-control) esteja no controle de origem.

* `sling.commons.scheduler`
   * Substitua o uso do [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) pelo [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), que dispõe de uma garantia de ao menos uma execução.
   * Tarefas de longa duração devem ser evitadas.

* `unsupported.asset.api`
   * Em vez de usar as APIs incompatíveis do Asset Manager, consulte [Upload no AEM](https://github.com/adobe/aem-upload).

* `javax.jcr.observation.EventListener`
   * Em vez de usar o ouvinte de eventos, é recomendável refatorar o mecanismo de manipulação de eventos para [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), pois isso proporciona a garantia de processamento.

* `custom.guava.cache`
   * Os caches, se necessários, devem ser criados fora do AEM. Uma solução externa de armazenamento em cache pode ser considerada.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.

* `configuration.admin`
   * Remova qualquer uso de configuração de recursos não compatíveis, como o Social.

* `guava.api`
   * Instale o Guava ou remova o uso se o Guava for usado em seu código personalizado.

* `com.day.cq.dam.scene7.api.model`
   * Atualize o intervalo de versões do pacote importado `com.day.cq.dam.scene7.api.model` para **3.0.4**.