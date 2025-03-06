---
title: SCR
description: Página de ajuda referente ao código do detector de padrões.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---

# SCR {#scr}

## Fundo {#background}

O SIF identifica o uso do AEM Screens que é incompatível com o AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Possíveis soluções {#solutions}

Encontre as soluções possíveis para os diferentes subtipos abaixo:

* `screens.bundles.detected` - Esses pacotes serão desinstalados durante a atualização.
* `screens.packages.detected` - Esses pacotes serão excluídos durante a atualização.
* `screens.packages.dependency` - Remova qualquer dependência do Screens de seus pacotes personalizados.
* `screens.configs.detected` - Verifique se você não está usando nenhuma propriedade de configuração do Screens em seu código personalizado.
* `screens.users.detected` - Verifique se você não está usando usuários do serviço Screens no código personalizado.
* `screens.paths.detected` - Remova os caminhos do Screens depois de verificar se eles não estão sendo usados no AEM.
* `screens.resource.type.detected` - Remover o uso do tipo de recurso do Screens.
* `screens.usage` - Remova as APIs do Screens de seu código personalizado.