---
title: LUI
description: Página de ajuda referente ao código do detector de padrões.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 100%

---

# LUI {#lui}

Interface do usuário herdada

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Interface do usuário herdada"
>abstract="O código LUI identifica o uso de elementos obsoletos da interface do usuário. Esses elementos não são recomendados ou não são compatíveis com versões posteriores do AEM e com o AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Alterações importantes: AEM as a Cloud Service"

`LUI` Identifica o uso de elementos obsoletos da interface do usuário. Esses elementos não são recomendados ou não são compatíveis com versões posteriores do AEM e com o AEM as a Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de elementos da interface que devem ou precisam ser atualizados:

* `legacy.dialog.classic`: as caixas de diálogo da IU Clássica com base em ExtJS devem ser alteradas para Coral.
   * Esse subtipo é detectado quando o nome da caixa de diálogo é `dialog` ou `design_dialog` e quando
o valor da propriedade `jcr:primaryType` ou `xtype` é `cq:Dialog`.
* `legacy.dialog.coral2`: as caixas de diálogo `Coral 2` devem ser atualizadas para usar `Coral 3`.
   * Este subtipo é detectado quando a caixa de diálogo e os nomes dos nós de conteúdo secundário são
      * `cq:dialog/content`,
      * `cq:design_dialog/content`,
      * `cq:dialog.coral2/content`,
      * ou `cq:design_dialog.coral2/content`
e o valor da propriedade `sling:resourceType` não contém `granite/ui/components/coral/foundation`.
* `legacy.custom.component`: componentes herdados do `foundation/components` devem ser atualizados para usar os componentes principais.
   * Este subtipo é detectado quando o valor da propriedade `jcr:primaryType` é `cq:Component` e o
     valor da propriedade `sling:resourceSuperType` contém “foundation/components”. Ou, quando qualquer um dos
     valores da propriedade `sling:resourceSuperType` da cadeia de componentes de supertipo contêm
“foundation/components”.
* `legacy.static.template`: modelos estáticos devem ser atualizados para modelos editáveis.
   * Este subtipo é detectado quando o valor da propriedade `jcr:primaryType` é `cq:Template`.
* `content.fragment.template`: os modelos de fragmento de conteúdo devem criar modelos de fragmento para substituir os modelos de fragmento.
   * Os modelos de fragmento de conteúdo podem ser encontrados nos seguintes locais:
      * Os modelos de fragmento de conteúdo prontos para uso são armazenados no `/libs/settings/dam/cfm/templates`
      * Eles podem ser sobrepostos no  `/apps/settings/dam/cfm/templates`  ou  `/conf/.../settings/dam/cfm/templates`(... = global ou “locatário”)
* `translation.dictionary`: o dicionário `I18n` que está presente em `/apps`.
   * `/apps` é imutável no tempo de execução e o arquivo translator.html não estaria mais disponível no AEM as a Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Diretrizes de implementação"
>abstract="A interface clássica não está mais disponível no AEM as a Cloud Service e a interface padrão para criação é a interface habilitada para toque. A prática recomendada é mover todas as interfaces não compatíveis e refatorar as personalizações vinculadas para recursos e funcionalidades mais recentes que sejam compatíveis com o AEM as a Cloud Service. Clientes podem usar o conjunto de modernização do AEM existente para reduzir o trabalho de modernização das implementações do AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Ferramentas de Modernização do AEM"

* A interface clássica não está mais disponível no AEM as a Cloud Service. A interface padrão para criação é a interface habilitada para toque.
* Depender de componentes personalizados herdados pode aumentar os custos de manutenção ao longo do tempo.
* Os modelos de fragmento de conteúdo legados foram substituídos pelos novos modelos de fragmentos de conteúdo no AEM 6.3. A migração de fragmentos de conteúdo baseados em modelos legados para o AEM as a Cloud Service manterá a funcionalidade desses fragmentos, mas não será possível criar mais fragmentos com base no modelo legado. Também não será possível entregar esses fragmentos usando o GraphQL do AEM, que precisa dos novos modelos de fragmentos de conteúdo como esquemas.
* /apps é imutável no tempo de execução e o arquivo translator.html não estaria mais disponível no AEM as a Cloud Service. Portanto, dicionários `I18n` precisam vir do Git por meio do pipeline de CI/CD.

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
   * Designs e caixas de diálogo de design para políticas de modelos editáveis
* Revise a biblioteca de componentes personalizados do seu projeto e faça a transição, se possível, para o conjunto de [Componentes principais](https://experienceleague.adobe.com/pt-br/docs/experience-manager-core-components/using/introduction) padronizados para acelerar o tempo de desenvolvimento e reduzir o custo de manutenção de seus aplicativos.
* Crie modelos de fragmentos de conteúdo com recursos equivalentes aos modelos legados e use esses modelos para criar fragmentos de conteúdo no futuro. Consulte [Modelos de fragmentos de conteúdo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models) para mais detalhes.
* Dicionários `I18n` devem vir do Git por meio do pipeline de CI/CD. [Documentação](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
