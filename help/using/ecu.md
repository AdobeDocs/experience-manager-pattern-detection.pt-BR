---
title: ECU
description: Página de ajuda referente ao código do detector de padrões.
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 75%

---

# ECU {#ecu}

OBSOLETO: uso de conteúdo externo (substituído por CAV, violação da área de conteúdo)

## Fundo {#background}

`ECU` identifica o padrão no qual diferentes áreas de conteúdo são usadas de uma maneira que viola as regras da classificação de conteúdo.

O processamento de solicitações do Sling define como o conteúdo de um recurso, mais especificamente sua propriedade `sling:resourceType`, é usado para determinar o script utilizado para renderizar o conteúdo. (Consulte [Localização do script](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script) para obter mais informações.) O Sling também fornece técnicas para acessar e mesclar recursos por meio de Sobreposições e substituições. Essas técnicas são descritas como parte da [Fusão de recursos do Sling](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) e no [Sobreposições](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Para tornar mais seguro e fácil para os clientes compreenderem quais as áreas de `/libs` são seguros para usar e sobrepor, o conteúdo em `/libs` foi classificado com propriedades de &quot;mixin&quot;:

* Público
* Abstrato
* Final
* Interno

Cada classificação contém regras sobre como o conteúdo pode ser usado, herdado ou sobreposto. Consulte [Atualizações sustentáveis](https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) para obter uma descrição detalhada.

## Possíveis implicações e riscos {#implications-and-risks}

* Uma atualização do AEM pode levar a problemas de renderização da página e a outros comportamentos indesejados.
* As atualizações de segurança não são eficazes.

## Possíveis soluções {#solutions}

* Minimize o uso de sobreposição de conteúdo para os casos em que for necessária.
* Em particular, evite a sobreposição de conteúdo restrito (classificações Final e Interno).
* Considere adaptar as alterações provenientes de `/libs` após atualizações do AEM e instalações de pacotes de serviço ou pacotes de correções cumulativos.
* Entre em contato com a [equipe de suporte do AEM](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou abordar suas considerações.
