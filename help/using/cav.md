---
title: CAV
description: Página de ajuda referente ao código do detector de padrões.
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 100%

---

# CAV {#cav}

Violação da área de conteúdo

## Fundo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Violação da área de conteúdo"
>abstract="O código CAV identifica o padrão em que diferentes áreas de conteúdo são usadas de uma maneira que viola as regras da classificação de conteúdo. Essa violação fornece uma visão geral sobre sobreposições e conteúdo restrito que necessitam de alterações depois de serem migrados para o AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sling Resource Merger"

`CAV` identifica o padrão no qual diferentes áreas do conteúdo são usadas de uma maneira que viola as regras da classificação de conteúdo.

O processamento de solicitações do Sling define como o conteúdo de um recurso, mais especificamente sua propriedade `sling:resourceType`, é usado para determinar o script utilizado para renderizar o conteúdo. Consulte [Localização de script](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script) para obter mais informações. O Sling também fornece técnicas para acessar e mesclar recursos por meio de “Sobreposições” e “Substituições”. Essas técnicas são descritas como parte da [Fusão de recursos do Sling](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) e na seção [Sobreposições](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Para garantir que clientes entendam quais áreas de `/libs` são seguras para usar e sobrepor, o conteúdo de `/libs` foi classificado com propriedades de “mixin”:

* Público
* Abstrato
* Final
* Interno

Cada classificação contém regras sobre como o conteúdo pode ser usado, herdado ou sobreposto. Consulte [Atualizações sustentáveis](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) para obter uma descrição detalhada.

## Possíveis implicações e riscos {#implications-and-risks}

* Uma atualização do AEM pode levar a problemas de renderização da página e a outros comportamentos indesejados.
* As atualizações de segurança não são eficazes.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Diretrizes de implementação"
>abstract="Deve-se revisar os padrões identificados como CAS, os quais mostram diferentes violações de área de conteúdo. Áreas de classificação de conteúdo final e interno devem ser evitadas. Entre em contato com o suporte da Adobe para obter ajuda ou esclarecimentos."
>additional-url="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Atualizações sustentáveis"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Minimize o uso de sobreposição de conteúdo para os casos em que for necessária.
* Em particular, evite a sobreposição de conteúdo restrito (classificações Final e Interno).
* Considere adaptar as alterações provenientes de `/libs` após atualizações do AEM e instalações de pacotes de serviço ou pacotes de correções cumulativos.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
