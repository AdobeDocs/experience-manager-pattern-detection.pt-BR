---
title: WRK
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 92%

---

# WRK {#wrk}

Fluxo de trabalho

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Fluxo de trabalho"
>abstract="O código WRK identifica uma conclusão relacionada a um modelo de fluxo de trabalho ou iniciador. Eles são relatados porque modelos de fluxo de trabalho de ativos personalizados devem ser migrados ao atualizar para o AEM as a Cloud Service. Com o AEM as a Cloud Service, o processamento de ativos agora é realizado pelos microsserviços de ativos."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview" text="Microsserviços de ativos"

`WRK` identifica uma descoberta relacionada a um modelo ou iniciador de fluxo de trabalho. Eles são relatados porque modelos de fluxo de trabalho de ativos personalizados devem ser migrados ao atualizar para o AEM as a Cloud Service.

Um subtipo é usado para identificar o tipo de problema de fluxo de trabalho detectado no momento.

* `custom.asset.workflow`: detecção de um modelo ou iniciador de fluxo de trabalho de ativo personalizado.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Diretrizes de implementação"
>abstract="Os fluxos de trabalho de ativos padrão são automaticamente compatíveis com os microsserviços de ativos. Portanto, a prática recomendada é revisar todos os modelos de fluxo de trabalho de ativos personalizados ou o inicializado para ver se eles são necessários após a transição para o AEM as a Cloud Service. As personalizações em fluxos de trabalho de ativos precisam da migração para funcionar com o AEM as a Cloud Service com a ajuda da ferramenta Migração de fluxo de trabalho de ativos"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use" text="Introdução - Microsserviços de ativos"

* Tradicionalmente, o processamento de ativos é executado com fluxos de trabalho de ativos executados na instância do autor do AEM. Com o AEM as a Cloud Service, o processamento de ativos agora é realizado pelos microsserviços de ativos. Consulte a [visão geral dos microsserviços de ativos](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview) para obter mais informações.
* Os fluxos de trabalho de ativos padrão são automaticamente compatíveis com os microsserviços de ativos.
* As personalizações dos fluxos de trabalho de ativos exigem migração para funcionar com o AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Ferramentas e recursos"
>abstract="Revise e planeje executar a ferramenta Migração de fluxo de trabalho de ativos depois que um modelo de fluxo de trabalho de ativos personalizado ou iniciador for identificado. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool" text="Ferramenta Migração de fluxo de trabalho de ativos"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Se um modelo ou iniciador de fluxo de trabalho de ativo personalizado for identificado, planeje executar a [ferramenta Migração de fluxo de trabalho de ativos](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool).
* Revise a [Introdução ao uso dos microsserviços de ativos](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use) para obter mais informações.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
