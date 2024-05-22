---
title: CTEM
description: Página de ajuda referente ao código do detector de padrões.
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 100%

---

# CTEM {#ctem}

Modelo personalizado

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Modelo personalizado"
>abstract="O código CTEM identifica componentes personalizados instalados no AEM. Essas informações são fornecidas para a avaliação de práticas recomendadas"

`CTEM` Identifica modelos personalizados instalados no AEM. Essas informações são fornecidas para a avaliação de práticas recomendadas.

Os modelos têm um valor de tipo principal de `cq:Template`, que ajuda na identificação. Um subtipo é usado com este código para identificar a categoria do modelo:

* `custom.editable.template`: o caminho do modelo não começa com `/apps`.
* `custom.static.template`: o caminho do modelo começa com `/apps`.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é mover todos os modelos estáticos para modelos editáveis. Os clientes podem aproveitar as Ferramentas de modernização do AEM para migrar modelos estáticos para modelos editáveis."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/platform/templates/templates" text="Modelos editáveis"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Ferramentas de Modernização do AEM"

* A prática recomendada é mover todos os modelos estáticos para modelos editáveis. 

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Ferramentas e recursos"
>abstract="Com a ajuda do Conjunto de modernização do AEM, os clientes podem manipular a estrutura de uma página, de uma definição estática para um modelo editável. O objetivo é ajudar os clientes a migrar das funcionalidades limitadas dos recursos herdados para as ofertas robustas e modernas do AEM. Essas ferramentas são configuráveis e extensíveis, e possuem reconhecimento de configuração. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/structure/about.html" text="Conversor de estrutura de página"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Use as [Ferramentas de modernização do AEM](https://opensource.adobe.com/aem-modernize-tools/) para migrar modelos estáticos para modelos editáveis.
* Encontre mais informações sobre Modelos editáveis em [Modelos](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/platform/templates/templates).
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
