---
title: NBCC
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# NBCC {#nbcc}

Alterações compatíveis com versões anteriores

## Segundo plano {#background}

`NBCC` identifica a situação em que alguns nós ou pacotes JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização.

## Possíveis implicações e riscos {#implications-and-risks}

* A funcionalidade que depende de qualquer componente que use alterações compatíveis não retroativas pode ser interrompida e pode não ser resolvida corretamente.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade AEM podem não funcionar corretamente após uma atualização.

## Possíveis soluções {#solutions}

* Sobrepor ou fazer referência somente a componentes Sling compatíveis com versões anteriores.
* Considere adaptar recursos que vêm de `/libs` ou pacotes após uma atualização AEM.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
