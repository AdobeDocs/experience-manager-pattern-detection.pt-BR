---
title: Forms
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: a6ba6e93c89644160650882ecbf17028bec35068
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---


# [!DNL FORMS] {#forms}

[!DNL Adobe Experience Manager Forms]

## Segundo plano {#background}

`FORMS` identifica possíveis problemas relacionados à migração do Adobe Experience Manager Forms para o Adobe Experience Manager Forms as a Cloud Service. Resolva esses problemas antes de migrar para o Cloud Service.

Os subtipos a seguir ajudam a identificar os diferentes tipos de problemas:

* `modified.feature`: Esses recursos, ativos ou APIs foram atualizados ou modificados para o Cloud Service. Antes de migrar para o Cloud Service, execute o utilitário de migração para tornar esses recursos e ativos compatíveis com o Cloud Service.
* `unavailable.feature`: Seu ambiente tem recursos e ativos que não estão disponíveis ou removidos do Cloud Service. Não migre esses recursos ou ativos para um ambiente Cloud Service.
* `unsupported.feature`: Seu ambiente usa alguns recursos ainda não suportados no Cloud Service. Não migre esses recursos ou ativos para um ambiente Cloud Service. Fique de olho nas notas de versão mensais para ver a disponibilidade dos recursos.
* `unsupported.api`: Seu ambiente tem algumas APIs ainda não compatíveis no Cloud Service. Antes de migrar para o Cloud Service, desative, substitua ou remova essas APIs do seu código. Fique de olho nas notas de versão mensais para ver a disponibilidade dos recursos.

Consulte as seções [Possíveis implicações e riscos](#implications-and-risks) e [Possíveis soluções](#solutions) para obter informações sobre substituições e outras ações necessárias para tornar alguns recursos e APIs compatíveis com o Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

Resolva os seguintes problemas, antes de migrar para o Adobe Experience Manager Forms as a Cloud Service. Quando as implicações e os riscos listados abaixo não são abordados, alguns recursos não funcionam como esperado no ambiente do Cloud Service.

* A funcionalidade do editor de códigos do recurso do editor de regras não está disponível. (CODE_EDITOR)

* Por padrão, o suporte de email (porta SMTP) está desativado. (EMAIL_SERVICE_CONFIGURATION)

* A ação de envio **[!UICONTROL Email PDF]** não está disponível.(EMAIL_PDF_SUBMIT_ACTION)

* Formulários adaptáveis baseados em XDP ainda não são compatíveis. (XDP_BASED_FORM)

* Uma ação de envio é invocada imediatamente no envio do formulário, em vez de esperar que todos os signatários concluam a assinatura. Portanto, o documento de assinatura do formulário adaptável (PDF do contrato Adobe Sign enviado aos signatários) não está disponível para envio de ações a serem usadas ou processadas. (FORM_SIGN_INTEGRATION)

* A etapa Assinatura não está disponível. (SIGNATURE_STEP)

* A etapa Verificar não está disponível. (VERIFY_STEP)

* O recurso do Portal Forms e **[!UICONTROL Ação de envio do Portal Forms]** não estão disponíveis. Não é possível usar o Forms Portal para listar formulários, salvar rascunhos ou mostrar formulários enviados. Não é possível enviar (usar **[!UICONTROL O Portal do Forms enviar dados de ação]** ) enviados para um formulário adaptável para um Portal do Forms. [!UICONTROL No momento, os recursos de formulário adaptável Salvar como ] rascunho e   Salvar automaticamente não são suportados. (FORMS_PORTAL_SUBMmission, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* A ação de envio **[!UICONTROL Enviar para o Forms workflow]** não está disponível. No AEM 6.5 Forms e versões anteriores, a ação de envio foi usada para enviar dados de formulário adaptáveis ao AEM Forms herdado em fluxos de trabalho e LiveCycles Workflow JEE. (LC_WORKFLOW_SUBMmission)

* O recurso Comunicações interativas não está disponível.  (FP_PROFILE_INTERATIVE_COMMUNICATIONS).

* **[!UICONTROL No momento, os recursos de formulário adaptável Salvar como]** rascunho e  **** Salvar automaticamente não são suportados. (RASCUNHO_AUTO_SAVE, RASCUNHO_SAVE)

* A opção Metadados não está disponível. (METADATA_ACCORDION_FORM_CONTAINER)

* O componente CAPTCHA agora usa o serviço Google reCAPTCHA para validar CAPTCHA, por padrão. A opção de usar o Adobe Experience Manager para validar CAPTCHA não está disponível. (FORMS_CAPTCHA)

## Possíveis soluções {#solutions}

* Use o utilitário de migração para converter todos os scripts de regras em seu ambiente em funções reutilizáveis. Você pode usar as funções reutilizáveis com o Editor de regras visuais para continuar obtendo resultados obtidos com scripts de regras. (CODE_EDITOR)

* Entre em contato com a equipe de suporte para ativar a funcionalidade de email (abrir Porta SMTP) para seu ambiente. Por padrão, somente as conexões HTTP e HTTPS de saída são ativadas. (EMAIL_SERVICE_CONFIGURATION)

* Use **[!UICONTROL Enviar ação por email]** em vez de **[!UICONTROL Enviar PDF por email]**. A ação de envio **[!UICONTROL Email]** fornece opções para enviar anexos e anexar Documento de registro (DoR) com email. (EMAIL_PDF_SUBMIT_ACTION)

* Não migre formulários adaptáveis baseados em XDP para um ambiente Cloud Service. Fique de olho nas notas de versão mensais para ver a disponibilidade dos recursos. (XDP_BASED_FORM)

* Os dados enviados contêm a ID do contrato de assinatura. Você pode usar a ID do contrato de assinatura para recuperar um PDF do contrato de assinatura, se necessário.  (FORM_SIGN_INTEGRATION)

* Substitua a etapa Assinatura em seus formulários adaptáveis pela opção Assinar um formulário adaptável após o envio, na mesma janela. Ajuda a continuar fornecendo uma [experiência de assinatura no navegador](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). (SIGNATURE_STEP)

* Remova a etapa de verificação dos formulários adaptáveis existentes antes de movê-los para um ambiente Cloud Service. (VERIFY_STEP)

* Não há alternativa para **[!UICONTROL ação de envio do Portal Forms]**. Você pode usar essa ação de envio depois que o recurso Portal do Forms for lançado para o Cloud Service. Fique de olho nas notas de versão mensais para ver a disponibilidade dos recursos. (FORMS_PORTAL_SUBMmission, FORMS_PORTAL)

* Não há uma ação de envio alternativa para **[!UICONTROL Enviar para o fluxo de trabalho do Forms]** enviar ações. Você pode desenvolver uma ação de envio personalizada para enviar dados, anexos ou Documento de registro (DoR) para um processo do LiveCycle. (LC_WORKFLOW_SUBMmission)

* Não migre suas Comunicações interativas, Cartas e Dicionários relacionados para um ambiente Cloud Service. (FP_PROFILE_INTERATIVE_COMMUNICATIONS)

* Desative a opção **[!UICONTROL Salvar como rascunho]** e **[!UICONTROL Ativar Salvar automaticamente]** em seus formulários adaptáveis antes de migrá-los para o Cloud Service. Você pode ativar essas opções depois que o recurso Portal do Forms for lançado para o Cloud Service. Fique de olho nas notas de versão mensais para ver a disponibilidade dos recursos. (RASCUNHO_AUTO_SAVE, RASCUNHO_SAVE)

* Não há substituição para opção de metadados. Remova-o de seus formulários antes de migrá-los para o Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Use o Google reCaptcha em vez do serviço CAPTCHA fornecido pela Adobe Experience Manager. (FORMS_CAPTCHA)

Entre em contato com [Adobe Support](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
