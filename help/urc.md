---
title: URC
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# URC {#urc}

Configuração de Modo de Execução Não Suportado

## Segundo plano {#background}

`URC` O identifica o uso de configurações baseadas em um nome de modo de execução que não é suportado no AEM como Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

* O conjunto de nomes que pode ser usado para runmodes no AEM como Cloud Service é limitado.
* As configurações baseadas em nomes de modo de execução não suportados não terão efeito quando implantadas em AEM como Cloud Service.

## Possíveis soluções {#solutions}

* Revise o uso dessa configuração para determinar se ela é necessária.
* Renomeie a configuração para usar um dos [nomes do modo de execução](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) suportados e siga [diretrizes de resolução do modo de execução](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) e entenda como as [violações URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) podem ser corrigidas e tornadas compatíveis com AEM como um Cloud Service.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
