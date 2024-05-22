---
title: ASO
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 85%

---

# ASO {#aso}

Visão geral do sistema AEM

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="Visão geral do sistema AEM"
>abstract="O código ASO identifica informações gerais sobre a instância do AEM. Cada descoberta fornece um valor para um tipo específico de informações do sistema que pode ajudar no planejamento da migração e no esforço de refatoração."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Notas de versão do AEM as a Cloud Service"

`ASO` identifica informações gerais sobre a instância do AEM. Cada descoberta fornece um valor de um tipo específico de informação do sistema.

Os subtipos são usados para identificar diferentes tipos de informações:

* `aem.version`: a versão do AEM.
* `aem.product`: detecção do uso de um produto do AEM (Commerce, Forms etc.).
* `node.count`: a contagem aproximada de nós de um determinado tipo (Página, Ativo etc.) e o total geral de nós.
* `node.store`: o tipo de implementação do armazenamento de nós (SegmentNodeStore, DocumentNodeStore) e seu tamanho.
* `data.store`: o tipo de implementação do armazenamento de dados (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: uma tarefa de manutenção.
* `slow.query`: uma consulta lenta.
* `group.membership`: o número de usuários e subgrupos (somente membros diretos/declarados) em um grupo.
* `cqtag.count`: o número de ativos marcados do CQ.
* `smarttag.count`: o número de ativos com tags inteligentes.
* `ccom.version`: a versão do pacote do Componente principal.
* `instance.type`: o tipo de instância AEM (author|publish).
* `unprocessed.asset.count`: o número de ativos não processados.
* `vanity.url.count`: o número de URLs personalizados.
* `index.size`: tamanho total do índice Lucene migrável.
* `workflow.count`: o número de fluxos de trabalho do autor em execução e no estado obsoleto.
* `jvm.arguments`: os argumentos JVM adicionados à linha de comando ao iniciar o AEM.

## Possíveis implicações e riscos {#implications-and-risks}

* A versão do AEM, contagens de nós, associação a grupos, armazenamento de nós, tipos de implementação de armazenamento de dados, contagem de tags CQ, contagem de tags inteligentes, versão do componente principal, tipo de instância do AEM e contagem de ativos não processados são fornecidos para fins informativos.
* O maior número de URLs personalizados (>1000) pode sobrecarregar o Dispatcher e os servidores de publicação com consultas caras.
* O aplicativo personalizado pode depender de produtos ou recursos não disponíveis no AEM as a Cloud Service.
* Atualizar com recursos não compatíveis pode resultar em uma falha de atualização e em um aplicativo não funcional.
* Um alto número de fluxos de trabalho do autor em um estado de execução ou obsoleto pode prejudicar o desempenho.
* Consultas lentas podem prejudicar o desempenho do sistema.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Diretrizes de implementação"
>abstract="As informações expostas por meio do código ASO fornecem informações gerais para o ambiente do AEM, incluindo versões, complementos para produtos e informações no nível do sistema. Verifique se há produtos ou recursos não compatíveis com o AEM as a Cloud Service. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Atualizações do AEM com produtos ou recursos incompatíveis não são recomendadas e podem não contar com suporte.
* Os ativos não processados devem ser `dam:assetState` propriedade no `jcr:content` do ativo deve ser definido como &quot;processado&quot;. Ou remova esses ativos do conjunto de migração antes de migrar para o AEMaaCS.
* URLs personalizados podem ser substituídos por regravações do Apache.
* Consulte a [documentação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/bestpractices/troubleshooting-slow-queries) para solucionar problemas de consultas lentas.
* Confira as [notas de versão](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current) para saber mais sobre as últimas mudanças no AEM as a Cloud Service.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
