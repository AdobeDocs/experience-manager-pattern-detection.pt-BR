---
title: IOI
description: Página de ajuda do código do Detector de padrões
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# IOI {#ioi}

Importação interna de Oak

## Segundo plano {#background}

`IOI` O identifica o uso de clientes de pacotes Oak internos, importando-os por meio do OSGi. Normalmente, são exportados sem qualquer versão específica e destinam-se ao consumo apenas por outros pacotes Oak ou serviços de AEM de baixo nível.

Alguns deles são usados por `com.adobe.granite.repository`, que configura um repositório para AEM durante a inicialização. Outro exemplo é o pacote de Adobe `com.adobe.granite.maintenance.oak`, que envolve e fornece tarefas de manutenção do Oak.

## Possíveis implicações e riscos {#implications-and-risks}

* Em uma versão futura do AEM, as exportações internas podem ser removidas, causando dependências quebradas e pacotes inativos, dependendo diretamente do Oak.
* A API nas exportações internas pode mudar.

## Possíveis soluções {#solutions}

* Use a API de recursos do Sling (ou a API JCR) em vez de acesso de baixo nível.
* Evite depender de pacotes internos que não fazem parte de nenhuma API pública ou SPI.
* Entre em contato com a [AEM Equipe de suporte](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou solucionar problemas.