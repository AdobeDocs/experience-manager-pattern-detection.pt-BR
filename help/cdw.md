---
title: CDW
description: Página de ajuda de códigos do detector de padrões
exl-id: a9e9dae8-0aa2-4679-a3c1-418cab01cfda
source-git-commit: d12f2613493d9bf379464d9c089ad376532c4de2
workflow-type: ht
source-wordcount: '185'
ht-degree: 100%

---

# CDW {#cdw}

Dispositivo de diálogo personalizado

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="Dispositivo de diálogo personalizado"
>abstract="O CDW identifica os Dispositivos de diálogo personalizados que devem ser atualizados para que sejam compatíveis com o AEM as a Cloud Service."

`CDW` Os Dispositivos de diálogo personalizados identificam os dispositivos de diálogo personalizados CoralUI e Classic. Eles devem ser atualizados para que sejam compatíveis com o AEM as a Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de informações, como:

* `custom.coral.widget`: identificar os dispositivos de diálogo personalizados com base no CoralUI 2 ou CoralUI 3.
* `custom.classic.widget`: identificar os dispositivos de diálogo personalizados com base em ExtJs.

## Possíveis implicações e riscos {#implications-and-risks}

* A interface clássica não está mais disponível no AEM as a Cloud Service. A interface padrão para criação é a interface habilitada para toque.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="Diretrizes de implementação"
>abstract="Entre em contato com o Atendimento ao cliente para obter ajuda."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Os Dispositivos de diálogo clássicos personalizados devem ser convertidos de ExtJS para [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html).
* Os Dispositivos de diálogo Coral personalizados devem ser avaliados para atualização para CoralUI 3.
* Entre em contato com a [Equipe de Atendimento ao cliente do Experience Manager](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
