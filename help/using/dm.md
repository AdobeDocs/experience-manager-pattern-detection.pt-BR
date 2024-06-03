---
title: DM
description: Saiba como os códigos do detector de padrões identificam o uso do AEM Assets Dynamic Media.
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 100%

---

# DM {#dm}

Dynamic Media

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="O código DM identifica o uso do AEM Assets Dynamic Media na implementação atual. O modo de execução detecta o modo de mídia dinâmica."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="Desenvolvimento do AEM – Diretrizes e práticas recomendadas"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Diretrizes de desenvolvimento do AEM as a Cloud Service"

O `DM` (Dynamic Media) identifica o uso do AEM Assets Dynamic Media. O modo de execução detecta o modo de mídia dinâmica.

Um subtipo é usado com este código:

* `dynamic.media.runmode`: o valor associado desse subtipo, se for fornecido, é:
   * `dynamicmedia`: Dynamic Media - modo híbrido
   * `dynamicmedia_scene7`: modo Scene7 do Dynamic Media

## Possíveis implicações e riscos {#implications-and-risks}

* `dynamic.media.runmode`
   * Pode haver problemas de atualização relacionados ao Dynamic Media.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Diretrizes de implementação"
>abstract="O AEM as a Cloud Service é compatível apenas com o modo de execução dynamicmedia_scene7. Verifique as configurações atuais e entre em contato com a equipe de suporte da Adobe para obter ajuda e esclarecimentos."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media" text="Configuração do Dynamic Media"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"


* `dynamic.media.runmode`
   * Encontre mais informações em [Configuração do Dynamic Media](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media).

* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
