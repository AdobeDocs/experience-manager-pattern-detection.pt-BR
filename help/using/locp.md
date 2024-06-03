---
title: LOCP
description: Página de ajuda referente ao código do detector de padrões.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 100%

---

# LOCP {#locp}

/libs Substituição de pacotes personalizados

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Substituição de pacotes personalizados"
>abstract="O LOCP identifica a detecção de um pacote personalizado que fornece conteúdo a `/libs`, que é um antipadrão (exceto se houver ACLs)."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Atualizações sustentáveis"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sling Resource Merger"

`LOCP` identifica a detecção de um pacote personalizado que entrega conteúdo a `/libs`, que é um antipadrão (exceto no caso de ACLs).

## Possíveis implicações e riscos {#implications-and-risks}

* O código do cliente pode ser excluído ou substituído ao atualizar o pacote de correções cumulativo, o pacote de serviço ou em qualquer outra atualização importante do AEM.
* Em alguns casos, o novo conteúdo pode não ser instalado corretamente.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Diretrizes de implementação"
>abstract="Clientes devem verificar seu código e seus pacotes personalizados para identificar se o conteúdo é entregue a `/libs`. Se necessário, refatore-o para depender da sobreposição de conteúdo em /apps e torná-lo compatível com o AEM as a Cloud Service. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sobreposições"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Os pacotes do cliente devem implantar conteúdo em `/apps` em vez de `/libs`.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
