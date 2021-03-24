---
title: TRAVÃO
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 1%

---


# WRK {#wrk}

Fluxo de trabalho

## Segundo plano {#background}

`WRK` identifica uma conclusão relacionada a um modelo de fluxo de trabalho ou iniciador. Eles são relatados porque os modelos de fluxo de trabalho de ativos personalizados devem ser migrados ao atualizar para o AEM como um Cloud Service.

Um subtipo é usado para identificar o tipo de problema de fluxo de trabalho detectado no momento.

* `custom.asset.workflow`: Detecção de um modelo ou iniciador de fluxo de trabalho de ativo personalizado.

## Possíveis implicações e riscos {#implications-and-risks}

* Tradicionalmente, o processamento de ativos é executado com fluxos de trabalho de ativos executados na instância do autor do AEM. Com o AEM como Cloud Service, o processamento de ativos agora é realizado pelos microsserviços de ativos. (Consulte a [visão geral dos microsserviços de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html) para obter mais informações.
* Os fluxos de trabalho de ativos padrão são compatíveis automaticamente com meus microsserviços de ativos.
* As personalizações em workflows de ativos exigem migração para funcionar com o AEM como um Cloud Service.

## Possíveis soluções {#solutions}

* Se um modelo ou iniciador de fluxo de trabalho de ativo personalizado for identificado, planeje executar a [Ferramenta Migração de fluxo de trabalho de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html).
* Revise o [Introdução ao uso dos microsserviços de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html) para obter mais informações.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
