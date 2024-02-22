---
title: MI
description: Página de ajuda de códigos do detector de padrões
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: efb06dc7e00f91d4c080553df3153deb90b093f2
workflow-type: ht
source-wordcount: '210'
ht-degree: 100%

---

# MI {#mi}

Problema de configuração incorreta

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Problema de configuração incorreta"
>abstract="O MI identifica problemas de configuração na instância do AEM"

`MI` O problema de configuração incorreta identifica problemas de configuração na instância do AEM.

Os subtipos são usados para identificar os diferentes tipos de informações, como:

* `sling.job.max.parallel`: identifique os processos do Sling nos quais a configuração paralela máxima está definida como -1.
* `missing.maintenance.configuration`: identifique as configurações da tarefa de manutenção ausentes.

## Possíveis implicações e riscos {#implications-and-risks}

* `sling.job.max.parallel`
   * Um valor de -1 é substituído pelo número de processadores disponíveis. Isso pode causar problemas de desempenho na instância do AEM.
* `missing.maintenance.configuration`
   * Configurações de tarefa de manutenção ausentes podem causar queda de desempenho ou corrupção da instância.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Diretrizes de implementação"
>abstract="Entre em contato com o Atendimento ao cliente para obter ajuda."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* `sling.job.max.parallel`
   * É aconselhável definir o valor como 0,5 para utilizar apenas metade dos processadores disponíveis.
* `missing.maintenance.configuration`
   * Limpeza de revisão: consulte a [Limpeza de revisão](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=pt-BR). A parte importante relacionada à configuração está aqui: [Limpeza de revisão - Configurar a compactação total e final](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html?lang=pt-BR#how-to-configure-full-and-tail-compaction).
   * Limpeza de binários do Lucene: consulte o [Painel de operações - Limpeza de binários do Lucene](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-dashboard.html?lang=pt-BR#lucene-binaries-cleanup).
   * Coleta de lixo do armazenamento de dados: consulte a [Coleta de lixo do armazenamento de dados](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/data-store-garbage-collection.html?lang=pt-BR).
   * Limpeza de fluxo de trabalho: consulte a [Limpeza regular de instâncias de fluxo de trabalho](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/workflows-administering.html?lang=pt-BR#regular-purging-of-workflow-instances).
   * Tarefa de manutenção do log de auditoria: consulte a [Manutenção do log de auditoria](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-audit-log.html?lang=pt-BR).
* Entre em contato com a [Equipe de atendimento ao cliente do Experience Manager](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
