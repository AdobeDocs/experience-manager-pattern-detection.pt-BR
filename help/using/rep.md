---
title: REP
description: Página de ajuda do código do Detector de padrões.
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 74%

---

# [!DNL REP] {#rep}

Agente de replicação

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Agente de replicação"
>abstract="O código REP identifica agentes de replicação ativados. Eles são relatados por causa do potencial para problemas que devem ser abordados ao atualizar para o AEM as a Cloud Service. O AEM as a Cloud Service usa o Sling Content Distribution para distribuir conteúdo do autor para os ambientes de publicação. Isso é feito fora do tempo de execução do AEM usando o serviço de pipeline do Adobe I/O Runtime no Adobe Developer. Isso é configurado automaticamente no ambiente as a Cloud Service AEM provisionado."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents" text="Alterações importantes no AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents" text="Diretrizes de desenvolvimento"

O código REP identifica agentes de replicação ativados. Eles são relatados por causa do potencial para problemas que devem ser abordados ao atualizar para o AEM as a Cloud Service.

Os subtipos são usados para identificar diferentes tipos de informações:

* `forward.replication`: Identifique os agentes de replicação direta ativados.
* `reverse.replication`: Identifique os agentes de replicação inversa ativados.
* `standard.replication.agent.modification`: Identifique os agentes de replicação padrão ativados que são modificados.
* `custom.replication.agent.detection`: Identifique os agentes de replicação personalizados ativados.

O AEM as a Cloud Service usa o [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) para distribuir conteúdo do autor para os ambientes de publicação. Isso é feito fora do tempo de execução do AEM usando o serviço de pipeline do Adobe I/O Runtime no Adobe Developer. Isso é configurado automaticamente no ambiente as a Cloud Service AEM provisionado.

## Possíveis implicações e riscos {#implications-and-risks}

* A configuração da replicação foi alterada com o AEM as a Cloud Service. Todos os agentes de replicação atuais devem ser revisados para ver quais são substituídos pelo recurso padrão, quais configurações devem ser movidas para o código e quais não são compatíveis.
* Qualquer uso de agentes de replicação no código personalizado ou em workflows deve ser revisado durante a atualização para o AEM as a Cloud Service.
* Inicialmente, a replicação inversa não é suportada no AEM as a Cloud Service.
* Não há necessidade de configurar um agente de limpeza do Dispatcher separado. Isso é configurado automaticamente no ambiente do AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar, alterar e otimizar a funcionalidade personalizada diretamente dependente dos agentes de replicação e torná-la compatível com o AEM as a Cloud Service. Entre em contato com o Suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication" text="Replicação - AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Consulte as [Diretrizes de desenvolvimento](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents) e notas de versão para [agentes de replicação](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents) do AEM as a Cloud Service.
* Revise, altere e otimize a funcionalidade diretamente dependente dos agentes de replicação para executar tarefas comerciais.
* Veja como a [replicação](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication) é afetada pela implantação no AEM as a Cloud Service.
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) esclarecimentos ou de ter preocupações em conta.
