---
title: OCU
description: Página de ajuda referente ao código do detector de padrões.
exl-id: cb28c727-415d-436c-ab74-cf7f1f34f7c7
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 100%

---

# OCU {#ocu}

OBSOLETO: Uso de código desatualizado (substituído pelo OU, Uso desatualizado)

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_overview"
>title="Uso de código desatualizado"
>abstract="O código OCU identifica a situação em que alguns nós do JCR, como componentes do Sling ou do AEM ou exportações OSGi de API, são alterados ou removidos de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. Eles podem ser atualizados para uma versão incompatível ou podem simplesmente não estar disponíveis."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Alterações importantes: AEM as a Cloud Service"

`OCU` identifica a situação em que alguns nós do JCR, como componentes do Sling ou do AEM, ou exportações do OSGi da API, são alterados ou removidos de forma incompatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. Eles podem ser atualizados para uma versão incompatível ou podem simplesmente não estar disponíveis.

Como as versões antigas não são instaladas por padrão, o aplicativo do cliente pode não funcionar corretamente.

## Possíveis implicações e riscos {#implications-and-risks}

* A funcionalidade que depende de qualquer componente que usa componentes ou APIs obsoletos pode ser corrompida e pode não ser resolvida corretamente após uma atualização.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade do AEM podem não funcionar corretamente ou podem não estar ativos após uma atualização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar e adaptar o código do cliente para usar a versão mais recente de componentes ou APIs do AEM. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="API do SDK do Adobe Experience Manager"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Curto prazo: a instalação do pacote de compatibilidade pode ajudar.
* Longo prazo: adapte o código do cliente para usar a versão mais recente de componentes ou APIs do AEM.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar os suas considerações.
