---
title: URS
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# URS {#urs}

Estrutura de Repositório Não Suportada

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

* Consulte [Reestruturação de Repositório](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) para obter orientação sobre como preparar para AEM como Cloud Service.
* Consulte também [AEM Estrutura do Projeto](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) para saber mais sobre áreas mutáveis e imutáveis do repositório.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
* Aproveite o [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools) para reestruturar pacotes de projetos existentes separando conteúdo e código em pacotes discretos para serem compatíveis com a estrutura do projeto definida para o Adobe Experience Manager como um Cloud Service.