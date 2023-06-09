---
title: URS
description: Página de ajuda de códigos do detector de padrões
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 100%

---

# URS {#urs}

Estrutura de repositório não compatível

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Estrutura de repositório não compatível"
>abstract="O código URS identifica casos de estrutura de repositório e características de nó não compatíveis. Essas informações são exibidas para evitar conflitos entre o código de produto do AEM e o código de cliente, conteúdo que está sendo reestruturado da pasta /etc para outras pastas no repositório e muito mais."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html?lang=pt-BR" text="Reestruturação do repositório"

## Segundo plano {#background}

O código `URS` identifica casos de estrutura de repositório e características de nó não compatíveis. A partir do AEM 6.4, foram fornecidas orientações para a reestruturação do conteúdo de repositórios. Ao definir claramente hierarquias para código de produto do AEM e código de cliente e evitar conflitos entre elas, o conteúdo está sendo reestruturado da pasta `/etc` para outras pastas no repositório, seguindo as seguintes regras de alto nível:

* O código de produto do AEM sempre será colocado em `/libs`, que não deve ser substituído por código personalizado.
* Códigos personalizados devem ser colocados em `/apps`, `/content` e `/conf`.
* O AEM as a Cloud Service não é compatível com nomes de nó longos (>150 bytes).
* É altamente recomendável que essas diretrizes sejam seguidas para o AEM as a Cloud Service.

Os subtipos são usados para identificar tipos específicos de problemas de repositório que devem ser abordados:
* `clientlibs.location`: uma biblioteca do cliente que faz referência a `/etc` por caminho.
* `file.location`: um arquivo em `/etc` que foi modificado desde a instalação.
* `node.location`: um nó em `/etc` que foi modificado desde a instalação.
* `workflow.location`: um modelo de fluxo de trabalho ou iniciador em `/etc/workflow`.
* `package.structure`: um pacote que contém conteúdo mutável e imutável.
* `node.name.length`: um nome de nó com comprimento não compatível.
* `node.size`: um nó com tamanho não compatível.

## Possíveis implicações e riscos {#implications-and-risks}

* Códigos personalizados que dependem de caminhos mais antigos podem causar comportamento indesejado e afetar a funcionalidade do produto.
* Pacotes contendo conteúdo mutável e imutável provavelmente causarão problemas durante a implantação.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar seu projeto de código e garantir que ele siga as diretrizes de estrutura do projeto do AEM e evitar que o código dependa de caminhos de repositório mais antigos/não compatíveis que possam causar comportamento indesejado no AEM as a Cloud Service. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=pt-BR" text="Diretrizes de estrutura de projetos do AEM"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Consulte [Reestruturação do repositório](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html?lang=pt-BR) para obter orientação sobre como se preparar para o AEM as a Cloud Service.
* Consulte também [Estrutura de projeto do AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=pt-BR) para saber mais sobre áreas mutáveis e imutáveis do repositório.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
* Aproveite o [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html?lang=pt-BR#refactoring-tools) para reestruturar pacotes de projetos existentes separando o conteúdo e o código em pacotes discretos para serem compatíveis com a estrutura do projeto definida para o Adobe Experience Manager as a Cloud Service.
