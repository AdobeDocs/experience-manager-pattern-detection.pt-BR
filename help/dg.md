---
title: DG
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---


# DG {#dg}

Orientação do desenvolvedor

## Segundo plano {#background}

`DG` identifica desvios das diretrizes de desenvolvimento selecionadas para  [AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html) e  [AEM como Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html). Seguir as práticas recomendadas pode melhorar a capacidade de manutenção e o desempenho do seu sistema. Embora alguns desses desvios possam não ser um problema em outros contextos de aplicativo, incluindo em versões anteriores do AEM, eles podem causar problemas quando usados com o AEM como Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de violações detectadas:

* `java.io.inputstream`: O uso de  `java.io.InputStream` no código do aplicativo.
* `maintenance.task.configuration`: A configuração de uma determinada atividade de manutenção periódica.
* `sling.commons.scheduler`: O uso da API do Sling Commons Scheduler para uma tarefa agendada.

## Possíveis implicações e riscos {#implications-and-risks}

* `java.io.inputstream`
   * A transmissão de dados binários com `java.io.InputStream` pode consumir recursos de memória a ponto de afetar o desempenho. Isso é particularmente um problema devido à memória limitada disponível em contêineres usados no AEM como Cloud Service.

* `maintenance.task.configuration`
   * Algumas tarefas de manutenção que anteriormente exigiam configuração explícita são configuradas e gerenciadas automaticamente no AEM como um Cloud Service.
   * A configuração da tarefa de manutenção no AEM como Cloud Service deve ser movida para o controle de origem.

* `sling.commons.scheduler`
   * Os aplicativos dependentes de tarefas em segundo plano usando [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) podem não funcionar como esperado porque a execução não pode ser garantida em AEM como um Cloud Service.
   * AEM como diretrizes de desenvolvimento de Cloud Service para [tarefas em segundo plano e tarefas de longa execução](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#background-tasks-and-long-running-jobs) sugerem que o código executado como uma tarefa agendada deve supor que a instância em que está sendo executado pode ser desativada a qualquer momento. Portanto, o código deve ser resiliente e retomável.

## Possíveis soluções {#solutions}

* `java.io.inputstream`
   * Use uma abordagem de upload binário direto na qual o binário seja adicionado diretamente ao armazenamento de dados.
   * Para casos de uso de ativos, use [aem-upload](https://github.com/adobe/aem-upload). Para outros tipos de binários, a lógica de upload personalizada pode ser modelada após esse mesmo padrão.

* `maintenance.task.configuration`
   * Revise o AEM como uma documentação de [Tarefa de Manutenção](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html).
   * Certifique-se de que [Configuração da Tarefa de Manutenção](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#maintenance-tasks-configuration-in-source-control) esteja no controlo de origem.

* `sling.commons.scheduler`
   * Substitua o uso de [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) por [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), que têm uma garantia de execução de pelo menos uma vez.
   * Se possível, devem ser evitados postos de trabalho de longa duração.

* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
