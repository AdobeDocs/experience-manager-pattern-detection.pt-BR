---
title: CTEM
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 4%

---


# CTEM {#ctem}

Modelo personalizado

## Segundo plano {#background}

`CTEM` identifica modelos personalizados que foram instalados em AEM. Estas informações são fornecidas para efeitos da avaliação das melhores práticas.

Os modelos são identificados por um valor de tipo primário de &quot;cq:Template&quot;. Um subtipo é usado com este código para identificar a categoria do template:

* `custom.editable.template`: O caminho do modelo não começa com &quot;/apps&quot;.
* `custom.static.template`: O caminho do modelo começa com &quot;/apps&quot;.

## Possíveis implicações e riscos {#implications-and-risks}

* A Prática recomendada é mover todos os modelos estáticos para modelos editáveis.

## Possíveis soluções {#solutions}

* Aproveite as [Ferramentas de Modernização AEM](https://opensource.adobe.com/aem-modernize-tools/) para migrar Modelos estáticos para Modelos editáveis.
* Encontre mais informações sobre Modelos editáveis em [Modelos](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html).
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
