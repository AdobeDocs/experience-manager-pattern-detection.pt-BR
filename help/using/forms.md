---
title: FORM
description: Página de ajuda referente ao código do detector de padrões.
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: ht
source-wordcount: '986'
ht-degree: 100%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="FORMS"
>abstract="O código FORMS identifica possíveis problemas relacionados à migração do AEM (Adobe Experience Manager) Forms para o AEM Forms as a Cloud Service. Analise as possíveis implicações e riscos associados, e solucione esses problemas antes de migrar para o Cloud Service."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-pattern-detection/table-of-contents/forms#implications-and-risks" text="Possíveis implicações e riscos"

`FORMS` identifica possíveis problemas relacionados à migração do [!DNL Adobe Experience Manager Forms] para o [!DNL Adobe Experience Manager Forms] as a [!DNL Cloud Service]. Resolva esses problemas antes de migrar para o [!DNL Cloud Service].

Os subtipos a seguir ajudam a identificar os diferentes tipos de problemas:

* `modified.feature`: esses recursos, ativos ou APIs foram atualizados ou modificados para o Cloud Service. Antes de migrar para o Cloud Service, execute o utilitário de migração para tornar esses recursos e ativos compatíveis com o Cloud Service.
* `unavailable.feature`: seu ambiente tem recursos e ativos que não estão disponíveis ou foram removidos do Cloud Service. Não migre esses recursos ou ativos para um ambiente do Cloud Service.
* `unsupported.feature`: seu ambiente usa alguns recursos ainda não suportados no Cloud Service. Não migre esses recursos ou ativos para um ambiente do Cloud Service. Verifique as notas de versão mensais para obter informações sobre a disponibilidade dos recursos.
* `unsupported.api`: seu ambiente tem algumas APIs ainda não compatíveis com o Cloud Service. Antes de migrar para o Cloud Service, desative, substitua ou remova essas APIs do seu código. Verifique as notas de versão mensais para obter informações sobre a disponibilidade dos recursos.

Consulte as seções [Possíveis implicações e riscos](#implications-and-risks) e [Possíveis soluções](#solutions) para obter informações sobre substituições e outras ações necessárias para tornar alguns recursos e APIs compatíveis com o Cloud Service

## Possíveis implicações e riscos {#implications-and-risks}

Resolva os seguintes problemas antes de migrar para o [!DNL Adobe Experience Manager Forms as a Cloud Service]. Quando as implicações e os riscos listados abaixo não são solucionados, alguns recursos não funcionam como esperado no ambiente do Cloud Service.

* A funcionalidade do editor de códigos do recurso do editor de regras não está disponível. (CODE_EDITOR)

* Por padrão, a compatibilidade com email (porta SMTP) está desabilitada. (EMAIL_SERVICE_CONFIGURATION)

* A ação de envio **[!UICONTROL PDF por email]** não está disponível.  (EMAIL_PDF_SUBMIT_ACTION)

* Os formulários adaptáveis baseados em XFA ainda não são compatíveis. (XFA_BASED_FORM, XDP_BASED_FORM)

* Uma ação enviar é invocada imediatamente no envio do formulário, em vez de esperar que todos os signatários concluam a assinatura. Portanto, o PDF de contrato do Adobe Acrobat Sign enviado aos signatários não está disponível para uso ou processamento de ações enviar. (FORM_SIGN_INTEGRATION)

* A etapa Assinatura não está disponível. (SIGNATURE_STEP)

* A etapa Verificar não está disponível. (VERIFY_STEP)

* A Ação de envio **[!UICONTROL Enviar para o Forms Workflow]** não está disponível. No AEM Forms 6.5 e em versões anteriores, a Ação de envio era usada para enviar dados de formulários adaptáveis para o AEM Forms herdado em fluxos de trabalho do JEE e do LiveCycle. (LC_WORKFLOW_SUBMISSION)

* O recurso de comunicações interativas não está disponível. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* O acordeão Metadados não está disponível. (METADATA_ACCORDION_FORM_CONTAINER)

* O componente CAPTCHA agora usa o serviço Google reCAPTCHA para validar CAPTCHA, por padrão. A opção de usar o Adobe Experience Manager para validar CAPTCHA está obsoleta. (FORMS_CAPTCHA)

* O aplicativo [!DNL AEM Forms] não está disponível para [!DNL Cloud Services]. (AEM_FORMS_APP)

* As etapas dos [Serviços de documento](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/forms/install-aem-forms/osgi-installation/install-configure-document-services#deployment-topology) não estão disponíveis nos fluxos de trabalho do AEM. (WORKFLOW_DOCSERVICES)

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="Diretrizes de implementação"
>abstract="As informações expostas por meio do código FORMS podem fornecer orientação sobre substituições e outras ações necessárias para tornar alguns recursos e APIs compatíveis com o Cloud Service. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Use um utilitário de migração para converter todos os scripts de regras no seu ambiente em funções reutilizáveis. E possível usar as funções reutilizáveis com o Editor de regras visuais para continuar recebendo resultados obtidos com scripts de regras. (CODE_EDITOR)

* Entre em contato com a equipe de suporte para habilitar a funcionalidade de email (porta SMTP aberta) no seu ambiente. Por padrão, somente as conexões HTTP e HTTPS de saída estão habilitadas. (EMAIL_SERVICE_CONFIGURATION, Email step)

* Use a ação enviar de **[!UICONTROL Email]** em vez de **[!UICONTROL PDF de email]**. A ação enviar de **[!UICONTROL Email]** fornece opções para enviar anexos e anexar Documento de registro (DoR) com o email. (EMAIL_PDF_SUBMIT_ACTION)

* Os dados enviados contêm a ID do contrato do Adobe Acrobat Sign. É possível usar a ID do contrato do Sign para recuperar um PDF de contrato do Sign, se necessário. (FORM_SIGN_INTEGRATION)

* Remova a etapa Assinatura de um formulário adaptável existente. Configure o formulário adaptável para usar uma [experiência de assinatura no navegador](https://blog.developer.adobe.com/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Exibe o contrato do Adobe Sign para assiná-lo no navegador ao enviar um formulário adaptável. A experiência de assinatura no navegador ajuda a fornecer uma experiência de assinatura mais rápida e economiza tempo para o signatário. (SIGNATURE_STEP)

* Remova a etapa de verificação dos seus formulários adaptáveis antes de movê-los para um ambiente do [!DNL Cloud Service]. (VERIFY_STEP)

* Edite os seus formulários adaptáveis para usar as ações de envio [Enviar para o terminal REST](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-to-rest-endpoint), [Enviar email](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#send-email), [Enviar usando modelo de dados do formulário](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-using-form-data-model) e [Chamar um fluxo de trabalho AEM](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow).

* É possível desenvolver um fluxo de trabalho do AEM e editar os seus formulários adaptáveis para usar a ação de envio [Fluxo de trabalho do AEM](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) para enviar dados a um fluxo de trabalho do AEM em vez de usar a ação de envio **[!UICONTROL Enviar para Fomulários de fluxo de trabalho]**. Você pode desenvolver uma ação enviar personalizada para enviar dados, anexos ou Documento de registro (DoR) para um processo do LiveCycle em vez de usar [!UICONTROL Enviar para o Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Verifique as notas de versão mensais para obter informações sobre a disponibilidade do recurso Comunicações interativas. Não migre suas comunicações interativas, cartas e dicionários relacionados para um ambiente Cloud Service até que o recurso não esteja disponível. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Não há substituição para o acordeão de metadados. Remova-o de seus formulários antes de migrá-los para o Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Use o Google reCAPTCHA em vez do serviço CAPTCHA fornecido pelo Adobe Experience Manager. (FORMS_CAPTCHA)

* Não migre para um modelo de fluxo de trabalho do AEM que utilize uma etapa de fluxo de trabalho dos serviços de documento. Também não migre nem atualize formulários adaptáveis que enviem dados do usuário a um modelo de fluxo de trabalho que utilize as etapas de fluxo de trabalho dos serviços de documento ou altere a **`Submit Action`** para uma [versão compatível](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions) antes de migrar o formulário. (WORKFLOW_DOCSERVICES)

* Os formulários adaptáveis oferecem um design responsivo. Esses formulários alteram a aparência, o design e a interatividade com base no dispositivo subjacente. Você pode continuar usando os formulários adaptáveis em dispositivos móveis. Verifique as notas de versão mensais para obter informações sobre a disponibilidade do aplicativo do [!DNL AEM Forms]. (AEM_FORMS_APP)

* O suporte para formulários adaptáveis baseados em XFA não está disponível imediatamente. Se você pretende usar formulários adaptáveis baseados em XFA, entre em contato com o Suporte da Adobe com detalhes do caso de uso e requisitos específicos.(XFA_BASED_FORM, XDP_BASED_FORM)

Entre em contato com o [suporte da Adobe](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar os suas considerações.
