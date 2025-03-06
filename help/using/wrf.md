---
title: WRF
description: Página de ajuda referente ao código do detector de padrões.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '90'
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