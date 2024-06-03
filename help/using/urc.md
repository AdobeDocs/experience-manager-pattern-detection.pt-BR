---
title: URC
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 100%

---

# URC {#urc}

Configuração do modo de execução incompatível

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configuração do modo de execução incompatível"
>abstract="O URC identifica o uso de configurações baseadas em um nome de modo de execução não compatível com o AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Modos de execução compatíveis"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Modos de execução"

`URC` identifica o uso de configurações baseadas em um nome do modo de execução incompatível com o AEM as a Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é verificar se todos os modos de execução usados no aplicativo são compatíveis. Certifique-se também de que eles sigam as diretrizes de resolução de modos de execução"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Diretrizes de resolução de modos de execução"

* O conjunto de nomes que pode ser usado para executar vários modos no AEM as a Cloud Service é limitado.
* As configurações baseadas em nomes de modo de execução incompatíveis não terão efeito quando implantadas no AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Ferramentas e recursos"
>abstract="Revise o projeto WKND herdado para entender como as violações de URC podem ficar compatíveis com o AEM Cloud Service. Além disso, consulte o exemplo de violação do URC no GitHub para entender como atualizar configurações personalizadas de OSGi baseadas no modo de execução para garantir a conformidade com o AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Projeto herdado WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Exemplo de violação de URC no GitHub"

* Revise o uso dessa configuração para determinar se ela é necessária.
* Renomeie a configuração usando um dos [nomes de modo de execução](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) compatíveis e siga as [diretrizes de resolução do modo de execução](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) e entenda como as [violações de URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) podem ser corrigidas e se tornar compatíveis com o AEM as a Cloud Service.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
