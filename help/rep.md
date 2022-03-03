---
title: REP
description: Página de ajuda de códigos do detector de padrões
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# [!DNL REP] {#rep}

Agente de replicação

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Agente de replicação"
>abstract="O código REP identifica agentes de replicação ativados. Eles são relatados por causa do potencial para problemas que devem ser abordados ao atualizar para o AEM as a Cloud Service. O AEM as a Cloud Service usa o Sling Content Distribution para distribuir conteúdo do autor para os ambientes de publicação. Isso é feito fora do tempo de execução do AEM usando o serviço de pipeline do Adobe I/O. Isso é configurado automaticamente no ambiente provisionado do AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=pt-BR#replication-agents" text="Alterações importantes no AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=pt-BR#no-reverse-replication-agents" text="Diretrizes de desenvolvimento"

O código `REP` identifica agentes de replicação ativados. Eles são relatados por causa do potencial para problemas que devem ser abordados ao atualizar para o AEM as a Cloud Service.

O AEM as a Cloud Service usa o [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) para distribuir conteúdo do autor para os ambientes de publicação. Isso é feito fora do tempo de execução do AEM usando o serviço de pipeline do Adobe I/O. Isso é configurado automaticamente no ambiente provisionado do AEM as a Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

* A configuração da replicação foi alterada com o AEM as a Cloud Service. Todos os agentes de replicação atuais devem ser revisados para ver quais são substituídos pelo recurso padrão, quais configurações devem ser movidas para o código e quais não são compatíveis.
* Qualquer uso de agentes de replicação no código personalizado ou em workflows deve ser revisado durante a atualização para o AEM as a Cloud Service.
* Inicialmente, a replicação inversa não é suportada no AEM as a Cloud Service.
* Não há necessidade de configurar um agente de liberação do dispatcher separado. Isso é configurado automaticamente no ambiente do AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar, alterar e otimizar a funcionalidade personalizada diretamente dependente dos agentes de replicação e torná-la compatível com o AEM as a Cloud Service. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=pt-BR#replication" text="Replicação - AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Consulte as [Diretrizes de desenvolvimento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=pt-BR#no-reverse-replication-agents) e notas de versão para [agentes de replicação](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=pt-BR#replication-agents) do AEM as a Cloud Service.
* Revise, altere e otimize a funcionalidade diretamente dependente dos agentes de replicação para executar tarefas comerciais.
* Veja como a [replicação](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=pt-BR#replication) é afetada pela implantação no AEM as a Cloud Service.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
