---
title: ACV
description: Página de ajuda de códigos do detector de padrões
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: bbeb7193e198a32a9bc966e1821b1058dbbc8c02
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 81%

---

# ACV {#acv}

Validador de conteúdo de ativos

## Segundo plano {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Validador de conteúdo de ativos"
>abstract="O código ACV identifica os nós obrigatórios ausentes no conteúdo de ativos."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html?lang=pt-BR" text="Alterações importantes - Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=pt-BR" text="Experience Manager as a Cloud Service - Notas de versão"

O Validador de conteúdo do Assets `ACV` identifica os nós obrigatórios ausentes e as violações no conteúdo do ativo. Isso pode levar à falha de determinados recursos do Assets no Experience Manager as a Cloud Service.

Os subtipos são usados para identificar os diferentes tipos de informações, como:

* `missing.jcrcontent`: Identifique as pastas com nós obrigatórios ausentes no repositório. A identificação de qualquer conteúdo ausente no repositório ajuda a impedir qualquer falha de recursos ou casos de uso.
* `missing.original.rendition`: Identifique os ativos com uma representação original obrigatória ausente no repositório. Observe que a visualização de páginas de PDF não requer a geração de subativos no AEMaaCS. Portanto, para arquivos PDF, os subativos de relatórios que não têm representação original são suprimidos.
* `metadata.descendants.violation`: Identifique os ativos com mais de 100 descendentes no nó de metadados do ativo no repositório.
* `conflict.node`: Identifique a presença de nós em conflito no repositório no caminho /content/dam.
* `psb.file.large`: Identifique arquivos PSB grandes (dc:format : application/vnd.3gpp.pic-bw-small) com tamanho superior a 2 gigabytes.

## Possíveis implicações e riscos {#implications-and-risks}

* Isso pode levar à falha de determinados recursos do Assets que dependem das propriedades herdadas no Experience Manager as a Cloud Service.
* O AEM Assets depende da existência da representação original. O processamento de ativos no Cloud Service entrará em um loop se a representação original estiver ausente. A geração de subativos não é permitida no AEMaaCS.
* O alto número de descendentes no nó de metadados pode retardar o carregamento de pastas que consistem em ativos que violam isso.
* A presença de nós em conflito pode levar a uma falha de assimilação no AEM as a Cloud Service.
* O Experience Manager pode não processar arquivos PSB de resolução muito alta. Os clientes que usam o ImageMagick para processar arquivos grandes podem enfrentar um impacto no desempenho se o benchmark adequado do servidor Experience Manager não for feito.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Diretrizes de implementação"
>abstract="A Adobe recomenda revisar a estrutura do conteúdo para evitar fluxos de trabalho quebrados que dependem de propriedades herdadas. Entre em contato com o Atendimento ao cliente para obter ajuda."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Analise uma pasta se ela tiver um nó filho ausente. Crie os nós manualmente se o número de pastas for gerenciável, caso contrário, use um script.
* Para os ativos que não têm a representação original, faça upload novamente dos ativos ou exclua-os antes de migrar.
* Nenhuma ação necessária para a representação original de subativos ausentes.
* No caso de nós em conflito, ou eles devem ser resolvidos ou podem precisar ser excluídos antes de migrar para o AEM as a Cloud Service.
* Entre em contato com o Suporte ao cliente do Adobe se planejar processar muitos arquivos PSD ou PSB grandes. O Experience Manager pode não processar arquivos PSB de resolução muito alta com mais de 30.000 x 23.000 pixels. Consulte [documentação](https://experienceleague.adobe.com/docs/experience-manager-64/assets/extending/best-practices-for-imagemagick.html).
* Entre em contato com a [Equipe de Atendimento ao cliente do Experience Manager](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
