---
title: ASO
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 4%

---


# ASO {#aso}

Visão geral do sistema AEM

## Segundo plano {#background}

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

* AEM atualizações com produtos ou recursos não suportados não são recomendadas e podem não ser suportadas.
* Revise as [notas de versão](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR) para saber mais sobre as alterações mais recentes no AEM como um Cloud Service.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
