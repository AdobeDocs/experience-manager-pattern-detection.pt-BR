---
title: URC
description: Página de ajuda do código do Detector de padrões
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# URC {#urc}

Configuração de Modo de Execução Não Suportado

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configuração de Modo de Execução Não Suportado"
>abstract="O URC identifica o uso de configurações que são baseadas em um nome de modo de execução que não é suportado no AEM como um Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes" text="Runmodes Suportados"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#runmodes" text="Runmodes"

`URC` O identifica o uso de configurações baseadas em um nome de modo de execução que não é suportado no AEM como Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Diretrizes de implementação"
>abstract="A Prática Recomendada é verificar se todos os modos de execução usados em seu aplicativo são compatíveis e garantir que sigam as diretrizes de resolução do modo de execução"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#deploying" text="Diretrizes de resolução do modo de execução"

* O conjunto de nomes que pode ser usado para runmodes no AEM como Cloud Service é limitado.
* As configurações baseadas em nomes de modo de execução não suportados não terão efeito quando implantadas em AEM como Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Ferramentas e recursos"
>abstract="Revise o projeto herdado WKND para entender como as violações de URC podem ser tornadas compatíveis com AEM Cloud Service. Além disso, analise o exemplo de violação de URC no Github para entender como as configurações de OSGi baseadas em modo de execução personalizado podem ser atualizadas para aderir com o AEM como Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Projeto WKND-Legacy"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Exemplo de violação de URC - Github"

* Revise o uso dessa configuração para determinar se ela é necessária.
* Renomeie a configuração para usar um dos [nomes do modo de execução](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) suportados e siga [diretrizes de resolução do modo de execução](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) e entenda como as [violações URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) podem ser corrigidas e tornadas compatíveis com AEM como um Cloud Service.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
