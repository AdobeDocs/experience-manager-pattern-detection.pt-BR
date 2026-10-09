---
title: AC
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 4c6ac075-5ba6-4511-97c6-a9b496d4677a
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
# AC {#ac}

## Fundo {#background}

O código AC identifica o uso de pacotes do Assets que é incompatível com o AEM 6.5 LTS

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Possíveis soluções {#solutions}

Encontre as soluções possíveis para os diferentes subtipos abaixo:

* `asset.bundles.detected` - Este pacote será desinstalado durante a atualização.
* `asset.usage` - Remover qualquer classificação de ativo e dependências de componentes do catálogo de ativos do código personalizado. Quando aplicável, altere o código para usar a nova API `List<Scene7ConfigSetting>` `com.day.cq.dam.scene7.api.model.Scene7ViewerConfig#getSettingsList()`.
* `asset.overlays.detected` - As sobreposições criadas nos componentes de Classificação e Catálogo do Assets precisam ser removidas.
* `asset.resource.type.detected` - Remova qualquer uso do tipo de recurso do componente de classificação do Assets em seu código personalizado.
* `asset.paths.detected` - Mova qualquer conteúdo do cliente presente nesses caminhos e remova esses caminhos depois de verificar se eles não estão sendo usados no AEM.

