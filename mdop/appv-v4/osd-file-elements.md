---
title: Elementi di file OSD
description: Elementi di file OSD
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816106"
---
# Elementi di file OSD


La directory di installazione di sequencer contiene un file di schema XML, **Softricity. xsd**, che definisce la struttura valida di un file OSD (Open Software Descriptor). Di seguito sono riportati alcuni degli elementi OSD più usati di frequente.

<a href="" id="softpkg"></a>SOFTPKG  
Elemento radice del file OSD che contiene tutti gli elementi che definiscono il pacchetto software.

<a href="" id="codebase"></a>CODEBASE  
Informazioni sul file SFT per il pacchetto, inclusi gli attributi HREF, FILENAME e GUID. Puoi modificare l'attributo HREF se modifichi il punto di distribuzione di questo particolare pacchetto.

<a href="" id="os"></a>Sistema operativo  
Definisce i sistemi operativi che questa applicazione può eseguire in base ai valori impostati inizialmente nella procedura guidata di sequenziazione. Questo valore può contenere solo i valori definiti in **Softricity. xsd**.

<a href="" id="local-interaction-allowed"></a>LOCAL \ _INTERACTION \ _ALLOWED  
Impostato su TRUE, questo consente di creare oggetti denominati (eventi, mutex, semafori, mapping di file e mailslot) e oggetti COM nello spazio dei nomi globale anziché isolati all'interno di un particolare ambiente virtuale, che consente alle applicazioni virtuali di interagire con le applicazioni del sistema operativo host.

Esempio: &lt; implementazione di SOFTPKG &gt; &lt;&gt;

&lt;&gt; &lt; criteri virtualenv&gt;

&lt;LOCAL \ _INTERACTION \ _ALLOWED &gt; true

&lt;/LOCAL\ _INTERACTION \ _ALLOWED&gt;

&lt;/POLICIES &gt; &lt; /virtualenv&gt;

&lt;/IMPLEMENTATION &gt; &lt; /SOFTPKG&gt;

<a href="" id="dependencies"></a>DIPENDENZE  
Definisce la composizione della famiglia dinamica (dipendenze su altri pacchetti) usando un tag CODEBASE da un altro pacchetto.

Esempio: &lt; Dipendenze &gt; &lt; codebase href = "RTSPS://Server/package.SFT" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE = "pkg. 1 \ \ osguard. CP" size = "6572748" obbligatorio = "false"/ &gt; &lt; /Dependencies&gt;

<a href="" id="package-name"></a>NOME PACCHETTO  
Un nome comune per il pacchetto immesso nella pagina delle **informazioni del pacchetto** di sequenziazione guidata, che consente di specificare un singolo nome usato per un'applicazione sequenziata contenente più applicazioni.

<a href="" id="title"></a>TITOLO  
Nome descrittivo facoltativo dell'applicazione che si sta sequenziando.

<a href="" id="abstract"></a>ASTRATTO  
Breve descrizione del pacchetto software immesso nel campo **Commenti** nella pagina delle **informazioni del pacchetto** di sequenziazione guidata. Una procedura consigliata consiste nel specificare informazioni come il livello di sistema operativo e di Service Pack della workstation Sequencer, la versione sequencer e il nome dell'ingegnere della sequenziazione.

<a href="" id="script"></a>SCRIPT  
Definisce eventi di script specifici che si verificano durante l'avvio, l'arresto o lo streaming.

<a href="" id="mgmt-shortcutlist"></a>MGMT \ _SHORTCUTLIST  
Elenco di tutti i collegamenti definiti nella procedura guidata.

<a href="" id="mgmt-fileassociations"></a>MGMT \ _FILEASSOCIATIONS  
Elenco dei tipi di file specificati nella procedura guidata.

## Argomenti correlati


[Informazioni sulla scheda OSD](about-the-osd-tab.md)

 

 





