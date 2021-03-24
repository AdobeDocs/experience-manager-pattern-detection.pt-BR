---
title: CAV
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# CAV {#cav}

Violação da área de conteúdo

## Segundo plano {#background}

`CAV` identifica o padrão em que diferentes áreas de conteúdo são usadas de uma maneira que viola as regras da classificação de conteúdo.

O processamento de solicitação Sling define como o conteúdo de um recurso, sua propriedade `sling:resourceType` em particular, é usado para determinar o script que será usado para renderizar o conteúdo. (Consulte [Localizando o script](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script) para obter mais informações.) O Sling também fornece técnicas para acessar e mesclar recursos por meio de &quot;Sobreposições&quot; e &quot;Sobreposições&quot;. Eles são descritos como parte do [Sling Resource Merger](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html) e em [Sobreposições](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html).

Para tornar mais seguro e fácil para os clientes entenderem quais áreas de `/libs` são seguras para usar e sobrepor o conteúdo em `/libs` foi classificado com propriedades de &quot;mixin&quot;: Público, Abstrato, Final e Interno. Cada classificação implica regras sobre como o conteúdo pode ser usuário, herdado ou sobreposto. Consulte [Upgrades sustentáveis](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html) para obter uma descrição detalhada.

## Possíveis implicações e riscos {#implications-and-risks}

* Uma atualização de AEM pode levar a problemas de renderização da página e a outros comportamentos indesejados.
* As atualizações de segurança não são eficazes.

## Possíveis soluções {#solutions}

* Minimize o uso de sobreposição de conteúdo para os casos em que ela é necessária.
* Em particular, evite sobrepor conteúdo restrito (Classificação final e interna).
* Considere adaptar as alterações provenientes de `/libs` após AEM atualizações, do ServicePack ou das instalações do CumulativeFixPack.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.
