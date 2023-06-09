---
title: IOI
description: Página de ajuda de códigos do detector de padrões
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '233'
ht-degree: 100%

---

# IOI {#ioi}

Importação interna de Oak

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Importação interna de Oak"
>abstract="O código IOI identifica o uso de pacotes Oak internos por clientes, importando-os por meio de OSGi. Normalmente, são exportados sem qualquer versão específica e destinam-se ao consumo apenas por outros pacotes Oak ou por serviços de baixo nível do AEM."

`IOI` identifica o uso de pacotes Oak internos por clientes, importando-os por meio do OSGi. Normalmente, são exportados sem qualquer versão específica e destinam-se ao consumo apenas por outros pacotes Oak ou por serviços de baixo nível do AEM.

Alguns deles são usados por `com.adobe.granite.repository`, que configura um repositório para o AEM durante a inicialização. Outro exemplo é o pacote Adobe `com.adobe.granite.maintenance.oak`, que contém e fornece tarefas de manutenção do Oak.

## Possíveis implicações e riscos {#implications-and-risks}

* Em uma versão futura do AEM, as exportações internas podem ser removidas, causando dependências quebradas e pacotes inativos, dependendo diretamente do Oak.
* A API nas exportações internas pode mudar.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Diretrizes de implementação"
>abstract="Os clientes devem revisar seu código personalizado para identificar o uso dessas APIs e fatorá-las novamente para que sejam compatíveis com o AEM as a Cloud Service. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Use a API de recursos do Sling (ou a API JCR) em vez de acesso de baixo nível.
* Evite depender de pacotes internos que não fazem parte de nenhuma API ou SPI pública.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
