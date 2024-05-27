---
title: DOPI
description: Página de ajuda referente ao código do detector de padrões.
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: ht
source-wordcount: '254'
ht-degree: 100%

---

# DOPI {#dopi}

Índice de propriedades ordenadas obsoletas

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Índice de propriedades ordenadas obsoletas"
>abstract="O código DOPI identifica o uso de definições de índice de propriedade ordenada (`primaryType=oak:QueryIndexDefinition` AND `type="ordered"`). A definição se tornou obsoleta no AEM 6.1 e foi removida no AEM 6.2."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing#the-ordered-index" text="Índice ordenado - Obsoleto"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/operations/indexing" text="Indexação - AEM as a Cloud Service"

O `DOPI` identifica o uso de definições de índice de propriedade ordenada (`primaryType=oak:QueryIndexDefinition` AND `type="ordered"`). As definições se tornaram obsoletas no AEM 6.1 e foram removidas no AEM 6.2.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar todos os índices ordenados obsoletos e convertê-los em índices Lucene compatíveis para evitar problemas de desempenho significativos ou requisitos de cliente não funcionais."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/deploying/practices/best-practices-for-queries-and-indexing" text="Práticas recomendadas - Consultas e indexação"

* Algumas consultas podem não responder.
* A funcionalidade do cliente pode não funcionar corretamente.
* Avisos transversais ou até mesmo erros e sanções significativas de desempenho, pois os índices obsoletos não têm efeito.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Ferramentas e recursos"
>abstract="Revise o projeto WKND herdado para entender como as violações de DOPI podem ficar compatíveis com o AEM Cloud Service. Além disso, confira o exemplo de violação do DOPI no GitHub. Ele pode ajudar a entender como converter índices ordenados herdados em índices baseados em Lucene, que são compatíveis com o AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Projeto herdado WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Exemplo de violação de DOPI no Github"

* Edite a definição de índice para convertê-la em (ou para substituir o índice por) uma definição de índice compatível. (Consulte [Consultas e indexação do Oak](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing)).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) e entenda como [Violações de DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) podem ser corrigidas e se tornar compatíveis com o AEM as a Cloud Service.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
