---
title: OU
description: Página de ajuda de códigos do detector de padrões
exl-id: 6ec96fab-dd6e-46af-864f-05dad387cbb6
source-git-commit: 8b8d902dc5b5a8534475d256c199dc235bb35464
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# OU {#ou}

Uso desatualizado

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_overview"
>title="Uso desatualizado"
>abstract="A OU identifica a situação em que alguns nós do JCR, como componentes do Sling ou do AEM, ou exportações de API OSGi, são alterados ou removidos de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. Eles podem ser atualizados para uma versão não compatível ou podem simplesmente não estar disponíveis."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=pt-BR" text="Alterações importantes no AEM as a Cloud Service"

`OU` identifica a situação em que alguns nós do JCR, como componentes do Sling ou do AEM, ou exportações de API OSGi, são alterados ou removidos de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. Eles podem ser atualizados para uma versão não compatível ou podem simplesmente não estar disponíveis.

Como as versões antigas não são instaladas por padrão, o aplicativo do cliente pode não funcionar corretamente.

## Possíveis implicações e riscos {#implications-and-risks}

* A funcionalidade que depende de qualquer componente que usa componentes ou APIs obsoletos pode ser corrompida e pode não ser resolvida corretamente após uma atualização.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade do AEM podem não funcionar corretamente ou podem não estar ativos após uma atualização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar e adaptar o código do cliente para usar a versão mais recente de componentes ou APIs do AEM. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="API do SDK do Adobe Experience Manager"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* A curto prazo: a instalação do pacote de compatibilidade pode ajudar.
* A longo prazo: adapte o código do cliente para usar a versão mais recente de componentes ou APIs do AEM.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
