---
title: PCX
description: Página de ajuda do código do Detector de padrões.
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 58%

---

# PCX {#pcx}

Complexidade da página

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Complexidade da página"
>abstract="O PCX identifica páginas que contêm um grande número de nós em sua estrutura."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Alterações importantes no AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/br/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="O AEM as a Cloud Service - notas de versão"

O PCX identifica páginas que contêm muitos nós em sua estrutura.

Os subtipos são usados para identificar os diferentes tipos de informações:

* `page.complexity.medium`: uma página contém um número moderadamente alto de nós que podem afetar o desempenho da renderização.
* `page.complexity.high`: uma página contém um alto número de nós que provavelmente afetam o desempenho da renderização.

## Possíveis implicações e riscos {#implications-and-risks}

* Muitos nós em uma página podem afetar seu desempenho de renderização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar a estrutura do conteúdo para reduzir a complexidade da página, o que, por sua vez, ajudaria a melhorar o desempenho de renderização da página. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Reduza o número total de nós em uma página executando a seguinte ação:
   * Verifique se não há contêineres desnecessários.
   * Teste se o mesmo layout pode ser obtido com menos contêineres.
   * Simplifique o conteúdo da página.
   * Reduza a profundidade da estrutura do nó.
   * Fatore novamente os Fragmentos de experiência inclusos para maior simplicidade.
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) esclarecimentos ou de ter preocupações em conta.
