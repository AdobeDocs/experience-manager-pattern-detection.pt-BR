---
title: LUI
description: Página de ajuda de códigos do detector de padrões
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: ht
source-wordcount: '554'
ht-degree: 100%

---

# LUI {#lui}

Interface do usuário herdada

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Interface do usuário herdada"
>abstract="O código LUI identifica o uso de elementos obsoletos da interface do usuário que não são recomendados ou não são compatíveis em versões posteriores do AEM e do AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=pt-BR" text="Alterações importantes no AEM as a Cloud Service"

O código `LUI` identifica o uso de elementos obsoletos da interface do usuário que não são recomendados ou não são compatíveis em versões posteriores do AEM e do AEM as a Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de elementos da interface do usuário que devem ou precisam ser atualizados:

* `legacy.dialog.classic`: as caixas de diálogo da interface clássica com base em ExtJS devem ser alteradas para Coral.
   * Isso é detectado quando o nome da caixa de diálogo é &quot;dialog&quot; ou &quot;design_dialog&quot; e quando 
o valor da propriedade `jcr:primaryType` ou o valor da propriedade `xtype` é &quot;cq:Dialog&quot;.
* `legacy.dialog.coral2`: as caixas de diálogo do Coral 2 devem ser atualizadas para usar o Coral 3.
   * Isso é detectado quando a caixa de diálogo e seus nomes de nó de conteúdo filho são &quot;cq:dialog/content&quot;, 
&quot;cq:design_dialog/content&quot;, &quot;cq:dialog.coral2/content&quot; ou &quot;cq:design_dialog.coral2/content&quot;
e o valor da propriedade `sling:resourceType` não contém &quot;granite/ui/components/coral/foundation&quot;.
* `legacy.custom.component`: componentes herdados de `foundation/components`, devem ser atualizados para usar os Componentes principais.
   * Isso é detectado quando o valor da propriedade `jcr:primaryType` é &quot;cq:Component&quot; e o
      o valor da propriedade `sling:resourceSuperType` contém &quot;foundation/components&quot; ou qualquer um dos
      os valores de propriedade `sling:resourceSuperType` da cadeia de componentes de supertipo contêm &quot;foundation/components&quot;.
* `legacy.static.template`: Modelos estáticos, devem ser atualizados para Modelos editáveis.
   * Isso é detectado quando o valor da propriedade `jcr:primaryType` é &quot;cq:Template&quot;.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Diretrizes de implementação"
>abstract="A interface clássica não está mais disponível no AEM as a Cloud Service e a interface padrão para criação é a interface habilitada para toque. A prática recomendada é mover todas as interfaces não compatíveis e as personalizações vinculadas devem ser refatoradas para recursos/funcionalidades mais recentes que sejam compatíveis com o AEM as a Cloud Service. Os clientes podem aproveitar o Conjunto de modernização do AEM existente para ajudar a reduzir o esforço necessário para modernizar as implementações do AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Ferramentas de Modernização do AEM"

* A interface clássica não está mais disponível no AEM as a Cloud Service. A interface padrão para criação é a interface habilitada para toque.
* Depender de componentes personalizados herdados pode aumentar os custos de manutenção ao longo do tempo.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Ferramentas e recursos"
>abstract="Com a ajuda do Conjunto de modernização do AEM, os clientes podem converter caixas de diálogo clássicas (ExtJS) em caixas de diálogo Coral. O objetivo é ajudar os clientes a migrar dos recursos não compatíveis ou herdados para as ofertas robustas e modernas do AEM. Essas ferramentas são configuráveis, com reconhecimento de configuração e extensíveis. Além disso, explore a substituição de componentes personalizados pelo conjunto de componentes principais padronizados para acelerar o tempo de desenvolvimento e reduzir o custo de manutenção de seus aplicativos."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/component.html" text="Conversor de componentes"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=pt-BR" text="Componentes principais"

* Utilizar o [Conjunto de ferramentas de modernização do AEM](https://opensource.adobe.com/aem-modernize-tools/) para reduzir o esforço necessário para modernizar suas implementações do AEM Sites. Essas ferramentas incluem a conversão de:
   * Caixas de diálogo clássicas (ExtJS) para caixas de diálogo Coral
   * Componentes de base para Componentes principais
   * Modelos estáticos e controle de coluna para modelos editáveis e grade responsiva
   * Desenhos e caixas de diálogo de design para políticas de modelos editáveis
* Revise a biblioteca de componentes personalizados do seu projeto e faça a transição, se possível, para o conjunto de [Componentes principais](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=pt-BR) padronizados para acelerar o tempo de desenvolvimento e reduzir o custo de manutenção de seus aplicativos.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
