---
title: LOCAL
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 1%

---


# LOCAL {#locp}

/libs Substituição de pacotes personalizados

## Segundo plano {#background}

`LOCP` identifica a detecção de um pacote personalizado que fornece conteúdo para o  `/libs`, que é um antipadrão (exceto no caso de ACLs).

## Possíveis implicações e riscos {#implications-and-risks}

* O código do cliente pode ser excluído ou substituído para qualquer atualização de CFP, SP ou AEM principal.
* Em alguns casos, o novo conteúdo pode não estar instalado corretamente.

## Possíveis soluções {#solutions}

* Os pacotes do cliente devem implantar conteúdo em `/apps` em vez de `/libs`.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
