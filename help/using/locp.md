---
title: LOCP
description: Página de ajuda de códigos do detector de padrões
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 100%

---

# LOCP {#locp}

/libs Substituição de pacotes personalizados

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Substituição de pacotes personalizados"
>abstract="O código LOCP identifica a detecção de um pacote personalizado que fornece conteúdo para /libs, que é um antipadrão (exceto no caso de ACLs)."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=pt-BR" text="Atualizações sustentáveis"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=pt-BR#platform" text="Fusão de recursos do Sling"

O código `LOCP` identifica a detecção de um pacote personalizado que entrega conteúdo para `/libs`, que é um antipadrão (exceto no caso de ACLs).

## Possíveis implicações e riscos {#implications-and-risks}

* O código do cliente pode ser excluído ou substituído para qualquer atualização importante do AEM, CFP ou SP.
* Em alguns casos, o novo conteúdo pode não ser instalado corretamente.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Diretrizes de implementação"
>abstract="Os clientes devem revisar seu código personalizado e pacotes para identificar se o conteúdo é entregue a /libs e refatorar para depender da sobreposição do conteúdo em /apps e torná-lo compatível com o AEM as a Cloud Service. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=pt-BR#platform" text="Sobreposições"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Os pacotes do cliente devem implantar conteúdo em `/apps` em vez de `/libs`.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
