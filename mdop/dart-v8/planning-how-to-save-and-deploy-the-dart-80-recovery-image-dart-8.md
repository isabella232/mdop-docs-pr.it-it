---
title: Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 8.0
description: Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 8.0
author: dansimp
ms.assetid: 939fbe17-0e30-4c85-8782-5b84d69442a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e5cca90c644eb3edf233564c474d2601d4227fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821245"
---
# Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 8.0


È possibile salvare e distribuire l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 usando i metodi seguenti. Quando si determina il metodo che si vuole usare, valutare i vantaggi e gli svantaggi di ognuno di essi. Dovresti anche prendere in considerazione l'infrastruttura e il personale di supporto. Se si dispone di un'infrastruttura di piccole dimensioni, è consigliabile distribuire il comando DaRT 8,0 usando un elemento multimediale rimovibile, poiché l'immagine di ripristino sarà sempre disponibile se viene installata nel disco rigido locale.

Se l'organizzazione usa servizi di dominio Active Directory, è consigliabile distribuire le immagini di ripristino come servizio di rete tramite Windows DS. Le immagini di ripristino sono sempre disponibili per qualsiasi computer connesso. È possibile distribuire più immagini da Windows DS e mantenerle tutte in un'unica posizione.

**Nota**  È consigliabile usare più di un metodo nell'organizzazione. Ad esempio, è possibile avviare il dardo da una partizione remota per la maggior parte delle situazioni e avere un'unità flash USB disponibile nel caso in cui il computer dell'utente finale non possa connettersi alla rete.

 

La tabella seguente mostra alcuni vantaggi e svantaggi di ogni metodo per l'uso di DaRT nell'organizzazione.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo per l'avvio in dardo</th>
<th align="left">Vantaggi</th>
<th align="left">Svantaggi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Supporto rimovibile</strong></p>
<p>L'immagine di ripristino viene scritta in un CD, un DVD o un'unità USB per consentire al personale di supporto di portare gli strumenti di ripristino al computer instabile.</p></td>
<td align="left"><p>Supporta scenari in cui il record di avvio Master (MBR) è danneggiato e non è possibile accedere al disco rigido e supporta i casi in cui non è disponibile una connessione di rete.</p>
<p>Consente di creare più immagini di ripristino con strumenti diversi per ottenere livelli di supporto diversi.</p>
<p>Fornisce uno strumento predefinito per la masterizzazione di immagini di ripristino su supporti rimovibili.</p></td>
<td align="left"><p>Richiede che il personale di supporto sia fisicamente al computer dell'utente finale per l'avvio in DaRT.</p>
<p>Richiede tempo e manutenzione per creare più elementi multimediali con configurazioni diverse per i computer a 32 bit e a 64 bit.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Da una partizione remota (rete)</strong></p>
<p>L'immagine di ripristino è ospitata in un server di avvio di rete, ad esempio servizi di distribuzione Windows (Windows DS), che consente agli utenti o al personale di supporto di eseguire lo streaming su computer su richiesta.</p></td>
<td align="left"><p>Disponibile per tutti i computer che hanno accesso al server di avvio di rete.</p>
<p>Le immagini di ripristino sono ospitate in un server centrale, che consente gli aggiornamenti centralizzati.</p>
<p>Il personale dell'help desk centralizzato può fornire le riparazioni usando la connettività remota.</p>
<p>Nessun requisito di archiviazione locale per i client.</p>
<p>Possibilità di creare più immagini di ripristino con strumenti diversi per livelli di supporto specifici.</p></td>
<td align="left"><p>La necessità di proteggere l'infrastruttura di Windows DS per garantire che gli utenti regolari possano avviare solo l'immagine di ripristino delle freccette e non il processo completo di imaging del sistema operativo.</p>
<p></p>
<p></p>
<p>Richiede che il computer dell'utente finale sia connesso alla rete in fase di esecuzione.</p>
<p>Richiede che l'immagine di ripristino venga portata in rete.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Da una partizione di ripristino nel disco rigido locale</strong></p>
<p>L'immagine di ripristino viene installata in un disco rigido locale manualmente o tramite sistemi elettronici di distribuzione del software, come System Center Configuration Manager.</p></td>
<td align="left"><p>L'immagine di ripristino è sempre disponibile perché è preimpostata nel computer.</p>
<p>Il personale dell'help desk centralizzato può fornire supporto tramite la connessione remota.</p>
<p>L'immagine di ripristino è gestita centralmente e distribuita.</p>
<p>Le richieste di chiave di ripristino aggiuntive nei computer protetti da crittografia unità BitLocker di Windows vengono eliminate.</p></td>
<td align="left"><p>Lo spazio di archiviazione locale è obbligatorio.</p>
<p>È consigliabile una partizione non crittografata dedicata per il posizionamento delle immagini di ripristino per ridurre il rischio di una partizione di avvio non riuscita.</p>
<p>Quando si aggiorna il dardo, è necessario aggiornare tutti i computer dell'organizzazione anziché una sola partizione (sulla rete) o un dispositivo rimovibile.</p>
<p>Se si distribuisce l'immagine di ripristino dopo l'abilitazione di BitLocker, è necessario un ulteriore considerazione.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Pianificazione della distribuzione di DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)

 

 





