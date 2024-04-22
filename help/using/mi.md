---
title: MI
description: Página de ajuda do código do Detector de padrões.
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 54%

---

# MI {#mi}

Problema de configuração incorreta

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Problema de configuração incorreta"
>abstract="O MI identifica problemas de configuração na instância do AEM"

MI Misconfiguration Issue identifica problemas de configuração na instância do AEM.

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
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html?lang=pt-BR" text="Suporte da Experience Cloud"

* `sling.job.max.parallel`
   * A Adobe recomenda configurar o valor como 0,5 para aproveitar a metade dos processadores disponíveis.
* `missing.maintenance.configuration`
   * Limpeza de revisão: consulte [Limpeza de revisão](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup). A parte importante relacionada à configuração está aqui: [Limpeza de revisão - Configurar a compactação total e final](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup).
   * Limpeza de binários do Lucene: consulte [Painel de operações - Limpeza de binários do Lucene](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/operations-dashboard#lucene-binaries-cleanup).
   * Coleta de Lixo do Armazenamento de Dados: Consulte [Coleta de lixo do armazenamento de dados](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/data-store-garbage-collection).
   * Expurgação do Workflow: Consulte [Limpeza regular de instâncias de fluxo de trabalho](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/workflows-administering#regular-purging-of-workflow-instances).
   * Tarefa de manutenção do AuditLog: consulte [Manutenção do Log de Auditoria](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/operations-audit-log).
* Entre em contato com [Equipe de Atendimento ao cliente do Experience Manager](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) clarificações ou para dar resposta a preocupações.
