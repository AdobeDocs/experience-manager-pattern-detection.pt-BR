---
title: ASO
description: Página de ajuda do código do Detector de padrões
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: d45c6b561a9665cbac39bfd8d9ce6eb2658c24e8
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 4%

---

# ASO {#aso}

Visão geral do sistema AEM

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="Visão geral do sistema AEM"
>abstract="O código ASO identifica informações gerais sobre a instância do AEM. Cada descoberta fornece um valor para um tipo específico de informações do sistema que pode ajudar no planejamento da migração e no esforço de refatoração."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service - Notas de versão"

`ASO` O identifica informações gerais sobre a instância do AEM. Cada descoberta fornece um valor de um tipo específico de informação do sistema.

Os subtipos são usados para identificar diferentes tipos de informações:

* `aem.version`: A versão AEM.
* `aem.product`: Detecção do uso de um produto AEM (Comércio, Forms etc.).
* `node.count`: A contagem aproximada de nós de um determinado tipo (Página, Ativo etc.) e o total geral de nós.
* `node.store`: O tipo de implementação do armazenamento de nós (SegmentNodeStore, DocumentNodeStore) e seu tamanho.
* `data.store`: O tipo de implementação do armazenamento de dados (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Uma tarefa de manutenção.
* `slow.query`: Uma consulta lenta.
* `group.membership`: O número de usuários e subgrupos (somente membros diretos/declarados ) em um grupo.
* `cqtag.count`: O número de ativos marcados do CQ.
* `smarttag.count`: O número de ativos com tags inteligentes.
* `ccom.version`: A versão do pacote do Componente principal.
* `instance.type`: O tipo de instância AEM (author|publish).

## Possíveis implicações e riscos {#implications-and-risks}

* A versão de AEM, contagens de nó, associação de grupo, armazenamento de nó, tipos de implementação de armazenamento de dados, Contagem de tag CQ, Contagem de tag inteligente, versão do Componente principal e AEM tipo de instância são fornecidas para fins informativos.
* O aplicativo personalizado pode depender de produtos ou recursos não disponíveis AEM as a Cloud Service.
* Atualizar com recursos não suportados pode resultar em uma falha de atualização e em um aplicativo não funcional.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Diretrizes de implementação"
>abstract="As informações expostas por meio do código ASO fornecem informações gerais para seu ambiente AEM, incluindo versões, complementos de produtos, informações de nível de sistema e devem ser revisadas para todos os produtos ou recursos não suportados AEM as a Cloud Service. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* AEM atualizações com produtos ou recursos não suportados não são recomendadas e podem não ser suportadas.
* Revise o [notas de versão](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR) para saber mais sobre as últimas mudanças no AEM as a Cloud Service.
* Entre em contato com a [Equipe de suporte AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou dar resposta a preocupações.
