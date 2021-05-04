---
title: OAUI
description: Página de ajuda do código do Detector de padrões
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 3%

---

# OAUI {#oaui}

Instância de usuários do OAuth

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="Instância de usuários do OAuth"
>abstract="O código OAUI identifica o padrão em que há pelo menos um usuário configurado relacionado ao OAuth que requer migração correta. O OAuth é configurado para usuários quando há um subnó chamado oauth diretamente em um nó rep:AuthorizableId na forma de /home/user-path/user-node/oauth"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR" text="AEM as a Cloud Service - Notas de versão"

`OAUI` identifica o padrão em que há pelo menos um usuário configurado relacionado ao OAuth que requer a migração correta.

O OAuth é configurado para usuários quando há um subnó chamado `oauth` diretamente em um nó `rep:AuthorizableId` no formato `/home/user-path/user-node/oauth`.

Um exemplo é: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Possíveis implicações e riscos {#implications-and-risks}

* Os usuários externos configurados com OAuth não poderão fazer logon em instâncias de autor/publicação até que sejam reconfigurados com o procedimento abaixo.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Diretrizes de implementação"
>abstract="Os usuários externos configurados com OAuth não poderão fazer logon em instâncias de autor/publicação até que sejam reconfigurados para serem compatíveis com AEM como Cloud Service. O AEM as a Cloud Service oferece suporte à autenticação IMS somente para usuários de Autor, Administrador e Desenvolvimento e integração baseada em SAML para os ambientes de publicação. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html" text="Suporte IMS - AEM como um Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/personalization/user-and-group-sync-for-publish-tier.html?lang=en#integration-with-an-idp" text="Integração SAML - Publicação"

* Entre em contato com seu representante do Adobe para discutir as opções de migração de usuário.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
