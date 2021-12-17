---
title: NCC
description: Página de ajuda do código do Detector de padrões
source-git-commit: fdc3e8bdef27de971743a9ecb04d3912cf8e60ad
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 3%

---

# NCC {#ncc}

Alterações não compatíveis

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Alterações não compatíveis"
>abstract="A CNCC identifica a situação em que alguns nós ou pacotes JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Alterações importantes - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR" text="Notas de versão - AEM as a Cloud Service"

`NCC` identifica a situação em que alguns nós ou pacotes JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização.

## Possíveis implicações e riscos {#implications-and-risks}

* A funcionalidade que depende de qualquer componente que use alterações não compatíveis pode ser corrompida e pode não ser resolvida corretamente.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade AEM podem não funcionar corretamente após uma atualização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar o código personalizado e garantir que apenas os componentes compatíveis do Sling sejam sobrepostos ou referenciados. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Sobreposições"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* Sobrepor ou fazer referência somente a componentes compatíveis do Sling.
* Considere adaptar os recursos provenientes de `/libs` ou pacotes após uma atualização de AEM.
* Entre em contato com a [Equipe de suporte AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou dar resposta a preocupações.
