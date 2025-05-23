---
title: CIF
description: Página de ajuda referente ao código do detector de padrões.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 76%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="A CIF identifica a versão clássica da Commerce Integration Framework que é incompatível com o AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/content-and-commerce/introduction" text=" Content and Commerce"

`CIF` identifica a versão clássica do uso da Commerce Integration Framework que é incompatível com o AEM as a Cloud Service. A mensagem para cada `CIF` encontrado identifica o uso e fornece informações adicionais.

Os subtipos são usados para identificar os diferentes tipos de informação:

* `commerce.integration.framework.detected`: uma versão clássica da Commerce Integration Framework incompatível com AEM as a Cloud Service.


## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é analisar toda a versão clássica de uso da Commerce Integration Framework."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/content-and-commerce/changes" text="Alterações importantes na CIF"

* A versão clássica da Commerce Integration Framework não é mais compatível com o AEM as a Cloud Service. Isso bloquearia a atualização para o AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Ferramentas e recursos"
>abstract="Este guia ajuda a identificar as áreas que necessitam de atualização para a migração do Experience Manager as Cloud Service."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/content-and-commerce/migration" text="Guia de migração para a CIF"

* Para o Experience Manager as a Cloud Service, o complemento da CIF é a única solução de integração comercial compatível para soluções comerciais do Adobe Commerce e de terceiros. O complemento CIF é implantado automaticamente para clientes no Experience Manager as a Cloud Service; não é necessária implantação manual. Consulte [Introdução ao AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/content-and-commerce/storefront/getting-started).
* Para prestar suporte a projetos que implantam a CIF, a Adobe fornece os [Componentes principais da CIF do AEM](https://github.com/adobe/aem-core-cif-components).
* O complemento da CIF está disponível para o AEM 6.5 e por meio do [Portal de distribuição de softwares](https://experience.adobe.com/#/downloads/content/software-distribution/br/aem.html). Ele é compatível e fornece os mesmos recursos do complemento CIF para o Experience Manager as a Cloud Service, não sendo necessário fazer ajustes.
* A CIF clássica com suas dependências não está mais disponível. Códigos que dependem dessa versão da CIF e utilizam as APIs Java™ com.adobe.cq.commerce.api devem ser ajustados para o complemento da CIF e seus princípios.

Além disso, encontre as soluções possíveis para os diferentes subtipos abaixo:

* `commerce.bundles.detected` - Estes pacotes serão desinstalados durante a atualização
* `commerce.packages.detected` - Estes pacotes serão excluídos durante a atualização
* `commerce.packages.dependency` - Remover qualquer dependência do Commerce de pacotes personalizados
* `commerce.nodes.detected` - Atualizar o código personalizado para não criar nós Commerce do CQ
* `commerce.configs.detected` - Não usar as propriedades de configuração do CQ Commerce no código personalizado
* `commerce.users.detected` - Não usar usuários do serviço CQ Commerce no código personalizado
* `commerce.overlays.detected` - Remover o uso de sobreposições do CQ Commerce
* `commerce.paths.detected` - Remova caminhos de comércio depois de verificar se esses caminhos não estão sendo usados no AEM
* `commerce.resource.type.detected` - Remover uso do tipo de recurso de comércio
* `commerce.usage` - Remova as APIs CQ Commerce do código personalizado.
