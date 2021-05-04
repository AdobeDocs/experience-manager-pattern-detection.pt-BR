---
title: LOCAL
description: Página de ajuda do código do Detector de padrões
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# LOCAL {#locp}

/libs Substituição de pacotes personalizados

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Substituição de pacotes personalizados"
>abstract="O LOCP identifica a detecção de um pacote personalizado que fornece conteúdo para /libs, que é um antipadrão (exceto no caso de ACLs)."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html" text="Atualizações sustentáveis"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html#platform" text="Fusão de Recursos Sling"

`LOCP` identifica a detecção de um pacote personalizado que fornece conteúdo para o  `/libs`, que é um antipadrão (exceto no caso de ACLs).

## Possíveis implicações e riscos {#implications-and-risks}

* O código do cliente pode ser excluído ou substituído para qualquer atualização de CFP, SP ou AEM principal.
* Em alguns casos, o novo conteúdo pode não estar instalado corretamente.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Diretrizes de implementação"
>abstract="Os clientes devem revisar seu código personalizado e pacotes para identificar se o conteúdo é entregue a /libs e refatorar para depender da sobreposição do conteúdo em /apps e torná-lo compatível com o AEM como um Cloud Service. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Sobreposições"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* Os pacotes do cliente devem implantar conteúdo em `/apps` em vez de `/libs`.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
