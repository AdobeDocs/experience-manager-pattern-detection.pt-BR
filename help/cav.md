---
title: CAV
description: Página de ajuda de códigos do detector de padrões
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 1966a3e83ab6b2247d9f1095c8965eac399e3b6e
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# CAV {#cav}

Violação da área de conteúdo

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Violação da área de conteúdo"
>abstract="O código CAV identifica o padrão em que diferentes áreas de conteúdo são usadas de uma maneira que viola as regras da classificação de conteúdo. Essa violação forneceria uma visão geral sobre sobreposições, conteúdo restrito que pode precisar de alterações depois de migrar para o AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=pt-BR#platform" text="Fusão de recursos do Sling"

O código `CAV` identifica o padrão em que diferentes áreas de conteúdo são usadas de uma maneira que viola as regras da classificação de conteúdo.

O processamento de solicitações do Sling define como o conteúdo de um recurso, em particular sua propriedade `sling:resourceType`, é usada para determinar o script que será usado para renderizar o conteúdo. Consulte [Localização de script](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html?lang=pt-BR#locating-the-script) para obter mais informações. O Sling também fornece técnicas para acessar e mesclar recursos por meio de &quot;Sobreposições&quot; e &quot;Substituições&quot;. Elas são descritas como parte da [Fusão de recursos do Sling](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=pt-BR) e em [Sobreposições](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=pt-BR).

Para tornar mais seguro e fácil para os clientes compreenderem quais as áreas de `/libs` são seguras para usar e sobrepor conteúdo, `/libs` foi classificado com propriedades de &quot;mixin&quot;: Público, Abstrato, Final e Interno. Cada classificação contém regras sobre como o conteúdo pode ser usado, herdado ou sobreposto. Consulte [Atualizações sustentáveis](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=pt-BR) para obter uma descrição detalhada.

## Possíveis implicações e riscos {#implications-and-risks}

* Uma atualização do AEM pode levar a problemas de renderização da página e a outros comportamentos indesejados.
* As atualizações de segurança não são eficazes.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Diretrizes de implementação"
>abstract="Os padrões identificados com o CAS, onde existem diferentes violações de área de conteúdo, devem ser revisados. Áreas de classificação de conteúdos finais e internos devem ser evitadas. Entre em contato com o Suporte da Adobe para obter ajuda e esclarecimentos."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=pt-BR" text="Atualizações sustentáveis"
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Minimize o uso de sobreposição de conteúdo para os casos em que for necessária.
* Em particular, evite a sobreposição de conteúdo restrito (classificações Final e Interno).
* Considere adaptar as alterações provenientes de `/libs` após atualizações do AEM e instalações do ServicePack ou do CumulativeFixPack.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
