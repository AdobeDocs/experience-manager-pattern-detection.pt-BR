---
title: DM
description: Página de ajuda do código do Detector de padrões
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 7%

---

# DM {#dm}

Dynamic Media

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="O código DM identifica o uso do AEM Assets Dynamic Media na implementação atual. O modo Dynamic Media é detectado pelo modo de execução."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html" text="Desenvolvimento de AEM - Diretrizes e práticas recomendadas"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="Diretrizes de desenvolvimento do AEM as a Cloud Service"

`DM` identifica o uso do AEM Assets Dynamic Media. O modo Dynamic Media é detectado pelo modo de execução.

Um subtipo é usado com este código:

* `dynamic.media.runmode`: O valor associado desse subtipo, se for fornecido, é:
   * `dynamicmedia`: Dynamic Media - Modo híbrido
   * `dynamicmedia_scene7`: Dynamic Media - Modo Scene7

## Possíveis implicações e riscos {#implications-and-risks}

* `dynamic.media.runmode`
   * Pode haver problemas de atualização relacionados ao Dynamic Media.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Diretrizes de implementação"
>abstract="O AEM como Cloud Service suporta apenas o modo de execução dynamicmedia_scene7. Revise as configurações atuais e entre em contato com a equipe de suporte do Adobe para obter ajuda e esclarecimentos."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html" text="Configuração do Dynamic Media"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"


* `dynamic.media.runmode`
   * Encontre mais informações em [Configurando o Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html).

* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
