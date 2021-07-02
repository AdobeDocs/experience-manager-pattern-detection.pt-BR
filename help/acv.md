---
title: ACV
description: Página de ajuda do código do Detector de padrões
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a5
source-git-commit: d61fbb28fdf91fd9b356654d5cd2d50b156398c4
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---

# ACV {#acv}

Validador de conteúdo de ativos

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Validador de conteúdo de ativos"
>abstract="O ACV identifica os nós obrigatórios ausentes no conteúdo de ativos."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html" text="Alterações importantes - Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR" text="Experience Manager as a Cloud Service - Notas de versão"

`ACV`  O Validador de conteúdo dos ativos identifica os nós obrigatórios ausentes no conteúdo do ativo. Isso pode levar à falha de determinados recursos do Assets no Experience Manager as a Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de informações, como:

* `assets.sanity.missing.jcrcontent`: Identifique as pastas com nós obrigatórios ausentes no repositório. A identificação de qualquer conteúdo ausente no repositório ajuda a impedir qualquer falha de recursos ou casos de uso.

## Possíveis implicações e riscos {#implications-and-risks}

Isso pode levar à falha de determinados recursos do Assets que dependem das propriedades herdadas no Experience Manager as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Diretrizes de implementação"
>abstract="O Adobe recomenda revisar a estrutura do conteúdo para evitar workflows quebrados que dependem das propriedades herdadas. Entre em contato com o Atendimento ao cliente para obter ajuda."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* Analise uma pasta se ela tiver um nó filho ausente. Crie os nós manualmente se o número de pastas for gerenciável, caso contrário, use um script.
* Entre em contato com a [Experience Manager Customer Care Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
