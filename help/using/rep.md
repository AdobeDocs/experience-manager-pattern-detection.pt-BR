---
title: REP
description: Página de ajuda referente ao código do detector de padrões.
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 57%

---

# [!DNL REP] {#rep}

Agente de replicação

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Agente de replicação"
>abstract="O código REP identifica agentes de replicação ativados. Esses agentes são relatados por causa do potencial para problemas que devem ser abordados ao atualizar para o AEM as a Cloud Service. O AEM as a Cloud Service usa o Sling Content Distribution para distribuir conteúdo do autor para os ambientes de publicação. Essa distribuição é feita fora do tempo de execução do AEM usando o serviço de pipeline do Adobe I/O Runtime no Adobe Developer. Esse workflow é configurado automaticamente no ambiente as a Cloud Service AEM provisionado."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents" text="Alterações importantes: AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents" text="Diretrizes de desenvolvimento"

`REP` identifica agentes de replicação habilitados. Esses agentes são relatados por causa do potencial para problemas que devem ser abordados ao atualizar para o AEM as a Cloud Service.

Os subtipos são usados para identificar diferentes tipos de informações:

* `forward.replication`: Identifique os agentes de replicação direta ativados.
* `reverse.replication`: Identifique os agentes de replicação inversa ativados.
* `standard.replication.agent.modification`: Identifique os agentes de replicação padrão ativados que são modificados.
* `custom.replication.agent.detection`: Identifique os agentes de replicação personalizados ativados.

O AEM as a Cloud Service usa o [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) para distribuir conteúdo do autor para os ambientes de publicação. Essa distribuição é feita fora do tempo de execução do AEM usando o serviço de pipeline do Adobe I/O Runtime no Adobe Developer. Esse workflow é configurado automaticamente no ambiente as a Cloud Service AEM provisionado.

## Possíveis implicações e riscos {#implications-and-risks}

* A configuração da replicação foi alterada com o AEM as a Cloud Service. Todos os agentes de replicação atuais devem ser revisados. A revisão ajuda a visualizar:
   * quais recursos padrão podem ser substituídos,
   * quais configurações devem ser movidas para o código,
   * e que não são compatíveis.
* Qualquer uso de agentes de replicação no código personalizado ou em workflows deve ser revisado durante a atualização para o AEM as a Cloud Service.
* Inicialmente, a replicação inversa não é suportada no AEM as a Cloud Service.
* Não é necessário configurar um agente de limpeza do Dispatcher separado. Em vez disso, ele é configurado automaticamente no ambiente as a Cloud Service do AEM.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar, alterar e otimizar a funcionalidade personalizada diretamente dependente dos agentes de replicação e torná-la compatível com o AEM as a Cloud Service. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication" text="Replicação - AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Consulte as [Diretrizes de desenvolvimento](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents) e notas de versão para [agentes de replicação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents) do AEM as a Cloud Service.
* Revise, altere e otimize a funcionalidade diretamente dependente dos agentes de replicação para executar tarefas comerciais.
* Veja como [replicação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication) O é afetado por meio da implantação no AEM as a Cloud Service.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
