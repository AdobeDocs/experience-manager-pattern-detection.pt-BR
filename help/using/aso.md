---
title: ASO
description: Página de ajuda de códigos do detector de padrões
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: a899311c975efee180bc1d3bc3c7bca30d429a22
workflow-type: ht
source-wordcount: '472'
ht-degree: 100%

---

# ASO {#aso}

Visão geral do sistema AEM

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="Visão geral do sistema AEM"
>abstract="O código ASO identifica informações gerais sobre a instância do AEM. Cada descoberta fornece um valor para um tipo específico de informações do sistema que pode ajudar no planejamento da migração e no esforço de refatoração."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR" text="O AEM as a Cloud Service - notas de versão"

O código `ASO` identifica informações gerais sobre a instância do AEM. Cada descoberta fornece um valor de um tipo específico de informação do sistema.

Os subtipos são usados para identificar diferentes tipos de informações:

* `aem.version`: a versão do AEM.
* `aem.product`: detecção do uso de um produto AEM (Commerce, Forms etc.).
* `node.count`: a contagem aproximada de nós de um determinado tipo (Página, Ativo, etc.) e o total geral de nós.
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

* A versão do AEM, contagens de nós, associação ao grupo, armazenamento de nós, tipos de implementação de armazenamento de dados, contagem de tags CQ, contagem de tags inteligentes, versão do componente principal, tipo de instância do AEM e contagem de ativos não processados são fornecidos para fins informativos.
* O maior número de URLs personalizados (>1000) pode sobrecarregar o Dispatcher e os servidores de publicação com consultas caras.
* O aplicativo personalizado pode depender de produtos ou recursos não disponíveis no AEM as a Cloud Service.
* Atualizar com recursos não compatíveis pode resultar em uma falha de atualização e em um aplicativo não funcional.
* Um alto número de fluxos de trabalho do autor em execução ou em estado obsoleto pode degradar o desempenho.
* Consultas lentas podem prejudicar o desempenho do sistema.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Diretrizes de implementação"
>abstract="As informações expostas por meio do código ASO fornecem informações gerais para seu ambiente AEM, incluindo versões, complementos de produtos, informações de nível de sistema e devem ser revisadas para todos os produtos ou recursos não compatíveis com o AEM as a Cloud Service. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Atualizações do AEM com produtos ou recursos não compatíveis não são recomendadas e podem não ter suporte.
* Os ativos não processados devem ser processados e a propriedade dam:assetState no nó jcr:content do ativo deve ser definida como “processado” ou remover esses ativos do conjunto de migração antes de migrar para o AEMaaCS.
* URLs personalizados podem ser substituídos por regravações do Apache.
* Consulte a [documentação](https://experienceleague.adobe.com/docs/experience-manager-65/developing/bestpractices/troubleshooting-slow-queries.html?lang=pt-BR) para solucionar problemas de consultas lentas.
* Revise as [notas de versão](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR) para saber mais sobre as últimas mudanças no AEM as a Cloud Service.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
