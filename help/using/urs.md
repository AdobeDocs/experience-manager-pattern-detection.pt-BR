---
title: URS
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 100%

---

# URS {#urs}

Estrutura de repositório não compatível

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Estrutura de repositório não compatível"
>abstract="URS identifica casos de URS (Estrutura de repositório não compatível) e características de nós. Essas informações são exibidas para evitar conflitos entre o código de produto do AEM e o código do cliente, conteúdo que está sendo reestruturado de `/etc` para outras pastas no repositório e mais."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Reestruturação do repositório"

## Fundo {#background}

`URS` identifica casos de URS (Estrutura de repositório não compatível) e características de nó. A partir do AEM 6.4, foram fornecidas orientações para a reestruturação do conteúdo de repositórios. Ao definir claramente hierarquias para o código de produto do AEM e para o código do cliente, evitando assim conflitos, o conteúdo é reestruturado de `/etc` para outras pastas no repositório. Ao fazer isso, siga as seguintes regras de nível superior:

* O código do produto do AEM sempre será colocado em `/libs` e códigos personalizados não podem substituí-lo.
* Códigos personalizados devem ser colocados em `/apps`, `/content` e `/conf`.
* É altamente recomendável que essas diretrizes sejam seguidas para o AEM as a Cloud Service.

Os subtipos são usados para identificar tipos específicos de problemas de repositório que devem ser abordados:

* `clientlibs.location`: uma biblioteca do cliente que faz referência a `/etc` por caminho.
* `file.location`: um arquivo em `/etc` que foi modificado desde a instalação.
* `node.location`: um nó em `/etc` que foi modificado desde a instalação.
* `workflow.location`: um modelo de fluxo de trabalho ou iniciador em `/etc/workflow`.
* `package.structure`: um pacote que contém conteúdo mutável e imutável.
* `node.size`: um nó com tamanho não compatível.

## Possíveis implicações e riscos {#implications-and-risks}

* Códigos personalizados que dependem de caminhos mais antigos podem causar comportamento indesejado e afetar a funcionalidade do produto.
* Pacotes com conteúdo mutável e imutável provavelmente causarão problemas durante a implantação.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar o projeto de código. Certifique-se de que esteja em conformidade com as diretrizes de estrutura de projetos do AEM e evite que o código dependa de caminhos de repositório mais antigos/incompatíveis e que possam causar comportamento indesejado no AEM as a Cloud Service. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="Diretrizes de estrutura de projetos do AEM"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Consulte [Reestruturação do repositório](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring) para obter orientações sobre como se preparar para o AEM as a Cloud Service.
* Consulte, também, a [Estrutura de projetos do AEM](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) para saber mais sobre as áreas mutáveis e imutáveis do repositório.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
* Utilize o [Modernizador de repositório](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools) para reestruturar pacotes de projetos, separando o conteúdo e o código em pacotes diferentes, de modo que sejam compatíveis com a estrutura do projeto definida para o Adobe Experience Manager as a Cloud Service.
