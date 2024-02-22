---
title: OAUI
description: Página de ajuda de códigos do detector de padrões
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '231'
ht-degree: 100%

---

# OAUI {#oaui}

Instância de usuários do OAuth

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="Instância de usuários do OAuth"
>abstract="O código OAUI identifica o padrão em que há pelo menos um usuário configurado relacionado ao OAuth que requer a migração correta. O OAuth é configurado para usuários quando há um subnó chamado oauth diretamente em um nó rep:AuthorizableId, na forma de /home/user-path/user-node/oauth"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR" text="O AEM as a Cloud Service - notas de versão"

O código `OAUI` identifica o padrão em que há pelo menos um usuário configurado relacionado ao OAuth que requer a migração correta.

O OAuth é configurado para usuários quando há um subnó chamado `oauth` diretamente em um nó `rep:AuthorizableId`, na forma de `/home/user-path/user-node/oauth`.

Um exemplo é: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Possíveis implicações e riscos {#implications-and-risks}

* Os usuários externos configurados com OAuth não poderão fazer logon em instâncias de autor/publicação até que sejam reconfiguradas com o procedimento abaixo.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Diretrizes de implementação"
>abstract="Os usuários externos configurados com OAuth não poderão fazer logon em instâncias de autor/publicação até que sejam reconfiguradas para serem compatíveis com o AEM as a Cloud Service. O AEM as a Cloud Service oferece compatibilidade à autenticação IMS somente para usuários Autor, Administrador e Desenvolvedor e integração baseada em SAML para os ambientes de publicação. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=pt-BR" text="Suporte IMS - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/personalization/user-and-group-sync-for-publish-tier.html?lang=pt-BR#integration-with-an-idp" text="Integração SAML - Publicação"

* Entre em contato com seu representante da Adobe para discutir as opções de migração de usuário.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
