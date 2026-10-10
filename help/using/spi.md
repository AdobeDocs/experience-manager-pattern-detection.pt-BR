---
title: SPI
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 39f2d04e-c6e4-4da6-b000-0115bc2b87bf
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
# SPI {#spi}

## Fundo {#background}

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
