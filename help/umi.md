---
title: UMI
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# UMI {#umi}

Problema de Configuração Incorreta de Atualização

## Segundo plano {#background}

`UMI` O identifica modificações em determinadas configurações do OSGi que causarão problemas ao atualizar, incluindo uma atualização com falha ou funcionalidade reduzida.

As seguintes configurações estão verificadas para modificação:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`

## Possíveis implicações e riscos {#implications-and-risks}

* Alterar ou remover configurações pode causar os seguintes problemas:
   * A atualização pode ficar travada (por exemplo, `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` estava ausente, mas estava presente em `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Os problemas de autorização podem ocorrer após a atualização (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Certas funcionalidades podem não funcionar conforme esperado. Por exemplo, alterar `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` pode resultar na não compilação de alguns arquivos JSP, o que resultará em perda de funcionalidade.

## Possíveis soluções {#solutions}

* Não altere ou remova as quatro configurações mencionadas acima.
* Se as configurações tiverem sido alteradas, elas deverão ser restauradas aos valores esperados. Esses valores são indicados nas mensagens `UMI` .
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
