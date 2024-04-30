---
title: PCX
description: Página de ajuda de códigos do detector de padrões.
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 95%

---

# PCX {#pcx}

Complexidade da página

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Complexidade da página"
>abstract="O PCX identifica páginas que contêm um grande número de nós em sua estrutura."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Alterações importantes no AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Notas de versão do AEM as a Cloud Service"

`PCX`  Identifica páginas que contêm muitos nós em sua estrutura.

Os subtipos são usados para identificar os diferentes tipos de informações:

* `page.complexity.medium`: uma página contém um número moderadamente alto de nós que podem afetar o desempenho da renderização.
* `page.complexity.high`: uma página contém um número alto de nós, o que pode afetar o desempenho da renderização.

## Possíveis implicações e riscos {#implications-and-risks}

* Um grande número de nós em uma página pode afetar o desempenho de renderização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar a estrutura do conteúdo para reduzir a complexidade da página, o que ajuda a melhorar o desempenho de renderização. Entre em contato com o Suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html?lang=pt-BR" text="Suporte da Experience Cloud"

* Reduza o número total de nós em uma página com a seguinte ação:
   * Verifique se não há contêineres desnecessários.
   * Teste se o mesmo layout pode ser obtido com menos contêineres.
   * Simplifique o conteúdo da página.
   * Reduza a profundidade da estrutura do nó.
   * Fatore novamente os Fragmentos de experiência inclusos para maior simplicidade.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
