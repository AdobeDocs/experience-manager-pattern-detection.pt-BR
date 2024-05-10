---
title: URC
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '261'
ht-degree: 100%

---

# URC {#urc}

Configuração do modo de execução não compatível

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configuração de modo de execução não compatível"
>abstract="O URC identifica o uso de configurações baseadas em um nome de modo de execução não compatível com o AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Modos de execução compatíveis"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Modos de execução"

`URC` identifica o uso de configurações baseadas em um nome do modo de execução incompatível com o AEM as a Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é verificar se todos os modos de execução usados em seu aplicativo são compatíveis e garantir que sigam as diretrizes de resolução do modo de execução"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Diretrizes de resolução do modo de execução"

* O conjunto de nomes que pode ser usado para executar vários modos no AEM as a Cloud Service é limitado.
* As configurações baseadas em nomes de modo de execução incompatíveis não terão efeito quando implantadas no AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Ferramentas e recursos"
>abstract="Revise o projeto herdado WKND para entender como as violações de URC podem ser compatíveis com o AEM Cloud Service. Além disso, revise o exemplo de violação de URC no GitHub para entender como as configurações personalizadas de OSGi baseadas em modo de execução podem ser atualizadas em conformidade com o AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Projeto herdado WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Exemplo de violação de URC no GitHub"

* Revise o uso dessa configuração para determinar se ela é necessária.
* Renomeie a configuração usando um dos [nomes de modo de execução](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) compatíveis e siga as [diretrizes de resolução do modo de execução](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) e entenda como as [violações de URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) podem ser corrigidas e se tornar compatíveis com o AEM as a Cloud Service.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
