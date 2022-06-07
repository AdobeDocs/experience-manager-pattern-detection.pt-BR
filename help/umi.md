---
title: UMI
description: Página de ajuda de códigos do detector de padrões
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: b19818f3f043641328b68adfe37a9c9cb09d1143
workflow-type: ht
source-wordcount: '325'
ht-degree: 100%

---

# UMI {#umi}

Problema de Configuração Incorreta de Atualização

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problema de Configuração Incorreta de Atualização"
>abstract="O código UMI identifica modificações em determinadas configurações do OSGi que causarão problemas ao atualizar, incluindo uma atualização com falha ou funcionalidade reduzida."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=pt-BR" text="Alterações importantes no AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR" text="O AEM as a Cloud Service - notas de versão"

O código `UMI` identifica modificações em determinadas configurações do OSGi que causarão problemas ao atualizar, incluindo uma atualização com falha ou funcionalidade reduzida.

As seguintes configurações são verificadas para procurar por modificações:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`

## Possíveis implicações e riscos {#implications-and-risks}

* Alterar ou remover configurações pode causar os seguintes problemas:
   * A atualização pode ficar paralisada (por exemplo, `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` estava ausente, mas presente em `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Problemas de autorização podem ocorrer após a atualização (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Certas funcionalidades podem não funcionar conforme esperado. Por exemplo, alterar o `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` pode resultar na não compilação de alguns arquivos JSP, o que resultará em perda de funcionalidade.
   * Os valores da configuração `com.day.cq.commons.impl.ExternalizerImpl` do externalizador são definidos por variáveis de ambiente do Cloud Manager no AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é rever as configurações atuais e reverter quaisquer alterações feitas nas configurações mencionadas para evitar problemas futuros de atualização. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Não altere ou remova as quatro configurações mencionadas acima.
   * No caso da seguinte violação:\
      “Propriedades obrigatórias para a configuração &#39;xyz-configuration&#39; do OSGi estão ausentes: &#39;[property-1, property-2...]&#39;”.\
      Confirme se essas exclusões são intencionais ou não, pois essas são as configurações padrão do OSGi e podem nunca ter sido modificadas/salvas no gerenciador de configurações do OSGi.
* Se as configurações foram alteradas, elas deverão ser restauradas aos seus valores esperados. Esses valores são indicados nas mensagens do `UMI`.
* Para `com.day.cq.commons.impl.ExternalizerImpl`, consulte a [documentação](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/externalizer.html?lang=pt-BR) para definir a configuração do externalizador usando variáveis de ambiente do Cloud Manager no AEM as a Cloud Service.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
