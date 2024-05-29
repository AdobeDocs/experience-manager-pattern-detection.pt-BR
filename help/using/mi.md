---
title: MI
description: Página de ajuda referente ao código do detector de padrões.
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: ht
source-wordcount: '199'
ht-degree: 100%

---

# MI {#mi}

Problema de configuração incorreta

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Problema de configuração incorreta"
>abstract="O MI identifica problemas de configuração na instância do AEM"

`MI` (problema de configuração incorreta) identifica problemas de configuração na instância do AEM.

Os subtipos são usados para identificar os diferentes tipos de informações, como:

* `sling.job.max.parallel`: identifique os processos do Sling nos quais a configuração paralela máxima está definida como -1.
* `missing.maintenance.configuration`: identifique as configurações da tarefa de manutenção ausentes.

## Possíveis implicações e riscos {#implications-and-risks}

* `sling.job.max.parallel`
   * Um valor de -1 é substituído pelo número de processadores disponíveis. Dessa forma, pode causar problemas de desempenho em uma instância do AEM.
* `missing.maintenance.configuration`
   * Configurações da tarefa de manutenção ausentes podem causar queda de desempenho ou corrupção da instância.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Diretrizes de implementação"
>abstract="Entre em contato com o Atendimento ao cliente para obter ajuda."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* `sling.job.max.parallel`
   * A Adobe recomenda definir o valor como 0,5 para aproveitar metade dos processadores disponíveis.
* `missing.maintenance.configuration`
   * Limpeza de revisão: consulte [Limpeza de revisão](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup). A parte importante relacionada à configuração está aqui: [Limpeza de revisão - Configurar a compactação total e final](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup).
   * Limpeza de binários do Lucene: consulte [Painel de operações - Limpeza de binários do Lucene](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/sites/administering/operations/operations-dashboard#lucene-binaries-cleanup).
   * Coleta de lixo do armazenamento de dados: consulte [Coleta de lixo do armazenamento de dados](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/sites/administering/operations/data-store-garbage-collection).
   * Limpeza de fluxo de trabalho: consulte [Limpeza regular de instâncias de fluxo de trabalho](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/sites/administering/operations/workflows-administering#regular-purging-of-workflow-instances).
   * Tarefa de manutenção do log de auditoria: consulte [Manutenção do log de auditoria](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/sites/administering/operations/operations-audit-log).
* Entre em contato com a [equipe de atendimento ao cliente do Experience Manager](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar considerações.
