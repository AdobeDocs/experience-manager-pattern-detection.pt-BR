---
title: NBCC
description: Página de ajuda do código do Detector de padrões.
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 91%

---

# NBCC {#nbcc}

OBSOLETO: Alterações não compatíveis com versões anteriores (substituídas por NCC, alterações não compatíveis)

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Alterações não compatíveis com versões anteriores"
>abstract="O código NBCC identifica a situação em que alguns nós ou pacotes JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=pt-BR" text="Alterações importantes no AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR" text="Notas de versão - AEM as a Cloud Service"

O código `NBCC` identifica a situação em que alguns nós ou pacotes JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização.

## Possíveis implicações e riscos {#implications-and-risks}

* A funcionalidade que depende de qualquer componente que use alterações compatíveis não retroativas pode ser corrompida e não ser resolvida corretamente.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade do AEM podem não funcionar corretamente após uma atualização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar o código personalizado e garantir que apenas os componentes do Sling compatíveis com versões anteriores sejam sobrepostos ou referenciados. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=pt-BR#platform" text="Sobreposições"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Sobrepor ou fazer referência somente a componentes Sling compatíveis com versões anteriores.
* Considere adaptar os recursos provenientes de `/libs` ou pacotes após uma atualização do AEM.
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) esclarecimentos ou de ter preocupações em conta.
