---
title: OAUI
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 88%

---

# OAUI {#oaui}

Instância de usuários do OAuth

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="Instância de usuários do OAuth"
>abstract="O código OAUI identifica o padrão em que há pelo menos um usuário configurado relacionado ao OAuth que requer a migração correta. O OAuth é configurado para usuários quando há um subnó chamado OAuth diretamente em um nó rep:AuthorizableId, na forma de /home/user-path/user-node/oauth"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Notas de versão do AEM as a Cloud Service"

`OAUI` identifica o padrão no qual há pelo menos um usuário configurado relacionado ao OAuth que precisa de uma migração correta.

O OAuth é configurado para usuários quando há um subnó chamado `oauth` diretamente em um nó `rep:AuthorizableId`, na forma de `/home/user-path/user-node/oauth`.

Um exemplo é: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Possíveis implicações e riscos {#implications-and-risks}

* Usuários externos configurados com OAuth não poderão fazer logon em instâncias de criação/publicação até que sejam reconfiguradas com o procedimento abaixo.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Diretrizes de implementação"
>abstract="Usuários externos configurados com OAuth não poderão fazer logon em instâncias de criação/publicação até que sejam reconfigurados para serem compatíveis com o AEM as a Cloud Service. O AEM as a Cloud Service oferece suporte à autenticação IMS somente para usuários do tipo Autor, Admin e Desenvolvedor e para a integração baseada em SAML nos ambientes de publicação. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/security/ims-support" text="Suporte IMS - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/sites/authoring/personalization/user-and-group-sync-for-publish-tier#integration-with-an-idp" text="Integração SAML - Publicação"

* Entre em contato com o(a) representante da Adobe para discutir as opções de migração de usuário.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
