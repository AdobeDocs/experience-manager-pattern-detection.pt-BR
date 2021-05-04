---
title: NBCC
description: Página de ajuda do código do Detector de padrões
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 3%

---

# NBCC {#nbcc}

Alterações compatíveis com versões anteriores

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Alterações compatíveis com versões anteriores"
>abstract="O NBCC identifica a situação em que alguns nós ou pacotes JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Alterações importantes - AEM como um Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR" text="Notas de versão - AEM como um Cloud Service"

`NBCC` identifica a situação em que alguns nós ou pacotes JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização.

## Possíveis implicações e riscos {#implications-and-risks}

* A funcionalidade que depende de qualquer componente que use alterações compatíveis não retroativas pode ser interrompida e pode não ser resolvida corretamente.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade AEM podem não funcionar corretamente após uma atualização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar o código personalizado e garantir que apenas os componentes do Sling compatíveis com versões anteriores sejam sobrepostos ou referenciados. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Sobreposições"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* Sobrepor ou fazer referência somente a componentes Sling compatíveis com versões anteriores.
* Considere adaptar recursos que vêm de `/libs` ou pacotes após uma atualização AEM.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
