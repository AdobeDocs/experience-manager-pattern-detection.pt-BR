---
title: DM
description: Página de ajuda de códigos do detector de padrões
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# DM {#dm}

Dynamic Media

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="O código DM identifica o uso do AEM Assets Dynamic Media na implementação atual. O modo Dynamic Media é detectado pelo modo de execução."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html?lang=pt-BR" text="Desenvolvimento do AEM - diretrizes e práticas recomendadas"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=pt-BR" text="Diretrizes de desenvolvimento do AEM as a Cloud Service"

`DM` identifica o uso do AEM Assets Dynamic Media. O modo Dynamic Media é detectado pelo modo de execução.

Um subtipo é usado com este código:

* `dynamic.media.runmode`: o valor associado desse subtipo, se for fornecido, é:
   * `dynamicmedia`: Dynamic Media - modo híbrido
   * `dynamicmedia_scene7`: Dynamic Media - modo Scene7

## Possíveis implicações e riscos {#implications-and-risks}

* `dynamic.media.runmode`
   * Pode haver problemas de atualização relacionados ao Dynamic Media.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Diretrizes de implementação"
>abstract="O AEM as a Cloud Service é compatível apenas com o modo de execução dynamicmedia_scene7. Revise as configurações atuais e entre em contato com a equipe de suporte da Adobe para obter ajuda e esclarecimentos."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html?lang=pt-BR" text="Configuração do Dynamic Media"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"


* `dynamic.media.runmode`
   * Encontre mais informações em [Configuração do Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html?lang=pt-BR).

* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
