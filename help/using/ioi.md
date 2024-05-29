---
title: IOI
description: Página de ajuda referente ao código do detector de padrões.
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: ht
source-wordcount: '212'
ht-degree: 100%

---

# IOI {#ioi}

Importação interna de Oak

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Importação interna de Oak"
>abstract="O código IOI identifica o uso de pacotes Oak internos por clientes, importando-os por meio do OSGi. São exportados sem nenhuma versão específica. Apenas pacotes Oak ou serviços do AEM de nível inferior os consomem."

`IOI` identifica o uso de pacotes Oak internos por clientes, importando-os por meio do OSGi. São exportados sem nenhuma versão específica. Apenas pacotes Oak ou serviços do AEM de nível inferior os consomem.
Algumas dessas áreas são usadas por `com.adobe.granite.repository`, o que configura um repositório para o AEM durante a inicialização. Outro exemplo é o pacote Adobe `com.adobe.granite.maintenance.oak`, que contém e fornece tarefas de manutenção do Oak.

## Possíveis implicações e riscos {#implications-and-risks}

* Em uma versão futura do AEM, as exportações internas poderão ser removidas, causando quebra de dependências e pacotes inativos que dependem diretamente do Oak.
* A API nas exportações internas pode mudar.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Diretrizes de implementação"
>abstract="Os clientes devem revisar seu código personalizado para identificar o uso dessas APIs e fatorá-las novamente para que sejam compatíveis com o AEM as a Cloud Service. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Use a API de recursos do Sling (ou a API JCR) em vez de acesso de baixo nível.
* Evite depender de pacotes internos que não fazem parte de nenhuma API ou SPI pública.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
