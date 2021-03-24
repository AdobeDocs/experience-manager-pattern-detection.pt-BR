---
title: REP
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 7d05067fc624571e6fe520e2a1addd5dff8acbd8
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 2%

---


# [!DNL REP] {#rep}

Agente de replicação

## Segundo plano {#background}

`REP` identifica agentes de replicação ativados. Eles são relatados devido ao potencial para problemas que devem ser abordados ao atualizar para o AEM como um Cloud Service.

O AEM como Cloud Service usa [Distribuição de conteúdo de sling](https://sling.apache.org/documentation/bundles/content-distribution.html) para distribuir conteúdo do autor para publicar ambientes. Isso é feito fora do tempo de execução AEM usando o serviço de pipeline do Adobe I/O. Isso é configurado automaticamente no AEM provisionado como um ambiente Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

* A configuração da replicação foi alterada com AEM como Cloud Service. Todos os agentes de replicação atuais devem ser revisados para ver quais são substituídos pelo recurso padrão, quais configurações devem ser movidas para código e quais não são suportadas.
* Qualquer uso de agentes de replicação no código personalizado ou em workflows deve ser revisado durante a atualização para o AEM como um Cloud Service.
* Inicialmente, a replicação inversa não é compatível no AEM como Cloud Service.
* Não há necessidade de configurar um agente de liberação do dispatcher separado. Isso é configurado automaticamente no AEM como um ambiente Cloud Service.

## Possíveis soluções {#solutions}

* Consulte o AEM como Cloud Service [Diretrizes de desenvolvimento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents) e notas de versão para [agentes de replicação](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents).
* Revise, refatere e otimize a funcionalidade diretamente dependente dos agentes de replicação para executar tarefas comerciais.
* Veja como [replication](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication) é afetado pela implantação no AEM como um Cloud Service.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
