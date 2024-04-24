---
title: DM
description: Saiba como o código do Detector de padrões identifica o uso do AEM Assets - Dynamic Media.
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 52%

---

# DM {#dm}

Dynamic Media

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="O código DM identifica o uso do AEM Assets Dynamic Media na implementação atual. O modo Dynamic Media é detectado pelo modo de execução."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="Desenvolvimento do AEM - diretrizes e práticas recomendadas"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Diretrizes de desenvolvimento do AEM as a Cloud Service"

`DM` (Dynamic Media) Identifica o uso do AEM Assets Dynamic Media. O modo Dynamic Media é detectado pelo modo de execução.

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
>abstract="O AEM as a Cloud Service suporta apenas o modo de execução dynamicmedia_scene7. Revise as configurações atuais e entre em contato com a Equipe de suporte do Adobe para obter ajuda e esclarecimentos."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media" text="Configuração do Dynamic Media"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"


* `dynamic.media.runmode`
   * Encontre mais informações em [Configurar Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media).

* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) se precisar de esclarecimentos ou dúvidas.
