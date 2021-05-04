---
title: TRAVÃO
description: Página de ajuda do código do Detector de padrões
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---

# WRK {#wrk}

Fluxo de trabalho

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Fluxo de trabalho"
>abstract="O código WRK identifica uma conclusão relacionada a um modelo de fluxo de trabalho ou iniciador. Eles são relatados porque os modelos de fluxo de trabalho de ativos personalizados devem ser migrados ao atualizar para o AEM como um Cloud Service. Com o AEM como Cloud Service, o processamento de ativos agora é realizado pelos microsserviços de ativos."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html" text="Microsserviços de ativos"

`WRK` identifica uma conclusão relacionada a um modelo de fluxo de trabalho ou iniciador. Eles são relatados porque os modelos de fluxo de trabalho de ativos personalizados devem ser migrados ao atualizar para o AEM como um Cloud Service.

Um subtipo é usado para identificar o tipo de problema de fluxo de trabalho detectado no momento.

* `custom.asset.workflow`: Detecção de um modelo ou iniciador de fluxo de trabalho de ativo personalizado.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Diretrizes de implementação"
>abstract="Como os fluxos de trabalho de ativos padrão são compatíveis automaticamente com meus microsserviços de ativos, a Prática recomendada é revisar todos os modelos ou iniciadores de fluxo de trabalho de ativos personalizados para ver se eles são necessários depois que passamos para o AEM como um Cloud Service. As personalizações em workflows de ativos exigem migração para funcionar com o AEM como um Cloud Service com a ajuda da ferramenta Migração de fluxo de trabalho de ativos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html" text="Introdução - Microserviços de ativos"

* Tradicionalmente, o processamento de ativos é executado com fluxos de trabalho de ativos executados na instância do autor do AEM. Com o AEM como Cloud Service, o processamento de ativos agora é realizado pelos microsserviços de ativos. (Consulte a [visão geral dos microsserviços de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html) para obter mais informações.
* Os fluxos de trabalho de ativos padrão são compatíveis automaticamente com meus microsserviços de ativos.
* As personalizações em workflows de ativos exigem migração para funcionar com o AEM como um Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Ferramentas e recursos"
>abstract="Revise e planeje executar a Ferramenta Migração de fluxo de trabalho de ativos depois que um modelo de fluxo de trabalho de ativos personalizado ou iniciador for identificado. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html" text="Ferramenta Migração de fluxo de trabalho de ativos"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* Se um modelo ou iniciador de fluxo de trabalho de ativo personalizado for identificado, planeje executar a [Ferramenta Migração de fluxo de trabalho de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html).
* Revise o [Introdução ao uso dos microsserviços de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html) para obter mais informações.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
