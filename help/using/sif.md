---
title: SIF
description: Página de ajuda referente ao código do detector de padrões.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 7%

---

# SIF {#sif}

## Fundo {#background}

O SIF identifica o uso do Social que é incompatível com o AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Possíveis soluções {#solutions}

Encontre as soluções possíveis para os diferentes subtipos abaixo:

* `social.bundles.detected` - Estes pacotes serão desinstalados durante a atualização
* `social.packages.detected` - Estes pacotes serão excluídos durante a atualização
* `social.packages.dependency` - Remova a dependência de pacote do social dos pacotes personalizados
* `social.nodes.detected` - Atualizar o código personalizado para não criar nós sociais
* `social.configs.detected` - Não usar propriedades de configuração social no código personalizado
* `social.users.detected` - Não usar usuários sociais no código personalizado
* `social.overlays.detected` - Remover uso de sobreposições sociais
* `social.paths.detected` - Remova os caminhos sociais depois de verificar se esses caminhos não estão sendo usados no AEM
* `social.resource.type.detected` - Remover o uso do tipo de recurso social
* `social.usage` - Remover APIs sociais do código personalizado.