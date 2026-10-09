---
title: WRF
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 36578498-d5b2-46d1-a274-a1646ceaa764
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 8%
---
# WRF {#wrf}

## Fundo {#background}

O WRF identifica o uso de we-retail que é incompatível com o AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Possíveis soluções {#solutions}

Encontre as soluções possíveis para os diferentes subtipos abaixo:

* `weretail.bundles.detected` - Estes pacotes serão desinstalados durante a atualização
* `weretail.packages.detected` - Estes pacotes serão excluídos durante a atualização
* `weretail.configs.detected` - Não use as propriedades de configuração do We.Retail em seu código personalizado
* `weretail.packages.dependency` - Remover a dependência de qualquer pacote personalizado no We.Retail
* `weretail.paths.detected` - Esses caminhos do We.Retail podem ser excluídos depois de se certificar de que você não está usando o social
* `weretail.resource.type.detected` - Remover o uso do tipo de recurso We.Retail
* `weretail.usage` - Remova as APIs We.Retail de seu código personalizado.
