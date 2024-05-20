---
title: LUI
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 49%

---

# LUI {#lui}

Interface do usuário herdada

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Interface do usuário herdada"
>abstract="O código LUI identifica o uso de elementos obsoletos da interface do usuário. Esses elementos não são recomendados ou não são compatíveis em versões posteriores do AEM e do AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Alterações importantes: AEM as a Cloud Service"

`LUI`  Identifica o uso de elementos obsoletos da interface do usuário. Esses elementos não são recomendados ou não são compatíveis em versões posteriores do AEM e no AEM as a Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de elementos da interface que devem ou precisam ser atualizados:

* `legacy.dialog.classic`: as caixas de diálogo da interface clássica com base em ExtJS devem ser alteradas para Coral.
   * Este subtipo é detectado quando o nome da caixa de diálogo é `dialog` ou `design_dialog` e quando a variável `jcr:primaryType` valor da propriedade ou o `xtype` o valor da propriedade é `cq:Dialog`.
* `legacy.dialog.coral2`: as caixas de diálogo `Coral 2` devem ser atualizadas para usar `Coral 3`.
   * Esse subtipo é detectado quando a caixa de diálogo e seus nomes de nó de conteúdo filho são
      * `cq:dialog/content`,
      * `cq:design_dialog/content`,
      * `cq:dialog.coral2/content`,
      * ou `cq:design_dialog.coral2/content`
e a variável `sling:resourceType` o valor da propriedade não contém `granite/ui/components/coral/foundation`.
* `legacy.custom.component`: componentes herdados do `foundation/components` devem ser atualizados para usar os componentes principais.
   * Esse subtipo é detectado quando a variável `jcr:primaryType` o valor da propriedade é `cq:Component` e a variável
     `sling:resourceSuperType` o valor da propriedade contém &quot;foundation / components&quot;. Ou, quando qualquer um dos
     `sling:resourceSuperType` os valores de propriedade da cadeia de componentes de supertipo contêm &quot;foundation / components&quot;.
* `legacy.static.template`: modelos estáticos devem ser atualizados para Modelos editáveis.
   * Esse subtipo é detectado quando a variável `jcr:primaryType` o valor da propriedade é `cq:Template`.
* `content.fragment.template`: os Modelos de fragmento de conteúdo devem criar modelos de fragmento para substituir os Modelos de fragmento.
   * Os modelos de fragmento de conteúdo podem ser encontrados nos seguintes locais:
      * Os modelos de fragmento de conteúdo prontos para uso são armazenados no `/libs/settings/dam/cfm/templates`
      * Eles podem ser sobrepostos no  `/apps/settings/dam/cfm/templates`  ou  `/conf/.../settings/dam/cfm/templates`(... = global ou “locatário”)
* `translation.dictionary`: `I18n` o dicionário que está presente em `/apps`.
   * `/apps` O é imutável no tempo de execução e o arquivo translator.html não estaria mais disponível no AEM as a Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Diretrizes de implementação"
>abstract="A interface clássica não está mais disponível no AEM as a Cloud Service e a interface padrão para criação é a interface habilitada para toque. A prática recomendada é mover todas as interfaces não compatíveis e as personalizações vinculadas devem ser refatoradas para recursos e funcionalidades mais recentes que sejam compatíveis com o AEM as a Cloud Service. Clientes podem usar o conjunto de modernização do AEM existente para reduzir o trabalho de modernização das implementações do AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Ferramentas de Modernização do AEM"

* A interface clássica não está mais disponível no AEM as a Cloud Service. A interface padrão para criação é a interface habilitada para toque.
* Depender de componentes personalizados herdados pode aumentar os custos de manutenção ao longo do tempo.
* Modelos de fragmento de conteúdo substituídos por modelos de fragmento de conteúdo no AEM 6.3. A migração de fragmentos de conteúdo baseados em modelos herdados para AEM as a Cloud Service retém esses fragmentos como funcionais, mas não é possível criar fragmentos com base no modelo herdado. Também não é possível entregar esses fragmentos usando o AEM GraphQL, que requer modelos de Fragmento de conteúdo como esquemas.
* /apps é imutável no tempo de execução e o arquivo translator.html não estaria mais disponível no AEM as a Cloud Service. Assim, `I18n` Os dicionários devem vir do Git por meio do pipeline de CI/CD.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Ferramentas e recursos"
>abstract="Com a ajuda do Conjunto de modernização do AEM, os clientes podem converter caixas de diálogo clássicas (ExtJS) em caixas de diálogo Coral. O objetivo é ajudar os clientes a migrar dos recursos não compatíveis ou herdados para as ofertas robustas e modernas do AEM. Essas ferramentas são configuráveis e extensíveis, e possuem reconhecimento de configuração. Além disso, explore a substituição de componentes personalizados pelo conjunto de componentes principais padronizados para acelerar o tempo de desenvolvimento e reduzir o custo de manutenção de seus aplicativos."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Conversor de componentes"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-core-components/using/introduction" text="Componentes principais"

* Para reduzir o esforço necessário para modernizar suas implementações do AEM Sites, use o [Conjunto de ferramentas de modernização do AEM](https://opensource.adobe.com/aem-modernize-tools/). Essas ferramentas incluem a conversão de:
   * Caixas de diálogo clássicas (ExtJS) para caixas de diálogo Coral
   * Componentes de base para Componentes principais
   * Modelos estáticos e controle de coluna para modelos editáveis e grade responsiva
   * Desenhos e caixas de diálogo de design para políticas de modelos editáveis
* Revise a biblioteca de componentes personalizados do seu projeto e faça a transição, se possível, para o conjunto de [Componentes principais](https://experienceleague.adobe.com/pt-br/docs/experience-manager-core-components/using/introduction) padronizados para acelerar o tempo de desenvolvimento e reduzir o custo de manutenção de seus aplicativos.
* Crie modelos de Fragmento de conteúdo com recursos equivalentes aos modelos herdados e use esses modelos para a criação de Fragmento de conteúdo no futuro. Consulte [Modelos de fragmentos de conteúdo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models) para mais detalhes.
* `I18n` Os dicionários devem vir do Git por meio do pipeline de CI/CD. [Documentação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
