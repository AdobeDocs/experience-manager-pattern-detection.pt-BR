---
title: INS
description: Página de ajuda de códigos do detector de padrões
source-git-commit: e469b546a75a77e538a54de3ffc1ca385c8cf21d
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 47%

---

# INS {#ins}

Namespace inválido

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_overview"
>title="Namespace inválido"
>abstract="O código INS identifica problemas de namespace na instância AEM"

`INS`  O namespace inválido identifica problemas de namespace na instância AEM.

Os subtipos são usados para identificar os diferentes tipos de informações, como:

* `uri`: Identifique o URI de namespace inválido no AEM.

## Possíveis implicações e riscos {#implications-and-risks}

* Não é possível replicar o conteúdo (entre camadas) ou copiar o conteúdo (entre ambientes — via `/crx/packMgr` ou Cópia de conteúdo).

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_guidance"
>title="Diretrizes de implementação"
>abstract="Entre em contato com o Atendimento ao cliente para obter ajuda."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Corrigir as definições de namespace de acordo com [Especificação do JCR](https://developer.adobe.com/experience-manager/reference-materials/spec/jcr/1.0/4.5_Namespaces.html). Seguir as etapas mencionadas [aqui](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/how-can-i-delete-a-namespace-created-in-crx/td-p/225163)
* Entre em contato com a [Equipe de atendimento ao cliente do Experience Manager](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.