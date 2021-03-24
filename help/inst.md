---
title: INST
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---


# INST {#inst}

Artefato Instalado

## Segundo plano {#background}

`INST` O identifica pacotes e pacotes personalizados e de terceiros que foram instalados no AEM pelo cliente. Elas são relatadas para ajudar a caracterizar o estado do sistema como o escopo geral de um esforço de atualização.

Quando várias versões de um pacote tiverem sido instaladas, somente a versão mais recente será relatada.

Os pacotes e pacotes detectados não foram necessariamente otimizados para AEM como Cloud Service. Qualquer pacote de terceiros deve ser verificado com seu criador ou Adobe para verificar a compatibilidade com o AEM como Cloud Service.

Os subtipos são usados para identificar diferentes tipos de informações:

* `custom.bundle`: Um pacote que foi instalado no AEM.
* `custom.package`: Um pacote que foi instalado no AEM.

## Possíveis implicações e riscos {#implications-and-risks}

* A instalação de pacotes de terceiros usando o Gerenciador de pacotes do CRX não é possível no AEM como um Cloud Service.
* Os aplicativos dependentes de pacotes de terceiros podem não funcionar conforme esperado até serem implantados corretamente para funcionar com o AEM como um Cloud Service.
* Pacotes de fornecedores de terceiros, se não otimizados para o AEM as a Cloud Service, podem resultar em comportamento indesejado.

## Possíveis soluções {#solutions}

* Os pacotes de terceiros devem ser implantados no AEM como parte do projeto usando o [processo de implantação](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html#deployment-process) do Cloud Manager.
* Analise como [incorporar pacotes de terceiros](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embedding-3rd-party-packages) em seu projeto para AEM como um Cloud Service.
* Os pacotes de terceiros devem aderir ao AEM como diretrizes Cloud Service [development](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) e [packaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html).
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) e entenda como [violações INST](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) podem ser corrigidas e tornadas compatíveis com AEM como um Cloud Service.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
