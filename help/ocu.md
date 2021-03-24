---
title: OCU
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# OCU {#ocu}

Uso de código desatualizado

## Segundo plano {#background}

`OCU` identifica a situação em que alguns nós do JCR, como componentes do Sling ou AEM ou exportações OSGi de API, são alterados ou removidos de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. Eles podem ser atualizados para uma versão não compatível ou não podem estar disponíveis.

Como as versões antigas não são instaladas por padrão, o aplicativo do cliente pode não funcionar corretamente.

## Possíveis implicações e riscos {#implications-and-risks}

* A funcionalidade que depende de qualquer componente que usa componentes ou APIs obsoletos pode ser corrompida e pode não ser resolvida corretamente após uma atualização.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade AEM podem não funcionar corretamente ou podem não estar ativos após uma atualização.

## Possíveis soluções {#solutions}

* A curto prazo: A instalação do pacote de compatibilidade pode ajudar.
* A longo prazo: Adapte o código do cliente para usar a versão mais recente de componentes ou APIs AEM.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
