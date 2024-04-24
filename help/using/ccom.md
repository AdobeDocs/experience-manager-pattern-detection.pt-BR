---
title: CCOM
description: Página de ajuda do código do Detector de padrões.
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 66%

---

# CCOM {#ccom}

Componente personalizado

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Componente personalizado"
>abstract="O CCOM identifica componentes personalizados que foram instalados no AEM. Estas informações são fornecidas para subsidiar a avaliação de práticas recomendadas"

`CCOM` Identifica componentes personalizados que foram instalados no AEM. Estas informações são fornecidas para efeitos de avaliação de práticas recomendadas.

Um subtipo é usado com este código para identificar a categoria do componente:

* `custom.core`: um supertipo na cadeia de supertipos do componente contém &quot;core/wcm/components&quot;, indicando que ele herda de um componente principal.
* `custom.foundation`: um supertipo na cadeia de supertipos do componente contém &quot;wcm/components&quot;, indicando que ele herda de um componente principal.
* `custom.overlay.foundation`: o caminho do componente contém &quot;wcm/foundation/components/&quot; ou &quot;foundation/components/&quot;, indicando que ele sobrepõe um componente fundamental.
* `custom`: o componente personalizado não herda ou sobrepõe um componente principal ou fundamental.

## Possíveis implicações e riscos {#implications-and-risks}

* A prática recomendada é minimizar o número de componentes personalizados, usar os componentes principais e usá-los com o Sistema de estilos para que você possa reduzir débitos técnicos.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é minimizar o número de componentes personalizados, usar os componentes principais e usá-los com o Sistema de estilos para reduzir débitos técnicos."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-core-components/using/introduction" text="Componentes principais"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring" text="Sistema de estilos"

* Encontre mais informações sobre os Componentes principais em [Introdução aos componentes principais](https://experienceleague.adobe.com/pt-br/docs/experience-manager-core-components/using/introduction).
* Encontre mais informações sobre o Sistema de estilos em [Uso do sistema de estilos](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring).
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) esclarecimentos ou de ter preocupações em conta.
