---
title: OID
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: ht
source-wordcount: '418'
ht-degree: 100%

---

# OID {#oid}

Definição de índice Oak

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Definição de índice Oak"
>abstract="O código OID identifica problemas relacionados às definições do índice Oak. Ele identifica modificações que foram feitas nas definições padrão do índice Oak. Também identifica definições de índice Oak personalizadas incompatíveis com o AEM as a Cloud Service. A mensagem para cada OID encontrado identifica o índice e fornece informações adicionais."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/operations/indexing#how-to-use" text="Diretrizes de indexação de conteúdo"

`OID` identifica problemas relacionados às definições do índice Oak. Ele identifica modificações que foram feitas nas definições padrão do índice Oak. Também identifica definições de índice Oak personalizadas incompatíveis com o AEM as a Cloud Service. A mensagem para cada `OID` encontrado identifica o índice e fornece informações adicionais.

Os subtipos são usados para identificar os diferentes tipos de informação:

* `index.rule.violation`: uma incompatibilidade do índice Oak personalizado com o AEM as a Cloud Service
* `standard.index.modification`: uma modificação em um índice Oak padrão.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar todos os índices personalizados e reestruturá-los de acordo com as diretrizes de indexação de conteúdo. Use o conversor de índice para migrar as definições do índice Oak personalizado para uma definição compatível do AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#oak-indexes" text="Diretrizes de empacotamento"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools" text="Conversor de índice"

* As modificações nas definições de índice Oak padrão podem ser perdidas durante uma atualização do AEM.
* As definições do Oak são imutáveis, devem ser empacotadas com o código do projeto do cliente e só devem ser implantadas usando o Cloud Manager.
* Todas as definições do índice Oak devem seguir a convenção de nomenclatura e outras regras referentes aos índices Oak no AEM as a Cloud Service. Caso contrário, pode ocorrer um comportamento indesejado.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Ferramentas e recursos"
>abstract="Revise o projeto WKND herdado para entender como as violações de OID podem ser resolvidas em seu projeto. Além disso, confira o exemplo de violação do OID no GitHub. Ele pode ajudar a entender como converter índices herdados por meio da ferramenta “Conversor de índices”, para que sejam compatíveis com o AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="Projeto herdado WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Exemplo de violação do OID: Github"

* Resolva as violações da regra de índice identificadas na mensagem.
* Para implantar definições do índice Oak novas ou personalizadas, siga as [diretrizes para pacotes](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) do AEM as a Cloud Service.
* Os índices padrão personalizados do AEM e as novas definições do índice Oak personalizadas devem seguir as [diretrizes de indexação de conteúdo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/operations/indexing#preparing-the-new-index-definition) do AEM as a Cloud Service.
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) e entenda como as [violações de OID](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) podem ser corrigidas para se tornarem compatíveis com o AEM as a Cloud Service.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
* Use o [Conversor de índices](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools) para migrar definições personalizadas do índice Oak, transformando-as em definições compatíveis com o AEM as a Cloud Service.
