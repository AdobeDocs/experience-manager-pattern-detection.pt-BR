---
title: URS
description: Página de ajuda do código do Detector de padrões
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# URS {#urs}

Estrutura de Repositório Não Suportada

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Estrutura de Repositório Não Suportada"
>abstract="O URS identifica casos de estrutura de repositório não suportada. Essas informações são exibidas para evitar conflitos entre AEM código de produto e código de cliente, conteúdo que está sendo reestruturado de /etc para outras pastas no repositório e muito mais."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html" text="Reestruturação do Repositório"

## Segundo plano {#background}

`URS` identifica casos de estrutura de repositório não suportada. A partir do AEM 6.4, foram fornecidas orientações para a reestruturação do conteúdo dos repositórios. Ao definir claramente hierarquias para AEM código de produto e código de cliente e evitar conflitos entre elas, o conteúdo está sendo reestruturado de `/etc` para outras pastas no repositório, seguindo as seguintes regras de alto nível:

* AEM código de produto sempre será colocado em `/libs`, que não deve ser substituído por código personalizado O código personalizado deve ser colocado em `/apps`, `/content` e `/conf`.
* É altamente recomendável que essas diretrizes sejam seguidas para AEM como um Cloud Service.

Os subtipos são usados para identificar tipos específicos de problemas de repositório que devem ser abordados:
* `clientlibs.location`: Uma biblioteca do cliente que faz referência  `/etc` por caminho.
* `file.location`: Um arquivo no  `/etc` que foi modificado desde a instalação.
* `node.location`: Um nó no  `/etc` que foi modificado desde a instalação.
* `workflow.location`: Um modelo de fluxo de trabalho ou iniciador em  `/etc/workflow`.
* `package.structure`: Um pacote que contém conteúdo mutável e imutável.

## Possíveis implicações e riscos {#implications-and-risks}

* O código personalizado que depende de caminhos mais antigos pode causar comportamento indesejado e afetar a funcionalidade do produto.
* Pacotes contendo conteúdo mutável e imutável provavelmente causarão problemas durante a implantação.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar seu projeto de código e garantir que ele siga as diretrizes de estrutura do projeto AEM e evitar que o código dependa de caminhos de repositório mais antigos/não compatíveis que possam causar comportamento indesejado no AEM como Cloud Service. Entre em contato com o Suporte do Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html" text="Diretrizes de estrutura do projeto AEM"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Suporte a Experience Cloud"

* Consulte [Reestruturação de Repositório](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) para obter orientação sobre como preparar para AEM como Cloud Service.
* Consulte também [AEM Estrutura do Projeto](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) para saber mais sobre áreas mutáveis e imutáveis do repositório.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
* Aproveite o [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools) para reestruturar pacotes de projetos existentes separando conteúdo e código em pacotes discretos para serem compatíveis com a estrutura do projeto definida para o Adobe Experience Manager como um Cloud Service.
