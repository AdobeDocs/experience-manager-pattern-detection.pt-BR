---
title: CCOM
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 100%

---

# CCOM {#ccom}

Componente personalizado

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Componente personalizado"
>abstract="O CCOM identifica componentes personalizados que foram instalados no AEM. Essas informações são fornecidas para a avaliação de práticas recomendadas"

`CCOM` Identifica componentes personalizados instalados no AEM. Essas informações são fornecidas para a avaliação de práticas recomendadas.

Um subtipo é usado com este código para identificar a categoria do componente:

* `custom.core`: um supertipo na cadeia de supertipos do componente contém `core/wcm/components/`, indicando que ele herda de um componente principal.
* `custom.foundation`: um supertipo na cadeia de supertipos do componente contém “`core/wcm/components/`”, indicando que ele herda de um componente principal.
* `custom.overlay.foundation`: o caminho do componente contém `wcm/foundation/components/` ou `foundation/components/`, indicando que ele sobrepõe um componente básico.
* `custom`: o componente personalizado não herda ou sobrepõe um componente principal ou fundamental.

## Possíveis implicações e riscos {#implications-and-risks}

* A prática recomendada é minimizar o número de componentes personalizados, utilizar os componentes principais com ou sem o sistema de estilos para reduzir a dívida técnica.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é minimizar o número de componentes personalizados, aproveitar os componentes principais e usá-los com o Sistema de estilos para reduzir a dívida técnica."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-core-components/using/introduction" text="Componentes principais"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring" text="Sistema de estilos"

* Encontre mais informações sobre os Componentes principais em [Introdução aos componentes principais](https://experienceleague.adobe.com/pt-br/docs/experience-manager-core-components/using/introduction).
* Encontre mais informações sobre o Sistema de estilos em [Uso do sistema de estilos](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring).
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
