---
title: LUI
description: Página de ajuda do código do Detector de padrões.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 54%

---

# LUI {#lui}

Interface do usuário herdada

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Interface do usuário herdada"
>abstract="O código LUI identifica o uso de elementos obsoletos da interface do usuário que não são recomendados ou não são compatíveis em versões posteriores do AEM e do AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Alterações importantes no AEM as a Cloud Service"

`LUI`  Identifica o uso de elementos obsoletos da interface do usuário que não são recomendados ou não são compatíveis em versões posteriores do AEM e no AEM as a Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de elementos da interface do usuário que devem ou precisam ser atualizados:

* `legacy.dialog.classic`: as caixas de diálogo da interface clássica com base em ExtJS devem ser alteradas para Coral.
   * Isso é detectado quando o nome da caixa de diálogo é &quot;dialog&quot; ou &quot;design_dialog&quot; e quando a variável `jcr:primaryType` valor da propriedade ou o `xtype` o valor da propriedade é `cq:Dialog`.
* `legacy.dialog.coral2`: `Coral 2` As caixas de diálogo devem ser atualizadas para usar o `Coral 3`.
   * Isso é detectado quando a caixa de diálogo e seus nomes de nó de conteúdo filho são `cq:dialog/content`,
     `cq:design_dialog/content`, `cq:dialog.coral2/content`&quot;, ou `cq:design_dialog.coral2/content`
e a variável `sling:resourceType` o valor da propriedade não contém &quot;granite/ui/components/coral/foundation&quot;.
* `legacy.custom.component`: componentes herdados do `foundation/components` devem ser atualizados para usar os Componentes principais.
   * Isso é detectado quando a variável `jcr:primaryType` o valor da propriedade é &quot;`cq:Component`&quot; e o
     `sling:resourceSuperType` o valor da propriedade contém &quot;foundation/components&quot;. Ou, qualquer um dos
     os valores de propriedade `sling:resourceSuperType` da cadeia de componentes de supertipo contêm &quot;foundation/components&quot;.
* `legacy.static.template`: modelos estáticos devem ser atualizados para Modelos editáveis.
   * Isso é detectado quando a variável `jcr:primaryType` o valor da propriedade é &quot;`cq:Template`&quot;.
* `content.fragment.template`: os Modelos de fragmento de conteúdo devem criar modelos de fragmento para substituir os modelos de fragmento.
   * Os modelos de fragmento de conteúdo podem ser encontrados nos seguintes locais:
      * Os modelos de fragmento de conteúdo prontos para uso são armazenados no `/libs/settings/dam/cfm/templates`
      * Eles podem ser sobrepostos no  `/apps/settings/dam/cfm/templates`  ou  `/conf/.../settings/dam/cfm/templates`(... = global ou “locatário”)
* `translation.dictionary`: `I18n` dicionário que está presente em /apps.
   * /apps é imutável no tempo de execução e o arquivo translator.html não estaria mais disponível no AEM as a Cloud Service.

## Possíveis implicações e riscos {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Diretrizes de implementação"
>abstract="A interface clássica não está mais disponível no AEM as a Cloud Service e a interface padrão para criação é a interface habilitada para toque. A prática recomendada é mover todas as interfaces não compatíveis e as personalizações vinculadas devem ser refatoradas para recursos/funcionalidades mais recentes que sejam compatíveis com o AEM as a Cloud Service. Os clientes podem usar o Conjunto de modernização do AEM existente para ajudar a reduzir o esforço necessário para modernizar as implementações do AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Ferramentas de Modernização do AEM"

* A interface clássica não está mais disponível no AEM as a Cloud Service. A interface padrão para criação é a interface habilitada para toque.
* Depender de componentes personalizados herdados pode aumentar os custos de manutenção ao longo do tempo.
* Os modelos de fragmento de conteúdo foram substituídos por modelos de fragmento de conteúdo no AEM 6.3. A migração de fragmentos de conteúdo baseados em modelos herdados para AEM as a Cloud Service retém esses fragmentos como funcionais, mas não é possível criar fragmentos com base no modelo herdado. Também não é possível entregar esses fragmentos usando o AEM GraphQL, que requer modelos de fragmento de conteúdo como esquemas.
* /apps é imutável no tempo de execução e o arquivo translator.html não estaria mais disponível no AEM as a Cloud Service. Assim, `I18n` Os dicionários devem vir do Git por meio do pipeline de CI/CD.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Ferramentas e recursos"
>abstract="Com a ajuda do Conjunto de modernização do AEM, os clientes podem converter caixas de diálogo clássicas (ExtJS) em caixas de diálogo Coral. O objetivo é ajudar os clientes a migrar dos recursos não compatíveis ou herdados para as ofertas robustas e modernas do AEM. Essas ferramentas são configuráveis, extensíveis e possuem reconhecimento de configuração. Além disso, explore a substituição de componentes personalizados pelo conjunto de componentes principais padronizados para acelerar o tempo de desenvolvimento e reduzir o custo de manutenção de seus aplicativos."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Conversor de componentes"
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-core-components/using/introduction" text="Componentes principais"

* Para reduzir o esforço necessário para modernizar suas implementações do AEM Sites, use [Conjunto de ferramentas de modernização do AEM](https://opensource.adobe.com/aem-modernize-tools/). Essas ferramentas incluem a conversão de:
   * Caixas de diálogo clássicas (ExtJS) para caixas de diálogo Coral
   * Componentes de base para Componentes principais
   * Modelos estáticos e controle de coluna para modelos editáveis e grade responsiva
   * Desenhos e caixas de diálogo de design para políticas de modelos editáveis
* Revise a biblioteca de componentes personalizados do seu projeto e faça a transição, se possível, para o conjunto de [Componentes principais](https://experienceleague.adobe.com/pt-br/docs/experience-manager-core-components/using/introduction) padronizados para acelerar o tempo de desenvolvimento e reduzir o custo de manutenção de seus aplicativos.
* Crie modelos de fragmento de conteúdo com recursos equivalentes aos modelos herdados e use esses modelos para a criação de fragmentos de conteúdo no futuro. Consulte [Modelos de fragmentos do conteúdo](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models) para obter mais detalhes.
* `I18n` Os dicionários devem vir do Git por meio do pipeline de CI/CD. [Documentação](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Entre em contato com [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) esclarecimentos ou de ter preocupações em conta.
