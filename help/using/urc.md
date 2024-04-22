---
title: URC
description: Página de ajuda do código do Detector de padrões.
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 24%

---

# URC {#urc}

Configuração do modo de Execução sem Suporte

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configuração de modo de execução não compatível"
>abstract="O código URC identifica o uso de configurações que são baseadas em um nome de modo de execução não suportado no AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Modos de execução suportados"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Modos de execução"

O código URC identifica o uso de configurações que são baseadas em um nome de modo de execução não suportado no AEM as a Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é verificar se todos os modos de execução usados em seu aplicativo são compatíveis e garantir que eles sigam as diretrizes de resolução do modo de execução"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Diretrizes de resolução do modo de execução"

* O conjunto de nomes que podem ser usados para executar vários modos no AEM as a Cloud Service é limitado.
* As configurações baseadas em nomes de modo de execução não suportados não têm efeito quando implantadas no AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Ferramentas e recursos"
>abstract="Revise o projeto herdado WKND para entender como as violações de URC podem ser compatíveis com o AEM Cloud Service. Além disso, revise o exemplo de violação de URC no GitHub para entender como as configurações de OSGi baseadas em modo de execução personalizado podem ser atualizadas para aderir ao AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Projeto herdado WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Exemplo de violação de URC - GitHub"

* Revise o uso dessa configuração para que você possa determinar se ela é necessária.
* Renomeie a configuração usando um dos [nomes do modo de execução](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) e siga [diretrizes de resolução do modo de execução](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) e entenda como as [violações de URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) podem ser corrigidas e se tornar compatíveis com o AEM as a Cloud Service.
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) esclarecimentos ou de ter preocupações em conta.
