---
title: DOPI
description: Página de ajuda do código do Detector de padrões.
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 43%

---

# DOPI {#dopi}

Índice de propriedades ordenadas obsoletas

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Índice de propriedades ordenadas obsoletas"
>abstract="O código DOPI identifica o uso de definições de índice de propriedade ordenada (`primaryType=oak:QueryIndexDefinition` E type=&quot;ordered&quot;), que foram descontinuados desde a versão 6.1 e removidos na versão 6.2."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing#the-ordered-index" text="Índice ordenado - Obsoleto"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing" text="Indexação - AEM as a Cloud Service"

DOPI identifica o uso de definições de índice de propriedade ordenada (`primaryType=oak:QueryIndexDefinition` E `type="ordered"`), que foram descontinuados desde a versão 6.1 e removidos na versão 6.2.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar todos os índices ordenados obsoletos e movê-los para a forma de índices Lucene compatíveis para evitar problemas de desempenho significativos ou requisitos não funcionais do cliente."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/practices/best-practices-for-queries-and-indexing" text="Práticas recomendadas - Consultas e indexação"

* Algumas consultas podem não responder.
* A funcionalidade do cliente pode não funcionar corretamente.
* Avisos transversais ou até mesmo erros e sanções significativas de desempenho, pois os índices obsoletos não têm efeito.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Ferramentas e recursos"
>abstract="Revise o projeto herdado WKND para entender como as violações de DOPI podem ser compatíveis com o AEM Cloud Service. Além disso, revise o exemplo de violação de DOPI no GitHub para entender como os índices ordenados herdados podem ser convertidos em índices baseados em Lucene que são compatíveis com o AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Projeto herdado WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Exemplo de violação de DOPI - GitHub"

* Modifique a definição do índice para que ele se torne, ou substitua o índice, uma definição de índice compatível. (Consulte [Consultas e indexação do Oak](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing)).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) e entenda como [Violações de DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) podem ser corrigidas e se tornar compatíveis com o AEM as a Cloud Service.
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) esclarecimentos ou de ter preocupações em conta.
