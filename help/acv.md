---
title: ACV
description: Página de ajuda do código do Detector de padrões
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a5
source-git-commit: 57e33b97aba253bad62cf95dcca9ef6885d263e6
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# ACV {#acv}

Validador de conteúdo de ativos

## Segundo plano {#background}

>[!INFO]
>id=&quot;aemcloud_bpa_acv_overview&quot;
>title=&quot;Validador de conteúdo de ativos&quot;
>abstract=&quot;ACV identifica os nós obrigatórios ausentes no conteúdo de ativos.&quot;
>additional-url=&quot;https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html&quot; text=&quot;Alterações importantes - Experience Manager como Cloud Service&quot;
>additional-url=&quot;https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html&quot; text=&quot;Experience Manager as a Cloud Service - Notas de versão&quot;

`ACV`  O Validador de conteúdo dos ativos identifica os nós obrigatórios ausentes no conteúdo do ativo. Isso pode levar à falha de determinados recursos do Assets no Experience Manager as a Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de informações, como:

* `assets.sanity.missing.jcrcontent`: Identifique as pastas com nós obrigatórios ausentes no repositório. A identificação de qualquer conteúdo ausente no repositório ajuda a impedir qualquer falha de recursos ou casos de uso.

## Possíveis implicações e riscos {#implications-and-risks}

Isso pode levar à falha de determinados recursos do Assets que dependem das propriedades herdadas no Experience Manager as a Cloud Service.

## Possíveis soluções {#solutions}

>[!INFO]
>id=&quot;aemcloud_bpa_acv_guide&quot;
>title=&quot;Diretrizes de implementação&quot;
>abstract=&quot;O Adobe recomenda a revisão da estrutura de conteúdo para evitar workflows quebrados que dependem das propriedades herdadas. Entre em contato com o Atendimento ao cliente para obter ajuda&quot;.
>additional-url=&quot;https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html&quot; text=&quot;Experience Cloud Support&quot;

* Analise uma pasta se ela tiver um nó filho ausente. Crie os nós manualmente se o número de pastas for gerenciável, caso contrário, use um script.
* Entre em contato com a [Experience Manager Customer Care Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
