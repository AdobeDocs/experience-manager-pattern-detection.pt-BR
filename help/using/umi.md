---
title: UMI
description: Página de ajuda de códigos do detector de padrões.
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 94%

---

# UMI {#umi}

Problema de Configuração Incorreta de Atualização

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problema de Configuração Incorreta de Atualização"
>abstract="O UMI identifica modificações em determinadas configurações do OSGi que causarão problemas ao atualizar, incluindo uma atualização com falha ou funcionalidade reduzida."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Alterações importantes no AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Notas de versão do AEM as a Cloud Service"

`UMI`  Identifica modificações em determinadas configurações do OSGi que causam problemas ao atualizar, incluindo uma atualização com falha ou funcionalidade reduzida.

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
   * Certas funcionalidades podem não funcionar conforme esperado. Por exemplo, alterar `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` pode impedir a compilação de alguns arquivos JSP, o que resulta na perda de funcionalidade.
   * Os valores da configuração `com.day.cq.commons.impl.ExternalizerImpl` do externalizador são definidos por variáveis de ambiente do Cloud Manager no AEM as a Cloud Service.
   * O AEM as a Cloud Service não oferece suporte a arquivos de log personalizados. Os registros gravados em logs com nomes personalizados não podem ser acessados no AEM as a Cloud Service.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é rever as configurações atuais e reverter todas as alterações feitas nas configurações mencionadas para evitar problemas futuros com atualizações. Entre em contato com o Suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html?lang=pt-BR" text="Suporte da Experience Cloud"

* Não altere ou remova as quatro configurações mencionadas acima.
   * Se houver a seguinte violação:\
     “Propriedades obrigatórias para a configuração `xyz-configuration` do OSGI estão ausentes: ‘[property-1, property-2...]’”.\
     Confirme se essas exclusões são intencionais ou não, pois essas são as configurações padrão do OSGI e podem nunca ter sido modificadas ou salvas no gerenciador de configurações do OSGI.
* Se as configurações foram alteradas, elas deverão ser restauradas aos seus valores esperados. Esses valores são indicados nas mensagens do `UMI`.
* No caso de `com.day.cq.commons.impl.ExternalizerImpl`, consulte a [documentação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer) para definir a configuração do externalizador usando variáveis de ambiente do Cloud Manager no AEM as a Cloud Service.
* Para `org.apache.sling.commons.log.LogManager.factory.config`, altere a configuração do OSGI para enviar o log personalizado para o arquivo `logs/error.log`. Consulte a [documentação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs) sobre o redirecionamento para o arquivo `logs/error.log`.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
