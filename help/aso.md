---
title: ASO
description: Página de ajuda do código do Detector de padrões
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
translation-type: tm+mt
source-git-commit: 449288e567adda9998a89e0ad5198fd5a4e93f35
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 5%

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
* `node.count`: A contagem aproximada de nós de um determinado tipo (Página, Ativo, etc.).
* `node.store`: O tipo de implementação do armazenamento de nós (SegmentNodeStore, DocumentNodeStore).
* `data.store`: O tipo de implementação do armazenamento de dados (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Uma tarefa de manutenção.
* `slow.query`: Uma consulta lenta.

## Possíveis implicações e riscos {#implications-and-risks}

* A versão de AEM, as contagens de nós e os tipos de implementação de armazenamento e armazenamento de dados são fornecidos para fins informativos.
* O aplicativo personalizado pode depender de produtos ou recursos não disponíveis no AEM como um Cloud Service.
* Atualizar com recursos não suportados pode resultar em uma falha de atualização e em um aplicativo não funcional.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Diretrizes de implementação"
>abstract="As informações expostas por meio do código ASO fornecem informações gerais para seu ambiente AEM, incluindo versões, complementos de produtos, informações de nível de sistema, e isso deve ser revisado para todos os produtos ou recursos não suportados no AEM as a Cloud Service. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* AEM atualizações com produtos ou recursos não suportados não são recomendadas e podem não ser suportadas.
* Revise as [notas de versão](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR) para saber mais sobre as alterações mais recentes no AEM como um Cloud Service.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
