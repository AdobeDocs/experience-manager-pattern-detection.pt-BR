---
title: DOPI
description: Página de ajuda de códigos do detector de padrões
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: ht
source-wordcount: '305'
ht-degree: 100%

---

# DOPI {#dopi}

Índice de propriedades ordenadas obsoletas

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Índice de propriedades ordenadas obsoletas"
>abstract="O código DOPI identifica o uso de definições de índice de propriedade ordenada (primaryType=oak:QueryIndexDefinition AND type=&quot;ordered&quot;), que foram descontinuadas desde a versão 6.1 e removidas na versão 6.2."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=pt-BR#the-ordered-index" text="Índice ordenado - Obsoleto"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=pt-BR" text="Indexação - AEM as a Cloud Service"

O código `DOPI` identifica o uso de definições de índice de propriedade ordenada (`primaryType=oak:QueryIndexDefinition` E `type="ordered"`), que foram descontinuadas desde a versão 6.1 e removidas na versão 6.2.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar todos os índices ordenados obsoletos e movê-los para a forma de índices Lucene compatíveis para evitar problemas de desempenho significativos ou necessidades não funcionais do cliente."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/practices/best-practices-for-queries-and-indexing.html?lang=pt-BR" text="Práticas recomendadas - Consultas e indexação"

* Algumas consultas podem não responder.
* A funcionalidade do cliente pode não funcionar corretamente.
* Avisos transversais ou até mesmo erros e sanções significativas de desempenho, pois os índices obsoletos não têm efeito.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Ferramentas e recursos"
>abstract="Revise o projeto herdado WKND para entender como as violações de DOPI podem ser compatíveis com o AEM Cloud Service. Além disso, revise o exemplo de violação do DOPI no Github para entender como os índices ordenados herdados podem ser convertidos em índices baseados em Lucene, compatíveis com o AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Projeto herdado WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Exemplo de violação de DOPI - Github"

* Modifique a definição do índice para torná-lo, ou substituir o índice por, uma definição de índice compatível. (Consulte [Consultas e indexação do Oak](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=pt-BR)).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) e entenda como [Violações de DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) podem ser corrigidas e se tornar compatíveis com o AEM as a Cloud Service.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
