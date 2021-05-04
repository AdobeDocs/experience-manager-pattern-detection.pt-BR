---
title: UMI
description: Página de ajuda do código do Detector de padrões
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
translation-type: tm+mt
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 3%

---

# UMI {#umi}

Problema de Configuração Incorreta de Atualização

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problema de Configuração Incorreta de Atualização"
>abstract="O UMI identifica modificações em determinadas configurações do OSGi que causarão problemas ao atualizar, incluindo uma atualização com falha ou funcionalidade reduzida."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Alterações importantes - AEM como um Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR" text="AEM as a Cloud Service - Notas de versão"

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

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é rever suas configurações atuais e reverter quaisquer alterações feitas nas configurações mencionadas para evitar problemas futuros de atualização. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* Não altere ou remova as quatro configurações mencionadas acima.
* Se as configurações tiverem sido alteradas, elas deverão ser restauradas aos valores esperados. Esses valores são indicados nas mensagens `UMI` .
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
