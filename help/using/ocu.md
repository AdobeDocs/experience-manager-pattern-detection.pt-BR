---
title: OCU
description: Página de ajuda do código do Detector de padrões.
exl-id: cb28c727-415d-436c-ab74-cf7f1f34f7c7
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 91%

---

# OCU {#ocu}

OBSOLETO: Uso de código desatualizado (substituído pelo OU, Uso desatualizado)

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_overview"
>title="Uso de código desatualizado"
>abstract="O código OCU identifica a situação em que alguns nós do JCR, como componentes do Sling ou do AEM ou exportações OSGi de API, são alterados ou removidos de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. Eles podem ser atualizados para uma versão não compatível ou podem simplesmente não estar disponíveis."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=pt-BR" text="Alterações importantes no AEM as a Cloud Service"

O código `OCU` identifica a situação em que alguns nós do JCR, como componentes do Sling ou do AEM ou exportações OSGi de API, são alterados ou removidos de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. Eles podem ser atualizados para uma versão não compatível ou podem simplesmente não estar disponíveis.

Como as versões antigas não são instaladas por padrão, o aplicativo do cliente pode não funcionar corretamente.

## Possíveis implicações e riscos {#implications-and-risks}

* A funcionalidade que depende de qualquer componente que usa componentes ou APIs obsoletos pode ser corrompida e pode não ser resolvida corretamente após uma atualização.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade do AEM podem não funcionar corretamente ou podem não estar ativos após uma atualização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar e adaptar o código do cliente para usar a versão mais recente de componentes ou APIs do AEM. Entre em contato com o Suporte do Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="API do SDK do Adobe Experience Manager"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* A curto prazo: a instalação do pacote de compatibilidade pode ajudar.
* A longo prazo: adapte o código do cliente para usar a versão mais recente de componentes ou APIs do AEM.
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) esclarecimentos ou de ter preocupações em conta.
