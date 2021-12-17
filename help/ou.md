---
title: OU
description: Página de ajuda do código do Detector de padrões
source-git-commit: fdc3e8bdef27de971743a9ecb04d3912cf8e60ad
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---

# OU {#ou}

Uso desatualizado

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_overview"
>title="Uso desatualizado"
>abstract="A OU identifica a situação em que alguns nós do JCR, como componentes do Sling ou AEM ou exportações de OSGi de API, são alterados ou removidos de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. Eles podem ser atualizados para uma versão não compatível ou não podem estar disponíveis."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Alterações importantes - AEM as a Cloud Service"

`OU` identifica a situação em que alguns nós do JCR, como componentes do Sling ou AEM ou exportações OSGi de API, são alterados ou removidos de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. Eles podem ser atualizados para uma versão não compatível ou não podem estar disponíveis.

Como as versões antigas não são instaladas por padrão, o aplicativo do cliente pode não funcionar corretamente.

## Possíveis implicações e riscos {#implications-and-risks}

* A funcionalidade que depende de qualquer componente que usa componentes ou APIs obsoletos pode ser corrompida e pode não ser resolvida corretamente após uma atualização.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade AEM podem não funcionar corretamente ou podem não estar ativos após uma atualização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar e adaptar o código do cliente para usar a versão mais recente de componentes ou APIs AEM. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="API do SDK do Adobe Experience Manager"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* A curto prazo: A instalação do pacote de compatibilidade pode ajudar.
* A longo prazo: Adapte o código do cliente para usar a versão mais recente de componentes ou APIs AEM.
* Entre em contato com a [Equipe de suporte AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou dar resposta a preocupações.
