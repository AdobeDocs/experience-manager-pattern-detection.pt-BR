---
title: INST
description: Página de ajuda do código do Detector de padrões
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# INST {#inst}

Artefato Instalado

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Artefato Instalado"
>abstract="O INST identifica pacotes e pacotes personalizados e de terceiros que foram instalados no AEM pelo cliente. Elas são relatadas para ajudar a caracterizar o estado do sistema como o escopo geral de um esforço de atualização. Qualquer pacote de terceiros deve seguir o AEM como diretrizes de desenvolvimento e embalagem de Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="Diretrizes de desenvolvimento - AEM como um Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html" text="Diretrizes de pacotes - AEM como um Cloud Service"

`INST` O identifica pacotes e pacotes personalizados e de terceiros que foram instalados no AEM pelo cliente. Elas são relatadas para ajudar a caracterizar o estado do sistema como o escopo geral de um esforço de atualização.

Quando várias versões de um pacote tiverem sido instaladas, somente a versão mais recente será relatada.

Os pacotes e pacotes detectados não foram necessariamente otimizados para AEM como Cloud Service. Qualquer pacote de terceiros deve ser verificado com seu criador ou Adobe para verificar a compatibilidade com o AEM como Cloud Service.

Os subtipos são usados para identificar diferentes tipos de informações:

* `custom.bundle`: Um pacote que foi instalado no AEM.
* `custom.package`: Um pacote que foi instalado no AEM.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Diretrizes de implementação"
>abstract="Os clientes não podem mais instalar pacotes de terceiros usando o Gerenciador de Pacotes do CRX. Os clientes devem analisar esses artefatos instalados e precisam ser estruturados e otimizá-los para trabalhar com o AEM como Cloud Service. Qualquer pacote de terceiros deve ser verificado com seu criador ou Adobe para verificar a compatibilidade com o AEM como Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embeddeds" text="Incorporação de subpacotes no pacote de contêiner"


* A instalação de pacotes de terceiros usando o Gerenciador de pacotes do CRX não é possível no AEM como um Cloud Service.
* Os aplicativos dependentes de pacotes de terceiros podem não funcionar conforme esperado até serem implantados corretamente para funcionar com o AEM como um Cloud Service.
* Pacotes de fornecedores de terceiros, se não otimizados para o AEM as a Cloud Service, podem resultar em comportamento indesejado.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Ferramentas e recursos"
>abstract="Revise o projeto herdado WKND para entender como as violações do INST podem ser tornadas compatíveis com AEM Cloud Service. Além disso, analise o exemplo de violação do INST no Github para entender como isso pode ser corrigido e implantado no AEM como um Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="Projeto WKND-Legacy"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Exemplo de violação INST - Github"

* Os pacotes de terceiros devem ser implantados no AEM como parte do projeto usando o [processo de implantação](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html#deployment-process) do Cloud Manager.
* Analise como [incorporar pacotes de terceiros](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embedding-3rd-party-packages) em seu projeto para AEM como um Cloud Service.
* Os pacotes de terceiros devem aderir ao AEM como diretrizes Cloud Service [development](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) e [packaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) e entenda como [violações INST](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) podem ser corrigidas e tornadas compatíveis com AEM como um Cloud Service.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
