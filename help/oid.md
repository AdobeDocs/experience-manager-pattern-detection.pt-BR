---
title: OID
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---


# OID {#oid}

Definição de Índice Oak

## Segundo plano {#background}

`OID` identifica problemas relacionados às definições do índice Oak. Ele identifica modificações que foram feitas nas definições padrão do índice Oak. Também identifica definições de índice Oak personalizadas que são incompatíveis com AEM como um Cloud Service. A mensagem para cada descoberta `OID` identificará o índice e fornecerá informações adicionais.

Os subtipos são usados para identificar os diferentes tipos de informações:

* `custom.index.violation`: Uma incompatibilidade de índice Oak personalizado com AEM como um Cloud Service.
* `standard.index.modification`: Uma modificação em um índice Oak padrão.

## Possíveis implicações e riscos {#implications-and-risks}

* As modificações nas definições de índice Oak padrão podem ser perdidas durante uma atualização de AEM.
* As definições do Oak são imutáveis, devem ser empacotadas com o código do projeto do cliente e só devem ser implantadas usando o Cloud Manager.
* Todas as definições de índice Oak devem seguir a convenção de nomenclatura e outras regras para os índices Oak em AEM como Cloud Service. Aquelas que não causarem comportamento indesejado.

## Possíveis soluções {#solutions}

* Resolva as violações da regra de índice identificadas na mensagem.
* Siga AEM como Cloud Service [diretrizes de empacotamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) para implantar definições de índice Oak novas ou personalizadas.
* Os índices personalizados AEM padrão e as novas definições personalizadas de índice Oak devem seguir as [diretrizes de indexação de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition) para AEM como Cloud Service.
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) e entenda como [as violações de OID](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) podem ser corrigidas e tornadas compatíveis com AEM como um Cloud Service.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
* Utilize o [Index Converter](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools) para migrar as Definições de Índice Oak Personalizado existentes para AEM como Definições de Índice Oak Personalizado compatíveis com Cloud Service.
