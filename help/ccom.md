---
title: CCOM
description: Página de ajuda do código do Detector de padrões
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 6%

---

# CCOM {#ccom}

Componente personalizado

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Componente personalizado"
>abstract="O CCOM identifica componentes personalizados que foram instalados no AEM. Estas informações são fornecidas para efeitos da avaliação das melhores práticas"

`CCOM` identifica componentes personalizados que foram instalados no AEM. Estas informações são fornecidas para efeitos da avaliação das melhores práticas.

Um subtipo é usado com este código para identificar a categoria do componente:

* `custom.core`: Um supertipo na cadeia de supertipos do componente contém &quot;core/wcm/components/&quot;, indicando que ele herda de um componente principal.
* `custom.foundation`: Um supertipo na cadeia de supertipos do componente contém &quot;core/wcm/components/&quot;, indicando que ele herda de um componente principal.
* `custom.overlay.foundation`: O caminho do componente contém &quot;wcm/foundation/components/&quot; ou &quot;foundation/components/&quot;, indicando que ele sobrepõe um componente de fundação.
* `custom`: O componente personalizado não herda ou sobrepõe um componente principal ou de base.

## Possíveis implicações e riscos {#implications-and-risks}

* A prática recomendada é minimizar o número de componentes personalizados, aproveitar os componentes principais e usar os componentes principais com o Sistema de estilos para reduzir a dívida técnica.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é minimizar o número de componentes personalizados, aproveitar os componentes principais e usar os componentes principais com o Sistema de estilos para reduzir a dívida técnica."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html" text="Componentes principais"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring" text="Sistema de estilos"

* Encontre mais informações sobre os Componentes principais em [Introdução dos componentes principais](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=pt-BR).
* Encontre mais informações sobre o Sistema de estilos em [Usando o Sistema de estilos](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring).
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
