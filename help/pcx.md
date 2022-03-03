---
title: PCX
description: Página de ajuda de códigos do detector de padrões
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# PCX {#pcx}

Complexidade da página

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Complexidade da página"
>abstract="O PCX identifica páginas que contêm um grande número de nós em sua estrutura."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=pt-BR" text="Alterações importantes no AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR" text="O AEM as a Cloud Service - notas de versão"

O `PCX` identifica páginas que contêm um grande número de nós em sua estrutura.

Os subtipos são usados para identificar os diferentes tipos de informações:

* `page.complexity.medium`: uma página contém um número moderadamente alto de nós que podem afetar o desempenho da renderização.
* `page.complexity.high`: uma página contém um número muito alto de nós que provavelmente afetarão o desempenho da renderização.

## Possíveis implicações e riscos {#implications-and-risks}

* Um grande número de nós em uma página pode afetar seu desempenho de renderização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é analisar a estrutura do conteúdo para reduzir a complexidade da página, o que ajudaria a melhorar o desempenho da renderização da página. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Execute etapas para reduzir o número total de nós em uma página, incluindo:
   * Verifique se não há contêineres desnecessários.
   * Teste se o mesmo layout pode ser obtido com menos contêineres.
   * Simplifique o conteúdo da página.
   * Reduza a profundidade da estrutura do nó.
   * Fatore novamente os Fragmentos de experiência inclusos para maior simplicidade.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
