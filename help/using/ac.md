---
title: AC
description: Página de ajuda referente ao código do detector de padrões.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
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