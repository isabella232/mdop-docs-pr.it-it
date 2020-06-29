---
title: Come installare il client App-V con Setup.msi
description: Come installare il client App-V con Setup.msi
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817335"
---
# Come installare il client App-V con Setup.msi


Questo argomento descrive come installare il client App-V usando il programma setup.msi. Prima di installare il client App-V tramite il programma setup.msi, è necessario determinare prima di tutto se è necessario installare un software prerequisito e quindi è necessario installarlo. Per installare il software prerequisito, vedere la sezione [installazione del software prerequisito](#prereq-sw) di questo argomento. Per installare il software client, vedere [installazione del client App-V tramite la sezione Setup.msi Program](#msi-setup) di questo argomento.

## <a href="" id="prereq-sw"></a>Installazione del software prerequisiti


Per installare il software prerequisito, è possibile usare le procedure seguenti. Puoi creare un file di comando ed eseguire i comandi dal prompt dei comandi oppure puoi usare un linguaggio di scripting come VBScript o Windows PowerShell per eseguire i comandi.

**Nota**  Le versioni x86 del software seguente sono necessarie per le versioni x86 e x64 del client App-V.

 

**Per installare Microsoft VisualC + + 2005SP1 Redistributable Package (x86)**

1. Scaricare il pacchetto software [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) dall'area download Microsoft ( <https://go.microsoft.com/fwlink/?LinkId=119961> ). \ [Modello di token value \] per la versione 4,5 SP2 e versioni successive del client App-V, Scarica vcredist\_x86.exe da [Microsoft Visual C++ 2005 Service Pack 1 ridistribuibile pacchetto di sicurezza ATL](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [modello di token value \]

2. Per eseguire l'installazione in modo invisibile all'utente, usare l'opzione della riga di comando "/Q" con vcredist\_x86.exe, ad esempio **vcredist\_x86.exe/q**.

3. Per installare il software usando il file vcredist\_x86.msi, usare l'opzione della riga di comando "/C/T: &lt; fullpathtofolder &gt; " per estrarre i file vcredist.msi e vcredis1.cab da vcredist\_x86.exe in una cartella temporanea. Per eseguire l'installazione in modo invisibile all'utente, usare l'opzione della riga di comando/quiet, ad esempio **msiexec/i vcredist.msi** /quiet.

### Per installare Microsoft VisualC + + 2008SP1 Redistributable Package (x86)

**Importante**  Per la versione 4.6 e successive del client App-V, è necessario installare anche l'aggiornamento della protezione ATL pacchetto ridistribuibile di Microsoft Visual C++ 2008 Service Pack 1.

 

****

1.  Scaricare il pacchetto software di [aggiornamento della sicurezza ATL pacchetto di Microsoft Visual C++ 2008 Service Pack 1 ridistribuibile](https://go.microsoft.com/fwlink/?LinkId=150700) dall'area download Microsoft ( https://go.microsoft.com/fwlink/?LinkId=150700) .

2.  Per eseguire l'installazione in modo invisibile all'utente, usare l'opzione della riga di comando "/Q" con vcredist\_x86.exe, ad esempio **vcredist\_x86.exe/q**.

### Per installare Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)

****

1.  Scaricare il pacchetto software [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) dall'area download Microsoft ( https://go.microsoft.com/fwlink/?LinkId=63266) .

2.  Per eseguire l'installazione in modo invisibile all'utente, usare l'opzione della riga di comando/quiet, ad esempio **msiexec/i msxml6\_x86.msi/quiet**.

### Per installare segnalazione errori applicazione Microsoft

Durante l'installazione della segnalazione errori applicazione Microsoft, è necessario usare il parametro *appGUID* per specificare il codice Product App-V. Il codice prodotto è univoco per ogni tipo e versione client App-V. Selezionare il codice prodotto corretto dalla tabella seguente.

**Importante**  Per App-V 4.6 SP2 e versioni successive, non è più necessario installare segnalazione errori applicazioni Microsoft (dw20shared.msi). App-V ora usa la segnalazione degli errori Microsoft.

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione</th>
<th align="left">Codice prodotto per client desktop</th>
<th align="left">Codice prodotto per client per Servizi Desktop remoto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4,5 CU1</p></td>
<td align="left"><p>FE495DBC-6D42-4698-B61F-86E655E0796D</p></td>
<td align="left"><p>8A97C241-D92A-47DC-B360-E716C1AAA929</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,5 SP1</p></td>
<td align="left"><p>93468B43-C19D-44F9-8BCC-114076DB0443</p></td>
<td align="left"><p>0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,5 SP2</p></td>
<td align="left"><p>C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</p></td>
<td align="left"><p>ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86</p></td>
<td align="left"><p>9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</p></td>
<td align="left"><p>439FAC21-B423-41D4-8126-54F9FCB70039</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64</p></td>
<td align="left"><p>E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</p></td>
<td align="left"><p>D2977C18-D88A-47CB-AFD8-652DD36F4D0D</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86 ¹</p></td>
<td align="left"><p>40C3258B-F9D1-46DF-AE97-72C1F86F2427</p></td>
<td align="left"><p>9915D911-CC73-4122-AF4F-564F89454655</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64 ¹</p></td>
<td align="left"><p>1650E31F-23B8-40B5-A60A-C5934F557E3B</p></td>
<td align="left"><p>7580D918-C621-49E7-9877-3CC59F9BD1DA</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86 SP1</p></td>
<td align="left"><p>DB9F70CD-29BC-480B-8BA2-C9C2232C4553</p></td>
<td align="left"><p>1354855A-2298-4C73-9022-EF0686C65991</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64 SP1</p></td>
<td align="left"><p>342C9BB8-65A0-46DE-AB7A-8031E151AF69</p></td>
<td align="left"><p>B2C6C8D5-FE76-4056-A326-EE5D633EA175</p></td>
</tr>
</tbody>
</table>

 

¹ App-V "lingue" rilascio.

**Nota**  Se è necessario trovare il codice prodotto, è possibile usare l'Orca.exe editor di database o uno strumento simile per esaminare i file di Windows Installer per trovare il valore della proprietà *ProductCode* . Per altre informazioni sull'uso di Orca.exe, vedere [strumenti di sviluppo di Windows Installer](https://go.microsoft.com/fwlink/?LinkId=150008) ( https://go.microsoft.com/fwlink/?LinkId=150008) .

 

****

1.  Individuare il programma di installazione della segnalazione degli errori delle applicazioni Microsoft, dw20shared.msi, che si trova nella cartella **Support\\Watson** del supporto di rilascio.

2.  Per installare il software, eseguire il comando seguente:

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a>Installazione del client App-V tramite il programma Setup.msi


Usare la procedura seguente per installare il client App-V. Verificare che sia stato installato il software necessario per i prerequisiti. \ [Template token value \] per la versione 4.6 e successive del client App-V, il programma setup.msi controlla il sistema e se il software prerequisito non è installato, viene generato un messaggio di errore che indica che l'installazione non può continuare. \ [Valore token modello \]

**Per installare il client di virtualizzazione dell'applicazione usando Setup.msi**

1.  Verificare di avere effettuato l'accesso con un account che disponga dei diritti di amministratore nel computer.

2.  Aprire una finestra del prompt dei comandi utilizzando diritti elevati e quindi modificare la directory nella cartella che contiene i file di configurazione. Quando si installa la versione 4.6 o una versione successiva del client App-V, è necessario usare il programma di installazione corretto per il sistema operativo del computer, 32 bit o 64 bit. L'installazione non riesce e verrà visualizzato un messaggio di errore se si usa il programma di installazione errato.

3.  Immettere la stringa di comando installa al prompt dei comandi. In alternativa, è possibile creare un file di comando ed eseguirlo dal prompt dei comandi. Puoi anche usare un linguaggio di scripting come VBScript o Windows PowerShell per eseguire il comando.

4.  Nell'esempio della riga di comando seguente viene illustrato il modo in cui setup.msi può essere usato con una serie di parametri facoltativi. Per altre informazioni su questi parametri, vedere [parametri della riga di comando di Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).

    **msiexec.exe/i "setup.msi" SWICACHESIZE = "10240" SWIPUBSVRDISPLAY = "sistema di produzione" SWIPUBSVRTYPE = "HTTP/Secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "/AppVirt/appsntype.xml" SWIPUBSVRREFRESH = "on" SWIGLOBALDATA = "D:\\AppVirt\\Global" SWIUSERDATA = "^% LOCALAPPDATA ^%\\Windows\\Application client di virtualizzazione" SWIFSDRIVE = "S"/q**

    **Importante**  
    -   L'opzione "**/q**" di Windows Installer consente di eseguire l'installazione invisibile all'utente.

    -   I **%** caratteri "" in "**% HOMEDRIVE%**" devono essere preceduti dal carattere di **^** escape "". In caso contrario, la shell dei comandi di Windows imposta il valore su quello dell'utente che sta eseguendo l'installazione.

    -   Per attivare la registrazione dell'installazione, usare lo switch msiexec **/l\ * v filename. log**.

     

## Argomenti correlati


[Come installare il client usando la riga di comando](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





