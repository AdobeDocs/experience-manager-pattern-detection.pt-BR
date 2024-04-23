---
title: UMI
description: Página de ajuda do código do Detector de padrões.
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 43%

---

# UMI {#umi}

Problema de Configuração Incorreta de Atualização

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problema de Configuração Incorreta de Atualização"
>abstract="O código UMI identifica modificações em determinadas configurações do OSGi que causam problemas ao atualizar, incluindo uma atualização com falha ou funcionalidade reduzida."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Alterações importantes no AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="O AEM as a Cloud Service - notas de versão"

O código UMI identifica modificações em determinadas configurações do OSGi que causam problemas ao atualizar, incluindo uma atualização com falha ou funcionalidade reduzida.

As seguintes configurações são verificadas para procurar por modificações:

* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`
* `org.apache.sling.commons.log.LogManager.factory.config`: Identifica se a propriedade `org.apache.sling.commons.log.file` dos logs personalizados aponta para algo diferente do arquivo `logs/error.log`.

## Possíveis implicações e riscos {#implications-and-risks}

* Alterar ou remover configurações pode causar os seguintes problemas:
   * A atualização pode ficar paralisada (por exemplo, `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` estava ausente, mas presente em `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Problemas de autorização podem ocorrer após a atualização (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Certas funcionalidades podem não funcionar conforme esperado. Por exemplo, alterar `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` pode resultar na não compilação de alguns arquivos JSP, o que resulta em perda de funcionalidade.
   * Os valores da configuração do Externalizador `com.day.cq.commons.impl.ExternalizerImpl` são definidos por variáveis de ambiente do cloud manager no AEM as a Cloud Service.
   * O AEM as a Cloud Service não oferece suporte a arquivos de log personalizados. Os registros gravados em logs com nomes personalizados não podem ser acessados pelo AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar as configurações atuais e reverter quaisquer alterações feitas nas configurações mencionadas para evitar problemas futuros de atualização. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Não altere ou remova as quatro configurações mencionadas acima.
   * Se houver a seguinte violação:\
     &quot;Propriedades obrigatórias para a configuração do OSGi `xyz-configuration` estão ausentes: &#39;[property-1,property-2...]&#39;.&quot;\
     Confirme se essas exclusões são legítimas ou não, pois essas configurações OSGi são OOTB e podem nunca ter sido modificadas/salvas no Gerenciador de configurações OSGi.
* Se as configurações foram alteradas, elas deverão ser restauradas aos seus valores esperados. Esses valores são indicados nas mensagens do `UMI`.
* Para `com.day.cq.commons.impl.ExternalizerImpl`, consulte [documentação](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer) para definir a configuração do Externalizador usando variáveis de ambiente do Cloud Manager no AEM as a Cloud Service.
* Para `org.apache.sling.commons.log.LogManager.factory.config`, altere a configuração do OSGI para enviar o log personalizado para o arquivo `logs/error.log`. Consulte [documentação](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs) para redirecionar para a `logs/error.log` arquivo.
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) esclarecimentos ou de ter preocupações em conta.
