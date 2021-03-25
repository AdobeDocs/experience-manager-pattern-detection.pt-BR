---
title: FORMULÁRIO
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 9a02482d023ce1a6cbbff24b8e6509c91ddd2a6b
workflow-type: tm+mt
source-wordcount: '1136'
ht-degree: 0%

---


# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Segundo plano {#background}

`FORMS` Identifica possíveis problemas relacionados à migração do  [!DNL Adobe Experience Manager Forms] para o  [!DNL Adobe Experience Manager Form]como  [!DNL Cloud Service]. Resolva esses problemas antes de migrar para [!DNL Cloud Service].

Os subtipos a seguir ajudam a identificar os diferentes tipos de problemas:

* `modified.feature`: Esses recursos, ativos ou APIs foram atualizados ou modificados para o Cloud Service. Antes de migrar para o Cloud Service, execute o utilitário de migração para tornar esses recursos e ativos compatíveis com o Cloud Service.
* `unavailable.feature`: Seu ambiente tem recursos e ativos que não estão disponíveis ou removidos do Cloud Service. Não migre esses recursos ou ativos para um ambiente Cloud Service.
* `unsupported.feature`: Seu ambiente usa alguns recursos ainda não suportados no Cloud Service. Não migre esses recursos ou ativos para um ambiente Cloud Service. Procure notas de versão mensais para obter informações sobre a disponibilidade dos recursos.
* `unsupported.api`: Seu ambiente tem algumas APIs ainda não compatíveis no Cloud Service. Antes de migrar para o Cloud Service, desative, substitua ou remova essas APIs do seu código. Procure notas de versão mensais para obter informações sobre a disponibilidade dos recursos.

Consulte as seções [Possíveis implicações e riscos](#implications-and-risks) e [Possíveis soluções](#solutions) para obter informações sobre substituições e outras ações necessárias para tornar alguns recursos e APIs compatíveis com o Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

Resolva os seguintes problemas, antes de migrar para [!DNL Adobe Experience Manager Forms as a Cloud Service]. Quando as implicações e os riscos listados abaixo não são abordados, alguns recursos não funcionam como esperado no ambiente do Cloud Service.

* A funcionalidade do editor de códigos do recurso do editor de regras não está disponível. (CODE_EDITOR)

* Por padrão, o suporte de email (porta SMTP) está desativado. (EMAIL_SERVICE_CONFIGURATION)

* A Ação **[!UICONTROL Enviar PDF por email]** não está disponível.(EMAIL_PDF_SUBMIT_ACTION)

* A Forms adaptativa baseada em XFA ainda não é suportada. (XFA_BASED_FORM, XDP_BASED_FORM)

* Uma Ação Enviar é invocada imediatamente no envio do formulário, em vez de esperar que todos os signatários concluam a assinatura. Portanto, o PDF do contrato Adobe Sign enviado aos signatários não está disponível para envio de ações para uso ou processamento. (FORM_SIGN_INTEGRATION)

* A etapa Assinatura não está disponível. (SIGNATURE_STEP)

* A etapa Verificar não está disponível. (VERIFY_STEP)

* O recurso Portal do Forms e **[!UICONTROL Ação de Envio do Portal do Forms]** ainda não estão disponíveis. (FORMS_PORTAL_SUBMmission, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* A Ação **[!UICONTROL Enviar para Forms Workflow]** Enviar não está disponível. Em [!DNL AEM 6.5 Forms] e versões anteriores, a Ação de envio foi usada para enviar dados de formulário adaptáveis para fluxos de trabalho e LiveCycles Workflow herdados [!DNL AEM Forms on JEE]. (LC_WORKFLOW_SUBMmission)

* O recurso Comunicações interativas não está disponível.  (FP_PROFILE_INTERATIVE_COMMUNICATIONS).

* **[!UICONTROL No momento, os recursos de formulário adaptável Salvar como]** rascunho e  **** Salvar automaticamente não são suportados. (RASCUNHO_AUTO_SAVE, RASCUNHO_SAVE)

* A opção Metadados não está disponível. (METADATA_ACCORDION_FORM_CONTAINER)

* O componente CAPTCHA agora usa o serviço Google reCAPTCHA para validar CAPTCHA, por padrão. A opção de usar o Adobe Experience Manager para validar CAPTCHA está obsoleta. (FORMS_CAPTCHA)

* [!DNL AEM Forms] o aplicativo não está disponível para  [!DNL Cloud Services]. (AEM_FORMS_APP)

* [As ](https://experienceleague.adobe.com/docs/experience-manager-65/forms/install-aem-forms/osgi-installation/install-configure-document-services.html?lang=en#deployment-topology) etapas dos Serviços de documento não estão disponíveis nos Fluxos de trabalho AEM. (WORKFLOW_DOCSERVICES)

## Possíveis soluções {#solutions}

* Use o utilitário de migração para converter todos os scripts de regras em seu ambiente em funções reutilizáveis. Você pode usar as funções reutilizáveis com o Editor de regras visuais para continuar obtendo resultados obtidos com scripts de regras. (CODE_EDITOR)

* Entre em contato com a equipe de suporte para ativar a funcionalidade de email (abrir Porta SMTP) para seu ambiente. Por padrão, somente as conexões HTTP e HTTPS de saída são ativadas. (EMAIL_SERVICE_CONFIGURATION, etapa Email)

* Use **[!UICONTROL Email]** Enviar ação em vez de **[!UICONTROL Email PDF]**. A **[!UICONTROL Ação de envio de email]** fornece opções para enviar anexos e anexar Documento de registro (DoR) com email. (EMAIL_PDF_SUBMIT_ACTION)

* Os dados enviados contêm a ID do contrato da Adobe Sign. Você pode usar a ID do contrato de assinatura para recuperar um PDF do contrato de assinatura, se necessário.  (FORM_SIGN_INTEGRATION)

* Remova a etapa Assinatura de um formulário adaptável existente. Configure seu formulário adaptável para usar [experiência de assinatura no navegador](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Ele exibe o contrato da Adobe Sign para assinar o contrato dentro do navegador no envio de um formulário adaptável. A experiência de assinatura no navegador ajuda a fornecer uma experiência de assinatura mais rápida e economiza tempo para o assinante. (SIGNATURE_STEP)

* Remova a etapa de verificação do Adaptive Forms existente antes de movê-los para um ambiente [!DNL Cloud Service]. (VERIFY_STEP)

* Modifique seus formulários adaptáveis existentes para usar [Enviar para o endpoint REST](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-to-rest-endpoint), [Enviar email](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#send-email), [Enviar usando o Modelo de dados de formulário](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-using-form-data-model) e [Invocar um fluxo de trabalho AEM](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Enviar ações. A Ação de Envio do Portal do Forms e do Portal do Forms ainda não está disponível. Procure notas de versão mensais para obter informações sobre a disponibilidade dos recursos. (FORMS_PORTAL_SUBMmission, FORMS_PORTAL)

* Você pode desenvolver um Fluxo de trabalho AEM e modificar seus formulários adaptáveis existentes para usar [AEM Fluxo de trabalho](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Enviar ação para enviar dados para um Fluxo de trabalho AEM em vez de usar a **[!UICONTROL Enviar para Forms Workflow]** Enviar ação. Você pode desenvolver uma Ação de envio personalizada para enviar dados, anexos ou Documento de registro (DoR) a um processo de LiveCycle em vez de usar o [!UICONTROL Enviar para Forms Workflow]. (LC_WORKFLOW_SUBMmission)

* Procure notas de versão mensais para obter informações sobre a disponibilidade do recurso Comunicações interativas . Não migre suas Comunicações interativas, Cartas e dicionários relacionados para um ambiente Cloud Service até que o recurso não esteja disponível. (FP_PROFILE_INTERATIVE_COMMUNICATIONS)

* Desative a opção **[!UICONTROL Salvar como rascunho]** e **[!UICONTROL Ativar salvamento automático]** no Adaptive Forms antes de migrá-los para o Cloud Service. Você pode ativar essas opções depois que o recurso Portal do Forms for lançado para o Cloud Service. Procure notas de versão mensais para obter informações sobre a disponibilidade dos recursos. (RASCUNHO_AUTO_SAVE, RASCUNHO_SAVE)

* Não há substituição para opção de metadados. Remova-o de seus formulários antes de migrá-los para o Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Use o Google reCaptcha em vez do serviço CAPTCHA fornecido pela Adobe Experience Manager. (FORMS_CAPTCHA)

* O Adaptive Forms oferece um design responsivo. Esses formulários alteram a aparência, o design e a interatividade com base no dispositivo subjacente. Você pode continuar usando o Adaptive Forms em dispositivos móveis. Procure notas de versão mensais para obter informações sobre a disponibilidade do aplicativo [!DNL AEM Forms]. (AEM_FORMS_APP)

* Não migre um modelo de Fluxo de trabalho AEM que use uma etapa do Fluxo de trabalho dos Serviços de documento. Além disso, não migre ou atualize o Adaptive Forms que envie dados do usuário para um Modelo de fluxo de trabalho que use as etapas do fluxo de trabalho dos serviços de documento ou altere a ação de envio para [compatível](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html) antes de migrar o formulário. (WORKFLOW_DOCSERVICES)

* O suporte para Forms adaptável baseado em XFA não está disponível imediatamente. Se você pretende usar o Forms adaptável baseado em XFA, entre em contato com o Suporte ao Adobe com detalhes do caso de uso e requisitos específicos.(XFA_BASED_FORM, XDP_BASED_FORM)

Entre em contato com [Adobe Support](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
