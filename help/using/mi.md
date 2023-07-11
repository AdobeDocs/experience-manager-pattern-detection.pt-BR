---
title: MI
description: Página de ajuda de códigos do detector de padrões
source-git-commit: aa05ebcb54c6945a903c76add4f31e3279cd05b5
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 30%

---

# MI {#mi}

Problema de configuração incorreta

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Problema de configuração incorreta"
>abstract="O MI identifica problemas de configuração na instância do AEM"

`MI`  O erro de configuração identifica problemas de configuração na instância do AEM.

Os subtipos são usados para identificar os diferentes tipos de informações, como:

* `sling.job.max.parallel`: identifique os trabalhos do sling nos quais a configuração paralela máxima está definida como -1.
* `missing.maintenance.configuration`: Identifique as configurações da tarefa de manutenção ausentes.

## Possíveis implicações e riscos {#implications-and-risks}

* `sling.job.max.parallel`
   * Um valor -1 é substituído pelo número de processadores disponíveis. Isso pode causar problemas de desempenho na instância do AEM.
* `missing.maintenance.configuration`
   * Configurações de tarefa de manutenção ausentes podem causar perda de desempenho ou corrupção de instância.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Diretrizes de implementação"
>abstract="Entre em contato com o Atendimento ao cliente para obter ajuda."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* `sling.job.max.parallel`
   * É aconselhável definir o valor como 0,5 para aproveitar metade dos processadores disponíveis.
* `missing.maintenance.configuration`
   * Limpeza de revisão: consulte [Limpeza de revisão](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html). A parte importante relacionada à configuração está aqui: [Limpeza de revisão - Configurar cauda e compactação completa](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html#how-to-configure-full-and-tail-compaction).
   * Limpeza de binários do Lucene: consulte [Painel de operações - Limpeza de binários do Lucene](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-dashboard.html#lucene-binaries-cleanup).
   * Coleta de lixo do armazenamento de dados: consulte [Coleta de lixo do armazenamento de dados](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/data-store-garbage-collection.html).
   * Limpeza do workflow: consulte [Limpeza regular de instâncias de fluxo de trabalho](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/workflows-administering.html?lang=pt-BR#regular-purging-of-workflow-instances).
   * Tarefa de manutenção do AuditLog: consulte [Manutenção do Log de Auditoria](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-audit-log.html).
* Entre em contato com a [Equipe de Atendimento ao cliente do Experience Manager](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.