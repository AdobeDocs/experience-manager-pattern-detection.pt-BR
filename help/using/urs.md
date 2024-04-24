---
title: URS
description: Página de ajuda do código do Detector de padrões.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 53%

---

# URS {#urs}

Estrutura de repositório não compatível

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Estrutura de repositório não compatível"
>abstract="O código URS identifica casos de estrutura de repositório e características de nó não compatíveis. Essas informações são exibidas para evitar conflitos entre o código de produto do AEM e o código de cliente, conteúdo que está sendo reestruturado da pasta /etc para outras pastas no repositório e muito mais."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Reestruturação do repositório"

## Segundo plano {#background}

`URS`  Identifica casos de estrutura de repositório e características de nó não compatíveis. A partir do AEM 6.4, foram fornecidas orientações para a reestruturação do conteúdo de repositórios. Ao definir claramente hierarquias para código de produto do AEM e código de cliente e evitar conflitos entre elas, o conteúdo está sendo reestruturado da pasta `/etc` para outras pastas no repositório, seguindo as seguintes regras de alto nível:

* O código do produto AEM é sempre colocado em `/libs`, que não deve ser substituído pelo código personalizado.
* O código personalizado deve ser colocado em `/apps`, `/content`, e `/conf`.
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
* Pacotes contendo conteúdo mutável e imutável provavelmente podem causar problemas durante a implantação.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Diretrizes de implementação"
>abstract="A prática recomendada é revisar o projeto de código. Certifique-se de que ele siga as diretrizes de estrutura do projeto AEM e evite que o código dependa de caminhos de repositório mais antigos/não compatíveis que possam causar comportamento indesejado no AEM as a Cloud Service. Entre em contato com o Suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="Diretrizes de estrutura de projetos do AEM"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Consulte [Reestruturação do repositório](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring) para orientação sobre como se preparar para o AEM as a Cloud Service.
* Consulte também [Estrutura de projeto do AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) se quiser saber mais sobre áreas mutáveis e imutáveis do repositório.
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html?lang=pt-BR) esclarecimentos ou de ter preocupações em conta.
* Use o [Modernizador de repositório](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools) reestruturar pacotes de projetos existentes separando o conteúdo e o código em pacotes discretos para serem compatíveis com a estrutura do projeto definida para o Adobe Experience Manager as a Cloud Service.
