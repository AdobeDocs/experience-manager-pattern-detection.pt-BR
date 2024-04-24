---
title: INST
description: Página de ajuda do código do Detector de padrões.
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 72%

---

# INST {#inst}

Artefato instalado

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Artefato instalado"
>abstract="O código INST identifica pacotes e conjuntos personalizados e de terceiros que foram instalados no AEM pelo cliente. Eles são relatados para ajudar a caracterizar o estado do sistema como o escopo geral de um esforço de atualização. Qualquer pacote de terceiros deve respeitar as diretrizes de desenvolvimento e pacotes do AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Diretrizes de desenvolvimento - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package" text="Diretrizes de pacotes - AEM as a Cloud Service"

`INST`  Identifica pacotes e conjuntos personalizados e de terceiros que foram instalados no AEM pelo cliente. Eles são relatados para ajudar a caracterizar o estado do sistema como o escopo geral de um esforço de atualização.

Quando várias versões de um pacote tiverem sido instaladas, somente a versão mais recente será relatada.

Os pacotes e conjuntos detectados não necessariamente foram otimizados para o AEM as a Cloud Service. Qualquer pacote de terceiros deve ser verificado com seu criador ou com a Adobe para compatibilidade com o AEM as a Cloud Service.

Os subtipos são usados para identificar diferentes tipos de informações:

* `custom.bundle`: um pacote que foi instalado no AEM.
* `custom.package`: um pacote que foi instalado no AEM.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Diretrizes de implementação"
>abstract="Os clientes não podem mais instalar pacotes de terceiros usando o Gerenciador de pacotes do CRX. Os clientes devem revisar esses artefatos instalados que devem ser estruturados e otimizá-los para funcionar com o AEM as a Cloud Service. Verifique qualquer pacote de terceiros com seu criador ou com Adobe para compatibilidade com o AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embeddeds" text="Incorporação de subpacotes no pacote de contêiner"


* Não é possível instalar pacotes de terceiros usando o Gerenciador de pacotes do CRX no AEM as a Cloud Service.
* Os aplicativos dependentes de pacotes de terceiros podem não funcionar conforme esperado até serem implantados corretamente para funcionar com o AEM as a Cloud Service.
* Pacotes de fornecedores de terceiros, quando não otimizados para o AEM as a Cloud Service, podem resultar em comportamento indesejado.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Ferramentas e recursos"
>abstract="Analise o projeto herdado WKND para entender como as violações do INST podem ser compatíveis com o AEM Cloud Service. Além disso, analise o exemplo de violação do INST no GitHub para entender como isso pode ser corrigido e implantado no AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="Projeto herdado WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Exemplo de violação de INST - GitHub"

* Os pacotes de terceiros devem ser implantados no AEM como parte do projeto usando o [processo de implantação](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deployment-process) do Cloud Manager.
* Revise como [incorporar pacotes de terceiros](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embedding-3rd-party-packages) no seu projeto para o AEM as a Cloud Service.
* Os pacotes de terceiros devem aderir às orientações de [desenvolvimento](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines) e [embalagem](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package) do AEM as a Cloud Service.
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) e entenda como as [violações do INST](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) podem ser corrigidas e compatíveis com o AEM as a Cloud Service.
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) esclarecimentos ou de ter preocupações em conta.
