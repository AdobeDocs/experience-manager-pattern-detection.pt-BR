---
title: CTEM
description: Página de ajuda do código do Detector de padrões
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 5%

---

# CTEM {#ctem}

Modelo personalizado

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Modelo personalizado"
>abstract="O CTEM identifica componentes personalizados que foram instalados no AEM. Estas informações são fornecidas para efeitos da avaliação das melhores práticas"

`CTEM` identifica modelos personalizados que foram instalados em AEM. Estas informações são fornecidas para efeitos da avaliação das melhores práticas.

Os modelos são identificados por um valor de tipo primário de &quot;cq:Template&quot;. Um subtipo é usado com este código para identificar a categoria do template:

* `custom.editable.template`: O caminho do modelo não começa com &quot;/apps&quot;.
* `custom.static.template`: O caminho do modelo começa com &quot;/apps&quot;.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Diretrizes de implementação"
>abstract="A Prática recomendada é mover todos os modelos estáticos para modelos editáveis. Os clientes podem aproveitar as Ferramentas de Modernização de AEM existentes para migrar Modelos estáticos para Modelos editáveis."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html" text="Modelos editáveis"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Ferramentas de Modernização do AEM"

* A Prática recomendada é mover todos os modelos estáticos para modelos editáveis.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Ferramentas e recursos"
>abstract="Com a ajuda do AEM Modernization Suite, os clientes podem manipular a estrutura de uma página de uma definição estática, para um modelo editável. O objetivo é ajudar os clientes a migrar dos recursos limitados dos recursos herdados para as ofertas de AEM robustas e modernas. Essas ferramentas são configuráveis, com reconhecimento de configuração e extensíveis. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/page-structure.html" text="Conversor de estrutura de página"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* Aproveite as [Ferramentas de Modernização AEM](https://opensource.adobe.com/aem-modernize-tools/) para migrar Modelos estáticos para Modelos editáveis.
* Encontre mais informações sobre Modelos editáveis em [Modelos](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html).
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
