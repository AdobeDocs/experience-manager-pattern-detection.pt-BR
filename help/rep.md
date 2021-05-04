---
title: REP
description: Página de ajuda do código do Detector de padrões
exl-id: e788deba-a301-404f-8e90-51f721409e69
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 2%

---

# [!DNL REP] {#rep}

Agente de replicação

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Agente de replicação"
>abstract="O REP identifica agentes de replicação ativados. Eles são relatados devido ao potencial para problemas que devem ser abordados ao atualizar para o AEM como um Cloud Service. O AEM como Cloud Service usa a Distribuição de conteúdo de sling para distribuir o conteúdo do autor para os ambientes de publicação. Isso é feito fora do tempo de execução AEM usando o serviço de pipeline do Adobe I/O. Isso é configurado automaticamente no AEM provisionado como um ambiente Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents" text="Alterações importantes - AEM como um Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents" text="Diretrizes de desenvolvimento"

`REP` identifica agentes de replicação ativados. Eles são relatados devido ao potencial para problemas que devem ser abordados ao atualizar para o AEM como um Cloud Service.

O AEM como Cloud Service usa [Distribuição de conteúdo de sling](https://sling.apache.org/documentation/bundles/content-distribution.html) para distribuir conteúdo do autor para publicar ambientes. Isso é feito fora do tempo de execução AEM usando o serviço de pipeline do Adobe I/O. Isso é configurado automaticamente no AEM provisionado como um ambiente Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

* A configuração da replicação foi alterada com AEM como Cloud Service. Todos os agentes de replicação atuais devem ser revisados para ver quais são substituídos pelo recurso padrão, quais configurações devem ser movidas para código e quais não são suportadas.
* Qualquer uso de agentes de replicação no código personalizado ou em workflows deve ser revisado durante a atualização para o AEM como um Cloud Service.
* Inicialmente, a replicação inversa não é compatível no AEM como Cloud Service.
* Não há necessidade de configurar um agente de liberação do dispatcher separado. Isso é configurado automaticamente no AEM como um ambiente Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar, refatorar e otimizar a funcionalidade personalizada diretamente dependente dos agentes de replicação e torná-la compatível com o AEM como Cloud Service. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication" text="Replicação - AEM como Cloud Service"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* Consulte o AEM como Cloud Service [Diretrizes de desenvolvimento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents) e notas de versão para [agentes de replicação](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents).
* Revise, refatere e otimize a funcionalidade diretamente dependente dos agentes de replicação para executar tarefas comerciais.
* Veja como [replication](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication) é afetado pela implantação no AEM como um Cloud Service.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
