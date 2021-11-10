---
title: CIF
description: Página de ajuda do código do Detector de padrões
source-git-commit: b611b595267e60df8a15511a8a2b4b30b601df1b
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 3%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="A CIF identifica a versão clássica do uso da Commerce Integration Framework que é incompatível com AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html" text=" Conteúdo e comércio"

`CIF` A CIF identifica a versão clássica do uso da Commerce Integration Framework que é incompatível com AEM as a Cloud Service. A mensagem para cada `CIF` A descoberta identificará a utilização e fornecerá informações adicionais.

Os subtipos são usados para identificar os diferentes tipos de informações:

* `commerce.integration.framework.detected`: Uma versão clássica da Commerce Integration Framework incompatível com AEM as a Cloud Service.


## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Diretrizes de implementação"
>abstract="A Prática recomendada é analisar toda a versão clássica do uso da Estrutura de integração do comércio."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html" text="Alterações importantes na CIF"

* A versão clássica da Commerce Integration Framework não é mais suportada AEM as a Cloud Service. Isso bloquearia a atualização para AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Ferramentas e recursos"
>abstract="Este guia ajuda a identificar as áreas que você precisa atualizar para a migração do Experience Manager Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html" text="Guia de migração para a CIF"

* Para o Experience Manager as a Cloud Service, o complemento CIF é a única solução de integração comercial compatível para soluções comerciais Adobe Commerce e de terceiros. O complemento CIF é implantado automaticamente para clientes no Experience Manager as a Cloud Service, não é necessária implantação manual. Consulte [Introdução ao AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html).
* Para dar suporte a projetos que implantam o Adobe da CIF [Componentes principais da CIF do AEM](https://github.com/adobe/aem-core-cif-components).
* O complemento CIF está disponível para o AEM 6.5 e por meio do [Portal de distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/br/aem.html). Ele é compatível e fornece os mesmos recursos do complemento CIF para o Experience Manager as a Cloud Service, não sendo necessário fazer ajustes.
* A CIF clássica com suas dependências não está mais disponível. O código que depende dessa versão da CIF usando as APIs do Java com.adobe.cq.commerce.api deve ser ajustado para o complemento CIF e seus princípios.
