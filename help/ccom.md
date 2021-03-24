---
title: CCOM
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---


# CCOM {#ccom}

Componente personalizado

## Segundo plano {#background}

`CCOM` identifica componentes personalizados que foram instalados no AEM. Estas informações são fornecidas para efeitos da avaliação das melhores práticas.

Um subtipo é usado com este código para identificar a categoria do componente:

* `custom.core`: Um supertipo na cadeia de supertipos do componente contém &quot;core/wcm/components/&quot;, indicando que ele herda de um componente principal.
* `custom.foundation`: Um supertipo na cadeia de supertipos do componente contém &quot;core/wcm/components/&quot;, indicando que ele herda de um componente principal.
* `custom.overlay.foundation`: O caminho do componente contém &quot;wcm/foundation/components/&quot; ou &quot;foundation/components/&quot;, indicando que ele sobrepõe um componente de fundação.
* `custom`: O componente personalizado não herda ou sobrepõe um componente principal ou de base.

## Possíveis implicações e riscos {#implications-and-risks}

* A prática recomendada é minimizar o número de componentes personalizados, aproveitar os componentes principais e usar os componentes principais com o Sistema de estilos para reduzir a dívida técnica.

## Possíveis soluções {#solutions}

* Encontre mais informações sobre os Componentes principais em [Introdução dos componentes principais](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=pt-BR).
* Encontre mais informações sobre o Sistema de estilos em [Usando o Sistema de estilos](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring).
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
