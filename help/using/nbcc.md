---
title: NBCC
description: Página de ajuda referente ao código do detector de padrões.
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 100%

---

# NBCC {#nbcc}

OBSOLETO: Alterações não compatíveis com versões anteriores (substituídas por NCC, alterações não compatíveis)

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Alterações não compatíveis com versões anteriores"
>abstract="O código NBCC identifica a situação em que alguns pacotes ou nós JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. "
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Alterações importantes: AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Notas de versão do AEM as a Cloud Service"

`NBCC` identifica a situação em que alguns pacotes ou nós JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização. 

## Possíveis implicações e riscos {#implications-and-risks}

* Funcionalidades que dependam de componente que usem alterações incompatíveis com versões anteriores podem ficar corrompidas, e podem não ser resolvidas corretamente.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade do AEM podem não funcionar corretamente após uma atualização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar o código personalizado e garantir que apenas os componentes do Sling com retrocompatibilidade estejam sobrepostos ou referenciados. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Sobreposições"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Sobrepor ou referenciar somente componentes com retrocompatibilidade do Sling.
* Considere adaptar os recursos provenientes de `/libs` ou pacotes após uma atualização do AEM.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
