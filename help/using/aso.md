---
title: ASO
description: Página de ajuda de códigos do detector de padrões.
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 67%

---

# ASO {#aso}

Visão geral do sistema AEM

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="Visão geral do sistema AEM"
>abstract="O código ASO identifica informações gerais sobre a instância do AEM. Cada descoberta fornece um valor para um tipo específico de informações do sistema que pode ajudar no planejamento da migração e no esforço de refatoração."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Notas de versão do AEM as a Cloud Service"

`ASO` Identifica informações gerais sobre a instância do AEM. Cada descoberta fornece um valor de um tipo específico de informação do sistema.

Os subtipos são usados para identificar diferentes tipos de informações:

* `aem.version`: a versão do AEM.
* `aem.product`: detecção do uso de um produto AEM (Commerce, Forms e assim por diante).
* `node.count`: a contagem aproximada de nós de um determinado tipo (Página, Ativo e assim por diante) e o total geral de nós.
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

* A versão do AEM, contagens de nó, associação de grupo, armazenamento de nó, tipos de implementação de armazenamento de dados, Contagem de tag CQ, Contagem de tag inteligente, versão do Componente principal, tipo de instância do AEM e contagem de ativos não processados são fornecidas para fins informativos.
* O maior número de URLs personalizados (>1000) pode sobrecarregar o Dispatcher e os servidores de publicação com consultas caras.
* O aplicativo personalizado pode depender de produtos ou recursos não disponíveis no AEM as a Cloud Service.
* Atualizar com recursos não compatíveis pode resultar em uma falha de atualização e em um aplicativo não funcional.
* Um alto número de fluxos de trabalho do autor em execução ou em estado obsoleto pode degradar o desempenho.
* Consultas lentas podem prejudicar o desempenho do sistema.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Diretrizes de implementação"
>abstract="As informações expostas por meio do código ASO fornecem informações gerais para o ambiente do AEM, incluindo versões, complementos para produtos e informações no nível do sistema. Verifique se há produtos ou recursos não compatíveis com o AEM as a Cloud Service. Entre em contato com o Suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html?lang=pt-BR" text="Suporte da Experience Cloud"

* Atualizações de AEM com produtos ou recursos não compatíveis não são recomendadas e podem não ser compatíveis.
* Os ativos não processados devem ser `dam:assetState` propriedade no `jcr:content` do ativo deve ser definido como &quot;processado&quot;. Ou remova esses ativos do conjunto de migração antes de migrar para o AEMaaCS.
* URLs personalizados podem ser substituídos por regravações do Apache.
* Consulte a [documentação](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/bestpractices/troubleshooting-slow-queries) para solucionar problemas de consultas lentas.
* Consulte a [notas de versão](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current) se você quiser saber mais sobre as últimas mudanças no AEM as a Cloud Service.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
