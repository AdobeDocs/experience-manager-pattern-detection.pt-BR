---
title: FORM
description: Página de ajuda de códigos do detector de padrões
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 100%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="FORMS"
>abstract="O código FORMS identifica possíveis problemas relacionados à migração do Adobe Experience Manager Forms para o Adobe Experience Manager Forms as a Cloud Service. Analise possíveis implicações e riscos associados e solucione esses problemas antes de migrar para o Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-pattern-detection/table-of-contents/forms.html?lang=pt-BR#implications-and-risks" text="Possíveis implicações e riscos"

O código `FORMS` identifica possíveis problemas relacionados à migração do [!DNL Adobe Experience Manager Forms] para o [!DNL Adobe Experience Manager Form]s as a [!DNL Cloud Service]. Resolva esses problemas antes de migrar para o [!DNL Cloud Service].

Os subtipos a seguir ajudam a identificar os diferentes tipos de problemas:

* `modified.feature`: esses recursos, ativos ou APIs foram atualizados ou modificados para o Cloud Service. Antes de migrar para o Cloud Service, execute o utilitário de migração para tornar esses recursos e ativos compatíveis com o Cloud Service.
* `unavailable.feature`: seu ambiente tem recursos e ativos que não estão disponíveis ou foram removidos do Cloud Service. Não migre esses recursos ou ativos para um ambiente do Cloud Service.
* `unsupported.feature`: seu ambiente usa alguns recursos ainda não suportados no Cloud Service. Não migre esses recursos ou ativos para um ambiente do Cloud Service. Verifique as notas de versão mensais para obter informações sobre a disponibilidade dos recursos.
* `unsupported.api`: seu ambiente tem algumas APIs ainda não compatíveis com o Cloud Service. Antes de migrar para o Cloud Service, desative, substitua ou remova essas APIs do seu código. Verifique as notas de versão mensais para obter informações sobre a disponibilidade dos recursos.

Consulte as seções [Possíveis implicações e riscos](#implications-and-risks) e [Possíveis soluções](#solutions) para obter informações sobre substituições e outras ações necessárias para tornar alguns recursos e APIs compatíveis com o Cloud Service

## Possíveis implicações e riscos {#implications-and-risks}

Resolva os seguintes problemas antes de migrar para o [!DNL Adobe Experience Manager Forms as a Cloud Service]. Quando as implicações e os riscos listados abaixo não são solucionados, alguns recursos não funcionam como esperado no ambiente do Cloud Service.

* A funcionalidade do editor de códigos do recurso do editor de regras não está disponível. (CODE_EDITOR)

* Por padrão, o suporte de email (porta SMTP) está desativado. (EMAIL_SERVICE_CONFIGURATION)

* A ação enviar **[!UICONTROL PDF de email]** não está disponível. (EMAIL_PDF_SUBMIT_ACTION)

* Os formulários adaptáveis baseados em XFA ainda não são compatíveis. (XFA_BASED_FORM, XDP_BASED_FORM)

* Uma ação enviar é invocada imediatamente no envio do formulário, em vez de esperar que todos os signatários concluam a assinatura. Portanto, o PDF de contrato do Adobe Acrobat Sign enviado aos signatários não está disponível para uso ou processamento de ações enviar. (FORM_SIGN_INTEGRATION)

* A etapa Assinatura não está disponível. (SIGNATURE_STEP)

* A etapa Verificar não está disponível. (VERIFY_STEP)

* A Ação de envio **[!UICONTROL Enviar para o Forms Workflow]** não está disponível. No AEM Forms 6.5 e em versões anteriores, a Ação de envio era usada para enviar dados de formulários adaptáveis para o AEM Forms herdado em fluxos de trabalho do JEE e do LiveCycle. (LC_WORKFLOW_SUBMISSION)

* O recurso Comunicações interativas não está disponível.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* O acordeão Metadados não está disponível. (METADATA_ACCORDION_FORM_CONTAINER)

* O componente CAPTCHA agora usa o serviço Google reCAPTCHA para validar CAPTCHA, por padrão. A opção de usar o Adobe Experience Manager para validar CAPTCHA está obsoleta. (FORMS_CAPTCHA)

* O aplicativo [!DNL AEM Forms] não está disponível para [!DNL Cloud Services]. (AEM_FORMS_APP)

* As etapas [Serviços de documento](https://experienceleague.adobe.com/docs/experience-manager-65/forms/install-aem-forms/osgi-installation/install-configure-document-services.html?lang=pt-BR#deployment-topology) não estão disponíveis em fluxos de trabalho do AEM. (WORKFLOW_DOCSERVICES)

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="Diretrizes de implementação"
>abstract="As informações expostas por meio do código FORMS podem fornecer orientação sobre substituições e outras ações necessárias para tornar alguns recursos e APIs compatíveis com o Cloud Service. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Use o utilitário de migração para converter todos os scripts de regras no seu ambiente em funções reutilizáveis. Você pode usar as funções reutilizáveis com o Editor de regras visuais para continuar tendo os resultados obtidos com scripts de regras. (CODE_EDITOR)

* Entre em contato com a equipe de suporte para ativar a funcionalidade de email (abrir Porta SMTP) para o seu ambiente. Por padrão, somente as conexões HTTP e HTTPS de saída são ativadas. (EMAIL_SERVICE_CONFIGURATION, Email step)

* Use a ação enviar de **[!UICONTROL Email]** em vez de **[!UICONTROL PDF de email]**. A ação enviar de **[!UICONTROL Email]** fornece opções para enviar anexos e anexar Documento de registro (DoR) com o email. (EMAIL_PDF_SUBMIT_ACTION)

* Os dados enviados contêm a ID do contrato do Adobe Acrobat Sign. Você pode usar a ID do contrato de assinatura para recuperar um PDF do contrato de assinatura, se necessário.  (FORM_SIGN_INTEGRATION)

* Remova a etapa Assinatura de um formulário adaptável existente. Configurar o formulário adaptável para usar a [experiência de assinatura no navegador](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Ele exibe o contrato do Adobe Acrobat Sign para assinar o contrato dentro do navegador no envio de um formulário adaptável. A experiência de assinatura no navegador ajuda a fornecer uma experiência de assinatura mais rápida e economiza tempo para o signatário. (SIGNATURE_STEP)

* Remova a etapa de verificação dos seus formulários adaptáveis existentes antes de movê-los para um ambiente [!DNL Cloud Service]. (VERIFY_STEP)

* Modifique seus formulários adaptáveis existentes para usar as Ações de envio [Enviar para endpoint REST](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=pt-BR#submit-to-rest-endpoint), [Enviar email](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=pt-BR#send-email), [Enviar usando o Modelo de dados de formulário](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=pt-BR#submit-using-form-data-model) e [Chamar um fluxo de trabalho do AEM.](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=pt-BR#invoke-an-aem-workflow)

* Você pode desenvolver um fluxo de trabalho do AEM e modificar seus formulários adaptáveis existentes para usar a ação enviar do [fluxo de trabalho do AEM](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=pt-BR#invoke-an-aem-workflow) para enviar dados para um fluxo de trabalho do AEM em vez de usar a ação enviar **[!UICONTROL Enviar para o Forms Workflow]**. Você pode desenvolver uma ação enviar personalizada para enviar dados, anexos ou Documento de registro (DoR) para um processo do LiveCycle em vez de usar [!UICONTROL Enviar para o Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Verifique as notas de versão mensais para obter informações sobre a disponibilidade do recurso Comunicações interativas. Não migre suas comunicações interativas, cartas e dicionários relacionados para um ambiente Cloud Service até que o recurso não esteja disponível. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Não há substituição para o acordeão de metadados. Remova-o de seus formulários antes de migrá-los para o Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Use o Google reCaptcha em vez do serviço CAPTCHA fornecido pelo Adobe Experience Manager. (FORMS_CAPTCHA)

* Não migre um modelo de fluxo de trabalho do AEM que usa uma etapa do fluxo de trabalho dos serviços de documento. Além disso, não migre ou atualize formulários adaptáveis que enviem dados do usuário para um modelo de fluxo de trabalho que use as etapas do fluxo de trabalho dos serviços de documento ou altere a ação enviar para uma versão [compatível](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=pt-BR) antes de migrar o formulário. (WORKFLOW_DOCSERVICES)

* Os formulários adaptáveis oferecem um design responsivo. Esses formulários alteram a aparência, o design e a interatividade com base no dispositivo subjacente. Você pode continuar usando os formulários adaptáveis em dispositivos móveis. Verifique as notas de versão mensais para obter informações sobre a disponibilidade do aplicativo [!DNL AEM Forms]. (AEM_FORMS_APP)

* O suporte para formulários adaptáveis baseados em XFA não está disponível imediatamente. Se você pretende usar formulários adaptáveis baseados em XFA, entre em contato com o Suporte da Adobe com detalhes do caso de uso e requisitos específicos.(XFA_BASED_FORM, XDP_BASED_FORM)

Entre em contato com o [Suporte da Adobe](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
