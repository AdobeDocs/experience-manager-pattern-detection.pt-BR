---
title: DOPI
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# DOPI {#dopi}

Índice de propriedades ordenadas obsoleto

## Segundo plano {#background}

`DOPI` O identifica o uso de definições de índice de propriedade ordenadas (`primaryType=oak:QueryIndexDefinition` AND  `type="ordered"`), que foram descontinuadas desde a versão 6.1 e removidas na versão 6.2.

## Possíveis implicações e riscos {#implications-and-risks}

* Algumas consultas podem não responder.
* A funcionalidade do cliente pode funcionar incorretamente.
* Avisos transversais ou até mesmo erros e sanções significativas de desempenho como índices obsoletos não têm efeito.

## Possíveis soluções {#solutions}

* Modifique a definição do índice para se tornar, ou substitua o índice por, uma definição de índice compatível. (Consulte [Consultas e Indexação do Oak](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html)).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) e entenda como [as violações de DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) podem ser corrigidas e tornadas compatíveis com AEM como um Cloud Service.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
