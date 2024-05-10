---
title: OU
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 6ec96fab-dd6e-46af-864f-05dad387cbb6
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '269'
ht-degree: 100%

---

# OU {#ou}

Uso desatualizado

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_overview"
>title="Uso desatualizado"
>abstract="A OU identifica a situação em que alguns nós do JCR, como componentes do Sling ou do AEM, ou exportações de API OSGi, são alterados ou removidos de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. Eles podem ser atualizados para uma versão incompatível ou podem simplesmente não estar disponíveis."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Alterações importantes: AEM as a Cloud Service"

`OU` identifica a situação em que alguns nós do JCR, como componentes do Sling ou do AEM, ou exportações do OSGi da API, são alterados ou removidos de forma incompatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. Eles podem ser atualizados para uma versão incompatível ou podem simplesmente não estar disponíveis.

Como as versões antigas não são instaladas por padrão, o aplicativo do cliente pode não funcionar corretamente.

## Possíveis implicações e riscos {#implications-and-risks}

* A funcionalidade que depende de qualquer componente que usa componentes ou APIs obsoletos pode ser corrompida e pode não ser resolvida corretamente após uma atualização.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade do AEM podem não funcionar corretamente ou podem não estar ativos após uma atualização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar e adaptar o código do cliente para usar a versão mais recente de componentes ou APIs do AEM. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="API do SDK do Adobe Experience Manager"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Curto prazo: a instalação do pacote de compatibilidade pode ajudar.
* Longo prazo: adapte o código do cliente para usar a versão mais recente de componentes ou APIs do AEM.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar os suas considerações.
