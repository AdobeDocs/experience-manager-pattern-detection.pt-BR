---
title: CTEM
description: Página de ajuda do código do Detector de padrões.
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 68%

---

# CTEM {#ctem}

Modelo personalizado

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Modelo personalizado"
>abstract="O código CTEM identifica componentes personalizados que foram instalados no AEM. Estas informações são fornecidas para subsidiar a avaliação de práticas recomendadas"

O código CTEM identifica modelos personalizados que foram instalados no AEM. Estas informações são fornecidas para efeitos de avaliação de práticas recomendadas.

Os modelos são identificados por um valor de tipo primário de `cq:Template`. Um subtipo é usado com este código para identificar a categoria do modelo:

* `custom.editable.template`: o caminho do modelo não começa com &quot;/apps&quot;.
* `custom.static.template`: o caminho do modelo começa com &quot;/apps&quot;.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é mover todos os modelos estáticos para modelos editáveis. Os clientes podem usar as Ferramentas de modernização do AEM existentes para migrar Modelos estáticos para Modelos editáveis."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/templates/templates" text="Modelos editáveis"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Ferramentas de modernização do AEM"

* A prática recomendada é mover todos os modelos estáticos para modelos editáveis.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Ferramentas e recursos"
>abstract="Com a ajuda do Conjunto de modernização do AEM, os clientes podem manipular a estrutura de uma página, de uma definição estática para um modelo editável. O objetivo é ajudar os clientes a migrar das funcionalidades limitadas dos recursos herdados para as ofertas robustas e modernas do AEM. Essas ferramentas são configuráveis, extensíveis e possuem reconhecimento de configuração. Entre em contato com o Suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/structure/about.html" text="Conversor de estrutura de página"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Use o [Ferramentas de modernização do AEM](https://opensource.adobe.com/aem-modernize-tools/) para migrar Modelos estáticos para Modelos editáveis.
* Encontre mais informações sobre Modelos editáveis em [Modelos](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/templates/templates).
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) esclarecimentos ou de ter preocupações em conta.
