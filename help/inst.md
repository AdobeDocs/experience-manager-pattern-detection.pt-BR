---
title: INST
description: Página de ajuda de códigos do detector de padrões
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: ht
source-wordcount: '523'
ht-degree: 100%

---

# INST {#inst}

Artefato instalado

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Artefato instalado"
>abstract="O código INST identifica pacotes e conjuntos personalizados e de terceiros que foram instalados no AEM pelo cliente. Eles são relatados para ajudar a caracterizar o estado do sistema como o escopo geral de um esforço de atualização. Qualquer pacote de terceiros deve respeitar as diretrizes de desenvolvimento e pacotes do AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=pt-BR" text="Diretrizes de desenvolvimento - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html?lang=pt-BR" text="Diretrizes de pacotes - AEM as a Cloud Service"

O código `INST` identifica pacotes e conjuntos personalizados e de terceiros que foram instalados no AEM pelo cliente. Eles são relatados para ajudar a caracterizar o estado do sistema como o escopo geral de um esforço de atualização.

Quando várias versões de um pacote tiverem sido instaladas, somente a versão mais recente será relatada.

Os pacotes e conjuntos detectados não necessariamente foram otimizados para o AEM as a Cloud Service. Qualquer pacote de terceiros deve ser verificado com seu criador ou com a Adobe para compatibilidade com o AEM as a Cloud Service.

Os subtipos são usados para identificar diferentes tipos de informações:

* `custom.bundle`: um pacote que foi instalado no AEM.
* `custom.package`: um pacote que foi instalado no AEM.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Diretrizes de implementação"
>abstract="Os clientes não podem mais instalar pacotes de terceiros usando o Gerenciador de pacotes do CRX. Os clientes devem revisar esses artefatos instalados e precisam estruturá-los e otimizá-los para funcionar com o AEM as a Cloud Service. Qualquer pacote de terceiros deve ser verificado com seu criador ou com a Adobe para compatibilidade com o AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=pt-BR#embeddeds" text="Incorporação de subpacotes no pacote de contêiner"


* Não é possível instalar pacotes de terceiros usando o Gerenciador de pacotes do CRX no AEM as a Cloud Service.
* Os aplicativos dependentes de pacotes de terceiros podem não funcionar conforme esperado até serem implantados corretamente para funcionar com o AEM as a Cloud Service.
* Pacotes de fornecedores de terceiros, quando não otimizados para o AEM as a Cloud Service, podem resultar em comportamento indesejado.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Ferramentas e recursos"
>abstract="Analise o projeto herdado WKND para entender como as violações do INST podem ser compatíveis com o AEM Cloud Service. Além disso, analise o exemplo de violação do INST no Github para entender como isso pode ser corrigido e implantado no AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="Projeto herdado WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Exemplo de violação de INST - Github"

* Os pacotes de terceiros devem ser implantados no AEM como parte do projeto usando o [processo de implantação](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html?lang=pt-BR#deployment-process) do Cloud Manager.
* Revise como [incorporar pacotes de terceiros](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=pt-BR#embedding-3rd-party-packages) no seu projeto para o AEM as a Cloud Service.
* Os pacotes de terceiros devem aderir às orientações de [desenvolvimento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=pt-BR) e [embalagem](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html?lang=pt-BR) do AEM as a Cloud Service.
* Revise o projeto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) e entenda como as [violações do INST](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) podem ser corrigidas e compatíveis com o AEM as a Cloud Service.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
