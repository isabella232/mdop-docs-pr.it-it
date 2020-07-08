---
title: Requisiti hardware e software per Application Virtualization Client
description: Requisiti hardware e software per Application Virtualization Client
author: dansimp
ms.assetid: 8b877a2c-5721-4b22-a47f-e2838d58ab12
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5b828f59ba36099b4f6a545cd5bbcb3c72d24e3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819735"
---
# Requisiti hardware e software per Application Virtualization Client


Questo argomento descrive la configurazione minima consigliata hardware e software per l'installazione di Application Virtualization Desktop client e Application Virtualization Client per Servizi Desktop remoto (in precedenza Servizi terminal).

## Client Desktop Application Virtualization


L'elenco seguente include i requisiti hardware e software minimi consigliati per il client Desktop Application Virtualization. I requisiti sono elencati per primo per Microsoft Application Virtualization (App-V) 4.6 SP2, seguiti dai requisiti per le versioni che hanno preceduto l'App-V 4.6 SP2.

**Nota**  Il client Desktop Application Virtualization (App-V) non richiede risorse di processore o RAM aggiuntive oltre ai requisiti del sistema operativo host.

 

### Requisiti hardware

I requisiti hardware sono applicabili a tutte le versioni.

-   Processore: vedere i requisiti di sistema consigliati per il sistema operativo in uso.

-   RAM: vedere requisiti di sistema consigliati per il sistema operativo in uso.

-   Disco: 30MB per l'installazione e 6GB per la cache.

### Requisiti software per App-V 4,6 SP2

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edizione</th>
<th align="left">Service Pack</th>
<th align="left">SKU di architettura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise o Ultimate Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Professional, Enterprise o Ultimate Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP1</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Pro o Enterprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
</tbody>
</table>

I prerequisiti software seguenti vengono installati automaticamente se si usa il metodo Setup.exe. Se si usa il programma di installazione Setup.msi, prima di tutto è necessario installare i prodotti seguenti.
- **Microsoft Visual c++ 2005 SP1 Redistributable Package (x86)**-per altre informazioni sull'installazione di Microsoft visual C++ 2005 SP1 Redistributable Package (x86), vedere [microsoft Visual c++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) ( https://go.microsoft.com/fwlink/?LinkId=119961) . Per la versione 4,5 SP2 del client App-V, scaricare Vcredist\_x86.exe da [Microsoft Visual C++ 2005 Service Pack 1 ridistribuibile pacchetto di sicurezza ATL](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360) .
  -   **Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)**-per altre informazioni sull'installazione di Microsoft Core XML Services (msxml) 6,0 SP1 (x86), vedere [Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) ( https://go.microsoft.com/fwlink/?LinkId=63266) .

Per il client Desktop Application Virtualization (App-V) 4,6, il seguente prerequisito software aggiuntivo viene installato automaticamente se si usa il metodo Setup.exe. Se si usa il programma di installazione Setup.msi, è necessario installarlo anche con gli altri prerequisiti elencati.

-   **Microsoft VisualC + + 2008SP1 Redistributable Package (x86)**-per altre informazioni sull'installazione di Microsoft VisualC + + 2008 SP1 Redistributable Package (x86), vedere [Microsoft VisualC + + 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700) ( https://go.microsoft.com/fwlink/?LinkId=150700) .

### Requisiti software per le versioni che precedono l'App-V 4,6 SP2

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edizione</th>
<th align="left">Service Pack</th>
<th align="left">SKU di architettura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Professional Edition</p></td>
<td align="left"><p>SP2 o SP3</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise o Ultimate Edition</p></td>
<td align="left"><p>Nessun Service Pack, SP1 o SP2</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7 ¹</p></td>
<td align="left"><p>Professional, Enterprise o Ultimate Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP1</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
</tbody>
</table>
¹ supportato per App-V 4,5 SP1 e SP2, App-V 4,6 e 4,6 SP1

Il client Desktop Application Virtualization (App-V) 4,6 supporta gli SKU x86 e x64 di questi sistemi operativi.

I prerequisiti software seguenti vengono installati automaticamente se si usa il metodo Setup.exe. Se si usa il programma di installazione Setup.msi, prima di tutto è necessario installare i prodotti seguenti.

-   <strong>Microsoft Visual C++ 2005 SP1 Redistributable Package (x86) </strong> -per altre informazioni sull'installazione di Microsoft Visual c++ 2005 SP1 Redistributable Package (x86), vedere <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961)"> Microsoft visual C++ 2005 SP1 Redistributable Package (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=119961"> https://go.microsoft.com/fwlink/?LinkId=119961 </a> ). Per la versione 4,5 SP2 del client App-V, scaricare Vcredist_x86.exe da <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="[Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360)"> Microsoft Visual C++ 2005 Service Pack 1 ridistribuibile pacchetto di sicurezza ATL </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=169360"> https://go.microsoft.com/fwlink/?LinkId=169360 </a> ).

-   <strong>Microsoft Core XML Services (MSXML) 6,0 SP1 (x86) </strong> -per altre informazioni sull'installazione di Microsoft Core XML Services (MSXML) 6,0 SP1 (x86), vedere <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="[Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266)"> Microsoft Core XML Services (msxml) 6,0 SP1 (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=63266"> https://go.microsoft.com/fwlink/?LinkId=63266 </a> ).

-   <strong>Segnalazione errori applicazioni Microsoft </strong> : il programma di installazione per questo software è incluso nella <strong> </strong> cartella Support\Watson nel file di archivio autoestraente.

Per il client Desktop Application Virtualization (App-V) 4,6, il seguente prerequisito software aggiuntivo viene installato automaticamente se si usa il metodo Setup.exe. Se si usa il programma di installazione Setup.msi, è necessario installarlo anche con gli altri prerequisiti elencati.

-   <strong>Microsoft Visual C++ 2008 SP1 Redistributable Package (x86) </strong> -per altre informazioni sull'installazione di Microsoft Visual c++ 2008 SP1 Redistributable Package (x86), vedere <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="[Microsoft Visual C++ 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700)"> Microsoft visual C++ 2008 SP1 Redistributable Package (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=150700"> https://go.microsoft.com/fwlink/?LinkId=150700 </a> ).

## Application Virtualization Client per Servizi Desktop remoto

Di seguito sono indicati i requisiti hardware e software consigliati per il client di virtualizzazione dell'applicazione per Servizi Desktop remoto. I requisiti sono elencati per primo per appv461_3, seguiti dai requisiti per le versioni che hanno preceduto l'App-V 4,6 SP2.

Il client Application Virtualization (App-V) per Servizi Desktop remoto non richiede ulteriori risorse di processore o RAM oltre ai requisiti del sistema operativo host.

### Requisiti hardware

I requisiti hardware sono applicabili a tutte le versioni.

-   Processore: vedere i requisiti di sistema consigliati per il sistema operativo in uso.

-   RAM: vedere requisiti di sistema consigliati per il sistema operativo in uso. Questi requisiti dipendono anche dal numero di utenti e applicazioni.

-   Disco: 30MB per l'installazione e 6GB per la cache.

### Requisiti software per App-V 4,6 SP2

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edizione</th>
<th align="left">Service Pack</th>
<th align="left">SKU di architettura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

I prerequisiti software seguenti vengono installati automaticamente se si usa il metodo Setup.exe. Se si usa il programma di installazione Setup.msi, prima di tutto è necessario installare i prodotti seguenti.

-   **Microsoft VisualC + + 2005SP1 Redistributable Package (x86)**-per altre informazioni sull'installazione di Microsoft VisualC + + 2005 SP1 Redistributable Package (x86), vedere [Microsoft VisualC + + 2005 SP1 Redistributable Package (x86](https://go.microsoft.com/fwlink/?LinkId=119961) ) ( https://go.microsoft.com/fwlink/?LinkId=119961) . Per la versione 4.5 SP2 del client App-V, scaricare Vcredist\_x86.exe da [Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package Security Update](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360) .

-   **Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)**-per altre informazioni sull'installazione di Microsoft Core XML Services (MSXML) 6.0 SP1 (x86), vedere [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) ( https://go.microsoft.com/fwlink/?LinkId=63266) .

-   **Segnalazione errori applicazioni Microsoft**: il programma di installazione per questo software è incluso nella cartella **Support\\Watson** nel file di archivio autoestraente.

Per il client Desktop Application Virtualization (App-V) 4,6, il seguente prerequisito software aggiuntivo viene installato automaticamente se si usa il metodo Setup.exe. Se si usa il programma di installazione Setup.msi, è necessario installarlo anche con gli altri prerequisiti elencati.

-   **Microsoft VisualC + + 2008SP1 Redistributable Package (x86)**-per altre informazioni sull'installazione di Microsoft VisualC + + 2008 SP1 Redistributable Package (x86), vedere [Microsoft VisualC + + 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700) ( https://go.microsoft.com/fwlink/?LinkId=150700) .

### Requisiti software per le versioni che precedono l'App-V 4,6 SP2

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edizione</th>
<th align="left">Service Pack</th>
<th align="left">SKU di architettura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Standard Edition, Enterprise Edition o Datacenter Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP2</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>SP1 o SP2</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise o Datacenter Edition</p></td>
<td align="left"><p>Nessun Service Pack o SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

Il client di 4,6 Application Virtualization (App-V) per Servizi Desktop remoto supporta SKU x86 e x64 di questi sistemi operativi.

## Argomenti correlati
- [Requisiti hardware e software per Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)
- [Requisiti di sistema di Application Virtualization](application-virtualization-system-requirements.md)
- [Come installare il client usando la riga di comando](how-to-install-the-client-by-using-the-command-line-new.md)
- [Come installare manualmente Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)
- [Come aggiornare Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)
