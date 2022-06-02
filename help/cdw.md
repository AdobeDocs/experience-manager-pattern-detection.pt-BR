---
title: CDW
description: Página de ajuda de códigos do detector de padrões
source-git-commit: 04709ba74eedad903669aae589c605542e1e3b09
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 44%

---

# CDW {#cdw}

Widget de diálogo personalizado

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="Widget de diálogo personalizado"
>abstract="O CDW identifica os widgets de caixa de diálogo personalizados que devem ser atualizados para que sejam compatíveis com AEM as a Cloud Service."

`CDW`  Os widgets de diálogo personalizados identificam os widgets de diálogo CoralUI e Classic personalizados. Eles devem ser atualizados para serem compatíveis com AEM as a Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de informações, como:

* `custom.coral.widget`: Identifique os widgets de diálogo personalizados com base na CoralUI 2 ou na CoralUI 3.
* `custom.classic.widget`: Identifique os widgets de diálogo personalizados com base em ExtJs.

## Possíveis implicações e riscos {#implications-and-risks}

* A interface clássica não está mais disponível no AEM as a Cloud Service. A interface padrão para criação é a interface habilitada para toque.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="Diretrizes de implementação"
>abstract="Entre em contato com o Atendimento ao cliente para obter ajuda."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Os widgets de caixa de diálogo clássico personalizado devem ser convertidos de ExtJS para [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html).
* Os widgets da caixa de diálogo Coral personalizado devem ser avaliados para atualização para CoralUI 3.
* Entre em contato com a [Equipe de Atendimento ao cliente do Experience Manager](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
