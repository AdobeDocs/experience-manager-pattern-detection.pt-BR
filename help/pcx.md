---
title: PCX
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# PCX {#pcx}

Complexidade da página

## Segundo plano {#background}

`PCX` identifica páginas que contêm um grande número de nós em sua estrutura.

Os subtipos são usados para identificar os diferentes tipos de informações:

* `page.complexity.medium`: Uma página contém um número moderadamente alto de nós que pode afetar o desempenho da renderização.
* `page.complexity.high`: Uma página contém um número muito alto de nós que provavelmente afetarão o desempenho da renderização.

## Possíveis implicações e riscos {#implications-and-risks}

* Um grande número de nós em uma página pode afetar seu desempenho de renderização.

## Possíveis soluções {#solutions}

* Execute etapas para reduzir o número total de nós em uma página, incluindo:
   * Verifique se não há contêineres desnecessários.
   * Teste se o mesmo layout pode ser obtido com menos contêineres.
   * Simplifique o conteúdo da página.
   * Reduza a profundidade da estrutura do nó.
   * Refatere os Fragmentos de experiência incluídos para simplificar.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
