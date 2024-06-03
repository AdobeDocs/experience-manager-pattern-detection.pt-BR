---
title: REP
description: Página de ajuda referente ao código do detector de padrões.
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 100%

---

# [!DNL REP] {#rep}

Agente de replicação

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Agente de replicação"
>abstract="O código REP identifica agentes de replicação ativados. Esses agentes são relatados devido ao seu potencial para gerar problemas, o qual deve ser considerado ao atualizar para o AEM as a Cloud Service. O AEM as a Cloud Service usa o Sling Content Distribution para distribuir conteúdo do ambiente de criação para o de publicação. Essa distribuição é feita fora do tempo de execução do AEM, por meio do serviço de pipeline do Adobe I/O Runtime no Adobe Developer. Esse fluxo de trabalho é configurado automaticamente no ambiente provisionado do AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents" text="Alterações importantes: AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents" text="Diretrizes de desenvolvimento"

`REP` identifica agentes de replicação habilitados. Esses agentes são relatados devido ao seu potencial para gerar problemas, o qual deve ser considerado ao atualizar para o AEM as a Cloud Service.

Os subtipos são usados para identificar diferentes tipos de informações:

* `forward.replication`: Identifique os agentes de replicação direta ativados.
* `reverse.replication`: Identifique os agentes de replicação inversa ativados.
* `standard.replication.agent.modification`: identifique os agentes de replicação padrão habilitados que foram modificados.
* `custom.replication.agent.detection`: Identifique os agentes de replicação personalizados ativados.

O AEM as a Cloud Service usa o [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) para distribuir conteúdo do autor para os ambientes de publicação. Essa distribuição é feita fora do tempo de execução do AEM, por meio do serviço de pipeline do Adobe I/O Runtime no Adobe Developer. Esse fluxo de trabalho é configurado automaticamente no ambiente provisionado do AEM as a Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

* A configuração da replicação foi alterada com o AEM as a Cloud Service. Verifique todos os agentes de replicação atuais. A verificação ajuda a visualizar:
   * quais podem ser substituídos por esse recurso padrão,
   * quais configurações devem ser movidas para o código
   * e quais não são compatíveis.
* Qualquer uso de agentes de replicação no código personalizado ou em workflows deve ser revisado durante a atualização para o AEM as a Cloud Service.
* Inicialmente, a replicação inversa não é suportada no AEM as a Cloud Service.
* Não é necessário configurar um agente de limpeza do Dispatcher separado. Em vez disso, ele é configurado automaticamente no ambiente do AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar, alterar e otimizar a funcionalidade personalizada diretamente dependente dos agentes de replicação e torná-la compatível com o AEM as a Cloud Service. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication" text="Replicação - AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Consulte as [Diretrizes de desenvolvimento](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents) e notas de versão para [agentes de replicação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents) do AEM as a Cloud Service.
* Revise, altere e otimize a funcionalidade diretamente dependente dos agentes de replicação para executar tarefas comerciais.
* Veja como a implantação no AEM as a Cloud Service afeta a [replicação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication).
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
