---
title: NCC
description: Página de ajuda do código do Detector de padrões.
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 65%

---

# NCC {#ncc}

Alterações não compatíveis

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Alterações não compatíveis"
>abstract="O código NCC identifica a situação em que alguns nós ou pacotes JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Alterações importantes no AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Notas de versão - AEM as a Cloud Service"

O código NCC identifica a situação em que alguns nós ou pacotes JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização.

## Possíveis implicações e riscos {#implications-and-risks}

* A funcionalidade que depende de qualquer componente que use alterações não compatíveis pode ser corrompida e não resolvida corretamente.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade do AEM podem não funcionar corretamente após uma atualização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar o código personalizado e garantir que apenas os componentes compatíveis com o Sling sejam sobrepostos ou referenciados. Entre em contato com o Suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Sobreposições"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Sobrepor ou fazer referência somente a componentes compatíveis com o Sling.
* Considere adaptar os recursos provenientes de `/libs` ou pacotes após uma atualização do AEM.
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) esclarecimentos ou de ter preocupações em conta.
