---
title: IOI
description: Página de ajuda do código do Detector de padrões
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# IOI {#ioi}

Importação interna de Oak

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Importação interna de Oak"
>abstract="O código IOI identifica o uso de clientes de pacotes Oak internos, importando-os por meio de OSGi. Normalmente, são exportados sem qualquer versão específica e destinam-se ao consumo apenas por outros pacotes Oak ou serviços de AEM de baixo nível."

`IOI` O identifica o uso de clientes de pacotes Oak internos, importando-os por meio do OSGi. Normalmente, são exportados sem qualquer versão específica e destinam-se ao consumo apenas por outros pacotes Oak ou serviços de AEM de baixo nível.

Alguns deles são usados por `com.adobe.granite.repository`, que configura um repositório para AEM durante a inicialização. Outro exemplo é o pacote de Adobe `com.adobe.granite.maintenance.oak`, que envolve e fornece tarefas de manutenção do Oak.

## Possíveis implicações e riscos {#implications-and-risks}

* Em uma versão futura do AEM, as exportações internas podem ser removidas, causando dependências quebradas e pacotes inativos, dependendo diretamente do Oak.
* A API nas exportações internas pode mudar.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Diretrizes de implementação"
>abstract="Os clientes devem revisar seu código personalizado para identificar o uso dessas APIs e refatê-las para serem compatíveis com o AEM como um Cloud Service. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* Use a API de recursos do Sling (ou a API JCR) em vez de acesso de baixo nível.
* Evite depender de pacotes internos que não fazem parte de nenhuma API pública ou SPI.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
