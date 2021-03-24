---
title: LUI
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 4%

---


# LUI {#lui}

Interface do usuário herdada

## Segundo plano {#background}

`LUI` O identifica o uso de elementos obsoletos da interface do usuário que não são recomendados ou não são compatíveis em versões posteriores do AEM e no AEM como Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de elementos da interface do usuário que devem ou devem ser atualizados:

* `legacy.dialog.classic`: As caixas de diálogo da interface clássica com base em ExtJS devem ser alteradas para Coral.
   * Isso é detectado quando o nome da caixa de diálogo é &quot;dialog&quot; ou &quot;design_dialog&quot; e quando
o valor da propriedade `jcr:primaryType` ou o valor da propriedade `xtype` é &quot;cq:Dialog&quot;.
* `legacy.dialog.coral2`: As caixas de diálogo do Coral 2 devem ser atualizadas para usar o Coral 3.
   * Isso é detectado quando a caixa de diálogo e seus nomes de nó de conteúdo filho são &quot;cq:dialog/content&quot;,
&quot;cq:design_dialog/content&quot;, &quot;cq:dialog.coral2/content&quot; ou &quot;cq:design_dialog.coral2/content&quot;
e o valor da propriedade `sling:resourceType` não contém
&quot;granite/ui/components/coral/foundation&quot;.
* `legacy.custom.component`: Os componentes herdados de  `foundation/components` devem ser atualizados para usar os Componentes principais.
   * Isso é detectado quando o valor da propriedade `jcr:primaryType` é &quot;cq:Component&quot; e a variável
      `sling:resourceSuperType` o valor da propriedade contém &quot;foundation/components&quot; ou qualquer um dos
      `sling:resourceSuperType` Os valores da propriedade da cadeia de componentes de supertipo contêm &quot;foundation/components&quot;.
* `legacy.static.template`: Modelos estáticos devem ser atualizados para Modelos editáveis.
   * Isso é detectado quando o valor da propriedade `jcr:primaryType` é &quot;cq:Template&quot;.

## Possíveis implicações e riscos {#implications-and-risks}

* A interface clássica não está mais disponível no AEM como Cloud Service. A interface padrão para criação é a interface habilitada para toque.
* Confiar em componentes personalizados herdados pode aumentar os custos de manutenção ao longo do tempo.

## Possíveis soluções {#solutions}

* Utilize [AEM conjunto de ferramentas de Modernização](https://opensource.adobe.com/aem-modernize-tools/) para reduzir o esforço necessário para modernizar suas implementações do AEM Sites. Essas ferramentas incluem a conversão de:
   * Caixas de diálogo clássicas (ExtJS) para caixas de diálogo de coral
   * Componentes básicos em componentes principais
   * Modelos estáticos e Controle de coluna para modelos editáveis e grade responsiva
   * Desenhos e caixas de diálogo de design para políticas de modelos editáveis
* Revise a biblioteca de componentes personalizados do seu projeto e faça a transição, se possível, para o conjunto de [Componentes principais](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=pt-BR) padronizados para acelerar o tempo de desenvolvimento e reduzir o custo de manutenção de seus aplicativos.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
