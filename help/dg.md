---
title: DG
description: Página de ajuda de códigos do detector de padrões
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: ht
source-wordcount: '569'
ht-degree: 100%

---

# DG {#dg}

Diretriz do desenvolvedor

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="Diretrizes do desenvolvedor"
>abstract="O código DG identifica desvios das orientações de desenvolvimento selecionadas para o AEM 6.5 e AEM as a Cloud Service. Seguir as práticas recomendadas pode melhorar a capacidade de manutenção e o desempenho do seu sistema. Embora alguns desses desvios possam não ser um problema em outros contextos de aplicativo, incluindo em versões anteriores do AEM, eles podem causar problemas quando usados com o AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html?lang=pt-BR" text="Desenvolvimento do AEM - diretrizes e práticas recomendadas"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=pt-BR" text="Diretrizes de desenvolvimento do AEM as a Cloud Service"


O código `DG` identifica desvios das diretrizes de desenvolvimento selecionadas para o [AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html?lang=pt-BR) e [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=pt-BR). Seguir as práticas recomendadas pode melhorar a capacidade de manutenção e o desempenho do seu sistema. Embora alguns desses desvios possam não ser um problema em outros contextos de aplicativo, incluindo em versões anteriores do AEM, eles podem causar problemas quando usados com o AEM as a Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de violações detectadas:

* `java.io.inputstream`: O uso de `java.io.InputStream` no código do aplicativo.
* `maintenance.task.configuration`: a configuração de uma determinada atividade de manutenção periódica.
* `sling.commons.scheduler`: o uso da API do Sling Commons Scheduler para uma tarefa agendada.

## Possíveis implicações e riscos {#implications-and-risks}

* `java.io.inputstream`
   * A transmissão de dados binários com o `java.io.InputStream` pode consumir recursos de memória a ponto de afetar o desempenho. Isso é um problema, especialmente devido à memória limitada disponível em contêineres usados no AEM as a Cloud Service.

* `maintenance.task.configuration`
   * Algumas tarefas de manutenção que anteriormente exigiam configuração explícita agora são automaticamente configuradas e gerenciadas dentro do AEM as a Cloud Service.
   * A configuração da tarefa de manutenção no AEM as a Cloud Service deve ser movida para o controle de origem.

* `sling.commons.scheduler`
   * Aplicativos dependentes de tarefas em segundo plano usando o [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) podem não funcionar como esperado porque a execução não pode ser garantida no AEM as a Cloud Service.
   * As orientações de desenvolvimento do AEM as a Cloud Service para [tarefas em segundo plano e tarefas de longa duração](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=pt-BR#background-tasks-and-long-running-jobs) sugerem que o código executado como uma tarefa agendada deve supor que a instância em que está sendo executada pode ser desativada a qualquer momento. Portanto, o código deve ser resiliente e retomável.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="Diretrizes de implementação"
>abstract="Seguindo as diretrizes e práticas recomendadas de desenvolvimento do AEM, os clientes devem revisar suas implementações sobre o uso do Sling Commons Scheduler e reestruturá-las para Sling Jobs, reestruturar suas tarefas de manutenção do sistema, revisar a transmissão de quaisquer dados binários e refatorar seu código para ser compatível com o AEM as a Cloud Service."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Sling Jobs"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html?lang=pt-BR" text="Tarefas de manutenção no AEM as a Cloud Service"

* `java.io.inputstream`
   * Use uma abordagem de upload binário direto na qual o binário seja adicionado diretamente ao armazenamento de dados.
   * Para casos de uso de ativos, use o [aem-upload](https://github.com/adobe/aem-upload). Para outros tipos de binários, a lógica de upload personalizada pode ser modelada seguindo esse mesmo padrão.

* `maintenance.task.configuration`
   * Revise a documentação de [Tarefa de manutenção](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html?lang=pt-BR) do AEM as a Cloud Service.
   * Certifique-se de que a [Configuração da tarefa de manutenção](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=pt-BR#maintenance-tasks-configuration-in-source-control) esteja no controle de origem.

* `sling.commons.scheduler`
   * Substitua o uso do [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) pelo [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), que dispõe de uma garantia de ao menos uma execução.
   * Se possível, a execução de trabalhos de longa duração deve ser evitada.

* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
