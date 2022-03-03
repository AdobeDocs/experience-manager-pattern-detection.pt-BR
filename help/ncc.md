---
title: NCC
description: Página de ajuda de códigos do detector de padrões
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
source-git-commit: 8b8d902dc5b5a8534475d256c199dc235bb35464
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# NCC {#ncc}

Alterações não compatíveis

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Alterações não compatíveis"
>abstract="O código NCC identifica a situação em que alguns nós ou pacotes JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=pt-BR" text="Alterações importantes no AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR" text="Notas de versão - AEM as a Cloud Service"

O código `NCC` identifica a situação em que alguns nós ou pacotes JCR são alterados de forma não compatível. O cliente pode não estar ciente dessa alteração antes de uma atualização.

## Possíveis implicações e riscos {#implications-and-risks}

* A funcionalidade que depende de qualquer componente que use alterações não compatíveis pode ser corrompida e não resolvida corretamente.
* Alguns recursos do aplicativo do cliente ou alguma funcionalidade do AEM podem não funcionar corretamente após uma atualização.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar o código personalizado e garantir que apenas os componentes compatíveis com o Sling sejam sobrepostos ou referenciados. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=pt-BR#platform" text="Sobreposições"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Sobrepor ou fazer referência somente a componentes compatíveis com o Sling.
* Considere adaptar os recursos provenientes de `/libs` ou pacotes após uma atualização do AEM.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
