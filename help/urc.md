---
title: URC
description: Página de ajuda de códigos do detector de padrões
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: ht
source-wordcount: '319'
ht-degree: 100%

---

# URC {#urc}

Configuração de modo de execução não compatível

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configuração de modo de execução não compatível"
>abstract="O código URC identifica o uso de configurações que são baseadas em um nome de modo de execução não suportado no AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=pt-BR#custom-runmodes" text="Modos de execução suportados"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=pt-BR#runmodes" text="Modos de execução"

O código `URC` identifica o uso de configurações que são baseadas em um nome de modo de execução não suportado no AEM as a Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é verificar se todos os modos de execução usados em seu aplicativo são compatíveis e garantir que eles sigam as diretrizes de resolução do modo de execução"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=pt-BR#deploying" text="Diretrizes de resolução do modo de execução"

* O conjunto de nomes que pode ser usado para os modos de execução no AEM as a Cloud Service é limitado.
* As configurações baseadas em nomes de modo de execução não suportados não terão efeito quando implantadas no AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Ferramentas e recursos"
>abstract="Revise o projeto herdado WKND para entender como as violações de URC podem ser compatíveis com o AEM Cloud Service. Além disso, revise o exemplo de violação de URC no Github para entender como as configurações de OSGi baseadas em modo de execução personalizado podem ser atualizadas para aderir ao AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Projeto herdado WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Exemplo de violação de URC - Github"

* Revise o uso dessa configuração para determinar se ela é necessária.
* Renomeie a configuração para usar um dos [nomes de modo de execução](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=pt-BR#custom-runmodes) compatíveis e siga as [diretrizes de resolução do modo de execução](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=pt-BR#runmode-resolution).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) e entenda como as [violações de URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) podem ser corrigidas e se tornar compatíveis com o AEM as a Cloud Service.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
