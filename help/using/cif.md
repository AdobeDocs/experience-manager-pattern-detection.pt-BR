---
title: CIF
description: Página de ajuda do código do Detector de padrões.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 52%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifica a versão clássica de uso do Commerce integration framework que é incompatível com o AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/introduction" text=" Content and Commerce"

CIF identifica a versão clássica de uso de Commerce integration framework AEM que é incompatível com o CIF as a Cloud Service. A mensagem para cada `CIF` a conclusão identifica o uso e fornece informações adicionais.

Os subtipos são usados para identificar os diferentes tipos de informações:

* `commerce.integration.framework.detected`: uma versão clássica da Commerce Integration Framework incompatível com AEM as a Cloud Service.


## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é analisar toda a versão clássica de uso da Commerce Integration Framework."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/changes" text="Alterações importantes na CIF"

* A versão clássica da Commerce Integration Framework não é mais compatível com o AEM as a Cloud Service. Isso bloquearia a atualização para o AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Ferramentas e recursos"
>abstract="Este guia ajuda a identificar as áreas que você deve atualizar para a migração de Experience Manager Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/migration" text="Guia de migração para a CIF"

* Para o Experience Manager as a Cloud Service, o complemento CIF é a única solução de integração comercial compatível para soluções comerciais da Adobe Commerce e de terceiros. O complemento CIF é implantado automaticamente para clientes no Experience Manager as a Cloud Service; não é necessária implantação manual. Consulte [Introdução ao AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/content-and-commerce/storefront/getting-started).
* Para apoiar projetos que implantam o CIF, o Adobe fornece [AEM Componentes principais do CIF](https://github.com/adobe/aem-core-cif-components).
* CIF está disponível para AEM 6.5, bem como através do sistema de gestão de [Portal de distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/br/aem.html). Ele é compatível e fornece os mesmos recursos do complemento CIF para o Experience Manager as a Cloud Service, não sendo necessário fazer ajustes.
* A CIF clássica com suas dependências não está mais disponível. Códigos que dependem dessa versão do CIF usando as APIs do Java™ com.adobe.cq.commerce.api devem ser ajustados para o complemento CIF e seus princípios.
