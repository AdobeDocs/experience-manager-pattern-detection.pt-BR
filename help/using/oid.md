---
title: OID
description: Página de ajuda de códigos do detector de padrões
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: d3e518cf8ad53a2cd28d4eea7f9b75c672881507
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 100%

---

# OID {#oid}

Definição de índice Oak

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Definição de índice Oak"
>abstract="O código OID identifica problemas relacionados às definições do índice Oak. Ele identifica modificações que foram feitas nas definições padrão do índice Oak. Também identifica definições de índice Oak personalizadas incompatíveis com o AEM as a Cloud Service. A mensagem para cada OID encontrado identificará o índice e fornecerá informações adicionais."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=pt-BR#how-to-use" text="Diretrizes de indexação de conteúdo"

O código `OID` identifica problemas relacionados às definições do índice Oak. Ele identifica modificações que foram feitas nas definições padrão do índice Oak. Também identifica definições de índice Oak personalizadas incompatíveis com o AEM as a Cloud Service. A mensagem para cada `OID` encontrado identificará o índice e fornecerá informações adicionais.

Os subtipos são usados para identificar os diferentes tipos de informações:

* `index.rule.violation`: uma incompatibilidade do índice Oak personalizado com o AEM as a Cloud Service
* `standard.index.modification`: uma modificação em um índice Oak padrão.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar todos os índices personalizados e reestruturados de acordo com as diretrizes de indexação de conteúdo. Use o conversor de índice para migrar as definições de índice Oak personalizado existentes para a definição de índice Oak personalizado compatível do AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=pt-BR#oak-indexes" text="Diretrizes de empacotamento"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html?lang=pt-BR#refactoring-tools" text="Conversor de índice"

* As modificações nas definições de índice Oak padrão podem ser perdidas durante uma atualização do AEM.
* As definições do Oak são imutáveis, devem ser empacotadas com o código do projeto do cliente e só devem ser implantadas usando o Cloud Manager.
* Todas as definições de índice Oak devem seguir a convenção de nomenclatura e outras regras para os índices Oak no AEM as a Cloud Service. Aquelas que não possam causar comportamento indesejado.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Ferramentas e recursos"
>abstract="Revise o projeto herdado WKND para entender como as violações de OID podem ser resolvidas em seu projeto. Além disso, revise o exemplo de violação de OID no Github para entender como os índices herdados podem ser convertidos usando a ferramenta Conversor de índice para se tornarem compatíveis com o AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="Projeto herdado WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Exemplo de violação de OID - Github"

* Resolva as violações da regra de índice identificadas na mensagem.
* Siga as [diretrizes de empacotamento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=pt-BR) do AEM as a Cloud Service para implantar definições de índice Oak novas ou personalizadas.
* Os índices padrão do AEM personalizados e as novas definições de índice Oak personalizadas devem seguir as [diretrizes de indexação de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=pt-BR#preparing-the-new-index-definition) para o AEM as a Cloud Service.
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) e entenda como as [violações de OID](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) podem ser corrigidas para se tornarem compatíveis com o AEM as a Cloud Service.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
* Use o [Conversor de índice](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html?lang=pt-BR#refactoring-tools) para migrar as definições de índice Oak personalizadas existentes para as definições de índice Oak personalizadas compatíveis com o AEM as a Cloud Service.
