---
title: ECU
description: Página de ajuda de códigos do detector de padrões
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: cbd43bca20831c19eb30703cc1ec528c75f2a2ef
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 100%

---

# ECU {#ecu}

OBSOLETO: uso de conteúdo externo (substituído por CAV, violação da área de conteúdo)

## Segundo plano {#background}

O código `ECU` identifica o padrão em que diferentes áreas de conteúdo são usadas de uma maneira que viola as regras da classificação de conteúdo.

O processamento de solicitações do Sling define como o conteúdo de um recurso, em particular sua propriedade `sling:resourceType`, é usada para determinar o script que será usado para renderizar o conteúdo. (Consulte [Localização do script](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html?lang=pt-BR#locating-the-script) para obter mais informações.) O Sling também fornece técnicas para acessar e mesclar recursos por meio de &quot;Sobreposições&quot; e &quot;Substituições&quot;. Elas são descritas como parte da [Fusão de recursos do Sling](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=pt-BR) e em [Sobreposições](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=pt-BR).

Para tornar mais seguro e fácil para os clientes compreenderem quais as áreas de `/libs` são seguras para usar e sobrepor conteúdo, `/libs` foi classificado com propriedades de &quot;mixin&quot;: Público, Abstrato, Final e Interno. Cada classificação contém regras sobre como o conteúdo pode ser usado, herdado ou sobreposto. Consulte [Atualizações sustentáveis](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=pt-BR) para obter uma descrição detalhada.

## Possíveis implicações e riscos {#implications-and-risks}

* Uma atualização do AEM pode levar a problemas de renderização da página e a outros comportamentos indesejados.
* As atualizações de segurança não são eficazes.

## Possíveis soluções {#solutions}

* Minimize o uso de sobreposição de conteúdo para os casos em que for necessária.
* Em particular, evite a sobreposição de conteúdo restrito (classificações Final e Interno).
* Considere adaptar as alterações provenientes de `/libs` após atualizações do AEM e instalações do ServicePack ou do CumulativeFixPack.
* Entre em contato com a [Equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
