---
title: FORM
description: Página de ajuda de códigos do detector de padrões.
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 73%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="FORMS"
>abstract="O código FORMS identifica possíveis problemas relacionados à migração do Adobe Experience Manager Forms para o Adobe Experience Manager Forms as a Cloud Service. Analise possíveis implicações e riscos associados e solucione esses problemas antes de migrar para o Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-pattern-detection/table-of-contents/forms#implications-and-risks" text="Possíveis implicações e riscos"

`FORMS`  Identifica possíveis problemas relacionados à migração do [!DNL Adobe Experience Manager Forms] para [!DNL Adobe Experience Manager Forms] as a [!DNL Cloud Service]. Resolva esses problemas antes de migrar para o [!DNL Cloud Service].

Os subtipos a seguir ajudam a identificar os diferentes tipos de problemas:

* `modified.feature`: esses recursos, ativos ou APIs foram atualizados ou modificados para o Cloud Service. Antes de migrar para o Cloud Service, execute o utilitário de migração para tornar esses recursos e ativos compatíveis com o Cloud Service.
* `unavailable.feature`: seu ambiente tem recursos e ativos que não estão disponíveis ou foram removidos do Cloud Service. Não migre esses recursos ou ativos para um ambiente do Cloud Service.
* `unsupported.feature`: seu ambiente usa alguns recursos ainda não suportados no Cloud Service. Não migre esses recursos ou ativos para um ambiente do Cloud Service. Verifique as notas de versão mensais para obter informações sobre a disponibilidade dos recursos.
* `unsupported.api`: seu ambiente tem algumas APIs ainda não compatíveis com o Cloud Service. Antes de migrar para o Cloud Service, desative, substitua ou remova essas APIs do seu código. Verifique as notas de versão mensais para obter informações sobre a disponibilidade dos recursos.

Consulte as seções [Possíveis implicações e riscos](#implications-and-risks) e [Possíveis soluções](#solutions) para obter informações sobre substituições e outras ações necessárias para tornar alguns recursos e APIs compatíveis com o Cloud Service

## Possíveis implicações e riscos {#implications-and-risks}

Resolva os seguintes problemas antes de migrar para o [!DNL Adobe Experience Manager Forms as a Cloud Service]. Quando as implicações e os riscos listados abaixo não são solucionados, alguns recursos não funcionam como esperado no ambiente do Cloud Service.

* A funcionalidade do editor de códigos do recurso do editor de regras não está disponível. (CODE_EDITOR)

* O suporte de email (porta SMTP) está desativado por padrão. (EMAIL_SERVICE_CONFIGURATION)

* A variável **[!UICONTROL PDF de email]** A ação enviar não está disponível. (EMAIL_PDF_SUBMIT_ACTION)

* Os formulários adaptáveis baseados em XFA ainda não são compatíveis. (XFA_BASED_FORM, XDP_BASED_FORM)

* Uma ação enviar é invocada imediatamente no envio do formulário, em vez de esperar que todos os signatários concluam a assinatura. Portanto, o PDF de contrato do Adobe Acrobat Sign enviado aos signatários não está disponível para uso ou processamento de ações enviar. (FORM_SIGN_INTEGRATION)

* A etapa Assinatura não está disponível. (SIGNATURE_STEP)

* A etapa Verificar não está disponível. (VERIFY_STEP)

* A Ação de envio **[!UICONTROL Enviar para o Forms Workflow]** não está disponível. No AEM Forms 6.5 e em versões anteriores, a Ação de envio era usada para enviar dados de formulários adaptáveis para o AEM Forms herdado em fluxos de trabalho do JEE e do LiveCycle. (LC_WORKFLOW_SUBMISSION)

* O recurso Comunicações interativas não está disponível. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* O acordeão Metadados não está disponível. (METADATA_ACCORDION_FORM_CONTAINER)

* O componente CAPTCHA agora usa o serviço Google reCAPTCHA para validar CAPTCHA, por padrão. A opção de usar o Adobe Experience Manager para validar CAPTCHA está obsoleta. (FORMS_CAPTCHA)

* O aplicativo [!DNL AEM Forms] não está disponível para [!DNL Cloud Services]. (AEM_FORMS_APP)

* [Serviços de documentos](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/forms/install-aem-forms/osgi-installation/install-configure-document-services#deployment-topology) As etapas não estão disponíveis em Fluxos de trabalho do AEM. (WORKFLOW_DOCSERVICES)

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="Diretrizes de implementação"
>abstract="As informações expostas por meio do código FORMS podem fornecer orientação sobre substituições e outras ações necessárias para tornar alguns recursos e APIs compatíveis com o Cloud Service. Entre em contato com o Suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html?lang=pt-BR" text="Suporte da Experience Cloud"

* Use o utilitário de migração para converter todos os scripts de regras no seu ambiente em funções reutilizáveis. Você pode usar as funções reutilizáveis com o Editor de regras visuais para continuar tendo os resultados obtidos com scripts de regras. (CODE_EDITOR)

* Entre em contato com a equipe de suporte para que você possa ativar a funcionalidade de email (abrir a Porta SMTP) em seu ambiente. Por padrão, somente as conexões HTTP e HTTPS de saída são ativadas. (EMAIL_SERVICE_CONFIGURATION, Email step)

* Use a ação enviar de **[!UICONTROL Email]** em vez de **[!UICONTROL PDF de email]**. A ação enviar de **[!UICONTROL Email]** fornece opções para enviar anexos e anexar Documento de registro (DoR) com o email. (EMAIL_PDF_SUBMIT_ACTION)

* Os dados enviados contêm a ID do contrato do Adobe Acrobat Sign. Você pode usar a ID do contrato de assinatura para recuperar um PDF do contrato de assinatura, se necessário. (FORM_SIGN_INTEGRATION)

* Remova a etapa Assinatura de um formulário adaptável existente. Configurar o formulário adaptável para usar a [experiência de assinatura no navegador](https://blog.developer.adobe.com/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Ele exibe o contrato do Adobe Acrobat Sign para assinar o contrato dentro do navegador no envio de um formulário adaptável. A experiência de assinatura no navegador ajuda a fornecer uma experiência de assinatura mais rápida e economiza tempo para o signatário. (SIGNATURE_STEP)

* Remova a etapa de verificação do seu Forms adaptável existente antes de movê-los para um [!DNL Cloud Service] ambiente. (VERIFY_STEP)

* Editar seus formulários adaptáveis existentes para poder usar [Enviar para endpoint REST](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-to-rest-endpoint), [Enviar e-mail](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#send-email), [Enviar usando modelo de dados do formulário](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-using-form-data-model), e [Chamar um fluxo de trabalho de AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) Ações de envio.

* Você pode desenvolver um fluxo de trabalho para AEM e editar seus formulários adaptáveis existentes para usar [Fluxo de trabalho do AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) Enviar ação para enviar dados a um fluxo de trabalho AEM em vez de usar o **[!UICONTROL Enviar para o Forms Workflow]** Ação de envio. Você pode desenvolver uma ação enviar personalizada para enviar dados, anexos ou Documento de registro (DoR) para um processo do LiveCycle em vez de usar [!UICONTROL Enviar para o Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Verifique as notas de versão mensais para obter informações sobre a disponibilidade do recurso Comunicações interativas. Não migre suas comunicações interativas, cartas e dicionários relacionados para um ambiente Cloud Service até que o recurso não esteja disponível. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Não há substituição para o acordeão de metadados. Remova-o de seus formulários antes de migrá-los para o Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Use o Google reCAPTCHA em vez do serviço CAPTCHA fornecido pelo Adobe Experience Manager. (FORMS_CAPTCHA)

* Não migre um modelo de fluxo de trabalho do AEM que use uma etapa do fluxo de trabalho dos serviços de documento. Além disso, não migre ou atualize o Adaptive Forms que envia dados do usuário para um modelo de fluxo de trabalho que usa etapas do fluxo de trabalho dos serviços de documento ou altere a variável **`Submit Action`** para um [compatível](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions) antes de migrar o formulário. (WORKFLOW_DOCSERVICES)

* Os formulários adaptáveis oferecem um design responsivo. Esses formulários alteram a aparência, o design e a interatividade com base no dispositivo subjacente. Você pode continuar usando os formulários adaptáveis em dispositivos móveis. Verifique as notas de versão mensais para obter informações sobre a disponibilidade do aplicativo [!DNL AEM Forms]. (AEM_FORMS_APP)

* O suporte para formulários adaptáveis baseados em XFA não está disponível imediatamente. Se você pretende usar formulários adaptáveis baseados em XFA, entre em contato com o Suporte da Adobe com detalhes do caso de uso e requisitos específicos.(XFA_BASED_FORM, XDP_BASED_FORM)

Contato [Suporte para Adobe](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) se precisar de esclarecimentos ou dúvidas.
