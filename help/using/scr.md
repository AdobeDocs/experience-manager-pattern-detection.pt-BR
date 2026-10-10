---
title: SCR
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 13b14cc2-f70b-45ff-a62d-dee647311d84
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
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
