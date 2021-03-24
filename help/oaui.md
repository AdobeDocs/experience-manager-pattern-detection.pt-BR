---
title: OAUI
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# OAUI {#oaui}

Instância de usuários do OAuth

## Segundo plano {#background}

`OAUI` identifica o padrão em que há pelo menos um usuário configurado relacionado ao OAuth que requer a migração correta.

O OAuth é configurado para usuários quando há um subnó chamado `oauth` diretamente em um nó `rep:AuthorizableId` no formato `/home/user-path/user-node/oauth`.

Um exemplo é: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Possíveis implicações e riscos {#implications-and-risks}

* Os usuários externos configurados com OAuth não poderão fazer logon em instâncias de autor/publicação até que sejam reconfigurados com o procedimento abaixo.

## Possíveis soluções {#solutions}

* Entre em contato com seu representante do Adobe para discutir as opções de migração de usuário.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
