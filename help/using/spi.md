---
title: SPI
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 39f2d04e-c6e4-4da6-b000-0115bc2b87bf
source-git-commit: 29d702c9662fd185ef806123fc4f4a03a70d64aa
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 8%
---
# SPI {#spi}

## Histórico {#background}

O código SIF identifica o uso do Search and Promote incompatível com o AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Possíveis soluções {#solutions}

Encontre as soluções possíveis para os diferentes subtipos abaixo:

* `searchpromote.bundles.detected` - Esses pacotes serão desinstalados durante a atualização
* `earchpromote.packages.detected` - Estes pacotes serão excluídos durante a atualização
* `searchpromote.packages.dependency` - Remova qualquer dependência do Search&amp;Promote que seus pacotes personalizados possam ter
* `searchpromote.usage` - Remover APIs do Search&amp;Promote de seu código personalizado
* `searchpromote.users.detected` - Não usar os usuários do serviço Search&amp;Promote no código personalizado
* `searchpromote.configs.detected` - Não use as propriedades de configuração do Search&amp;Promote em seu código personalizado.
