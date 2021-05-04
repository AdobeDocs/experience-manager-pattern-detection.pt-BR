---
title: DOPI
description: Página de ajuda do código do Detector de padrões
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# DOPI {#dopi}

Índice de propriedades ordenadas obsoleto

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Índice de propriedades ordenadas obsoleto"
>abstract="O código DOPI identifica o uso de definições de índice de propriedade ordenada (primaryType=oak:QueryIndexDefinition AND type=&quot;ordered&quot;), que foram descontinuadas desde a versão 6.1 e removidas na versão 6.2."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=en#the-ordered-index" text="Índice ordenado - obsoleto"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html" text="Indexação - AEM como um Cloud Service"

`DOPI` O identifica o uso de definições de índice de propriedade ordenadas (`primaryType=oak:QueryIndexDefinition` AND  `type="ordered"`), que foram descontinuadas desde a versão 6.1 e removidas na versão 6.2.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Diretrizes de implementação"
>abstract="A Prática Recomendada é revisar todos os índices ordenados obsoletos e movê-los para a forma de índices lucene suportados para evitar problemas significativos de desempenho ou necessidades não funcionais do cliente."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/practices/best-practices-for-queries-and-indexing.html" text="Práticas recomendadas - Consultas e indexação"

* Algumas consultas podem não responder.
* A funcionalidade do cliente pode funcionar incorretamente.
* Avisos transversais ou até mesmo erros e sanções significativas de desempenho como índices obsoletos não têm efeito.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Ferramentas e recursos"
>abstract="Revise o projeto herdado WKND para entender como as violações de DOPI podem ser tornadas compatíveis com AEM Cloud Service. Além disso, analise o exemplo de violação de DOPI no Github para entender como os índices ordenados herdados podem ser convertidos em índices baseados em Lucene, que são suportados no AEM como um Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Projeto WKND-Legacy"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Exemplo de violação de DOPI - Github"

* Modifique a definição do índice para se tornar, ou substitua o índice por, uma definição de índice compatível. (Consulte [Consultas e Indexação do Oak](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html)).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) e entenda como [as violações de DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) podem ser corrigidas e tornadas compatíveis com AEM como um Cloud Service.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
