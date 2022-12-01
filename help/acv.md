---
title: ACV
description: Página de ajuda de códigos do detector de padrões
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: e7096efc1d9da7f5aad5a5b353ba622c879cc4a5
workflow-type: ht
source-wordcount: '348'
ht-degree: 100%

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

## Possíveis implicações e riscos {#implications-and-risks}

* Isso pode levar à falha de determinados recursos do Assets que dependem das propriedades herdadas no Experience Manager as a Cloud Service.
* O AEM Assets depende da existência da representação original. O processamento de ativos no Cloud Service entrará em um loop se a representação original estiver ausente. A geração de subativos não é permitida no AEMaaCS.
* O alto número de descendentes no nó de metadados pode retardar o carregamento de pastas que consistem em ativos que violam isso.

## Possíveis soluções {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Diretrizes de implementação"
>abstract="A Adobe recomenda revisar a estrutura do conteúdo para evitar fluxos de trabalho quebrados que dependem de propriedades herdadas. Entre em contato com o Atendimento ao cliente para obter ajuda."
>additional-url="https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html" text="Suporte da Experience Cloud"

* Analise uma pasta se ela tiver um nó filho ausente. Crie os nós manualmente se o número de pastas for gerenciável, caso contrário, use um script.
* Para os ativos que não têm a representação original, faça upload novamente dos ativos ou exclua-os antes de migrar.
* Nenhuma ação necessária para a representação original de subativos ausentes.
* Entre em contato com a [Equipe de Atendimento ao cliente do Experience Manager](https://helpx.adobe.com/br/enterprise/using/support-for-experience-cloud.html) para obter esclarecimentos ou fazer considerações.
