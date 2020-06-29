---
title: Introduzione a UE-V 2.x
description: Introduzione a UE-V 2.x
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823286"
---
# Introduzione a UE-V 2.x


Seguire i passaggi descritti in questa guida per distribuire rapidamente Microsoft User Experience Virtualization (UE-V) 2,0 o 2,1 in un ambiente di test ridotto. In questo modo, puoi determinare se UE-V è la soluzione più adatta per gestire le impostazioni utente in più dispositivi all'interno dell'azienda.

**Nota**  Le informazioni in questa sezione vengono ripetute in modo più dettagliato in tutto il resto della documentazione. Quindi, se si sa già che l'UE-V 2 è la soluzione giusta e non è necessario valutarla, è sufficiente andare a destra per [preparare una distribuzione UE-v 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md).

 

L'installazione standard di UE-V sincronizza le impostazioni predefinite di Microsoft Windows e Office e molte impostazioni delle app di Windows. Verificare che l'ambiente di test includa due o più computer utente che condividono l'accesso alla rete e si valuterà la valutazione di UE-V in poco tempo.

-   [Passaggio 1: confermare i prerequisiti](#step1): verificare che l'ambiente sia in grado di eseguire la versione UE-V, inclusi i dettagli sulle configurazioni supportate.

-   [Passaggio 2: distribuire il percorso di archiviazione delle impostazioni per la versione UE-v 2](#step2): tutte le distribuzioni UE-v richiedono una posizione per i pacchetti di impostazioni che contengono i valori di impostazione sincronizzati.

-   [Passaggio 3: distribuire l'agente UE-v 2](#step3): per sincronizzare le impostazioni con UE-v, i dispositivi devono avere l'agente UE-v installato ed eseguito.

-   [Passaggio 4: verificare la distribuzione della valutazione UE-v 2](#step4): eseguire alcuni test su due computer in cui è installato l'agente UE-v e verificare la modalità di funzionamento di UE-v.

Questo è tutto! Dopo aver eseguito la procedura, sarà possibile valutare l'utilizzo di UE-V nell'organizzazione.

**Ulteriore valutazione:** È anche possibile eseguire ulteriori passaggi per configurare alcune applicazioni di terze parti e line-of-business per sincronizzare le proprie impostazioni con UE-V come descritto in dettaglio in [distribuire UE-v 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## <a href="" id="step1"></a>Passaggio 1: confermare i prerequisiti


Prima di procedere, verificare che l'ambiente contenga questi requisiti per l'uso di UE-V.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Sistema operativo</strong></th>
<th align="left"><strong>Edizione</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>Architettura di sistema</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Ultimate, Enterprise o Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 o versioni successive</p></td>
<td align="left"><p>.NET Framework 4 o versioni successive</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter o server Web</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 o versioni successive</p></td>
<td align="left"><p>.NET Framework 4 o versioni successive</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Enterprise o Pro</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>32 o 64 bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 o versioni successive</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2 o Windows Server 2012</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 o versioni successive</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 10, pre-1607 versione</p></td>
<td align="left"><p>Enterprise o Pro</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 o versioni successive</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 o versioni successive</p></td>
<td align="left"><p>.NET Framework 4,5</p></td>
</tr>
</tbody>
</table>

**Nota:** A partire da Windows 10, versione 1607, UE-V è incluso in [Windows 10 per le aziende](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) e non fa più parte del Microsoft Desktop Optimization Pack

Inoltre...

-   **Licenza MDOP:** Questa tecnologia fa parte di Microsoft Desktop Optimization Pack (MDOP). I clienti aziendali possono ottenere MDOP con Microsoft Software Assurance. Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere come si ottiene MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Credenziali amministrative** per qualsiasi computer in cui verrà installato

## <a href="" id="step2"></a>Passaggio 2: distribuire il percorso di archiviazione delle impostazioni per UE-V 2


È necessario distribuire un percorso di archiviazione delle impostazioni, una condivisione di rete standard in cui le impostazioni utente sono archiviate in un file del pacchetto di impostazioni. Quando si crea la condivisione di archiviazione delle impostazioni, è necessario limitare l'accesso agli utenti che lo richiedono. [Distribuire una posizione di archiviazione delle impostazioni](https://technet.microsoft.com/library/dn458891.aspx#ssl) fornisce informazioni più dettagliate.

**Creare una condivisione di rete**

1.  Creare un nuovo gruppo di sicurezza e aggiungere gli utenti di UE-V.

2.  Creare una nuova cartella nel computer situato in posizione centrale in cui sono archiviati i pacchetti di impostazioni UE-V e quindi concedere agli utenti di UE-V l'accesso con le autorizzazioni di gruppo alla cartella. L'amministratore che supporta UE-V deve disporre delle autorizzazioni per questa cartella condivisa.

3.  Assegnare agli utenti di UE-V l'autorizzazione per creare una directory quando si connettono. Concedere l'autorizzazione completa a tutte le sottodirectory di tale cartella, ma bloccare l'accesso a qualsiasi elemento di cui sopra.

    1.  Impostare le autorizzazioni SMB (Server Message Block) di livello di condivisione seguenti per la cartella della posizione di archiviazione delle impostazioni.

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong>Account utente</strong></th>
        <th align="left"><strong>Autorizzazioni consigliate</strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Tutti</p></td>
        <td align="left"><p>Nessuna autorizzazione</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Gruppo di sicurezza degli utenti di UE-V</p></td>
        <td align="left"><p>Controllo completo</p></td>
        </tr>
        </tbody>
        </table>

         

    2.  Impostare le autorizzazioni di file system NTFS seguenti per la cartella della posizione di archiviazione delle impostazioni.

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong>Account utente</strong></th>
        <th align="left"><strong>Autorizzazioni consigliate</strong></th>
        <th align="left"><strong>Cartella</strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Creatore/proprietario</p></td>
        <td align="left"><p>Controllo completo</p></td>
        <td align="left"><p>Solo sottocartelle e file</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Gruppo di sicurezza degli utenti di UE-V</p></td>
        <td align="left"><p>Cartella di elenco/dati letti, creare cartelle/accodare dati</p></td>
        <td align="left"><p>Solo questa cartella</p></td>
        </tr>
        </tbody>
        </table>

         

**Nota sulla sicurezza:**

Se si crea la condivisione di archiviazione delle impostazioni in un computer che esegue un sistema operativo Windows Server, configurare UE-V per verificare che il gruppo Administrators locale o l'utente corrente sia il proprietario della cartella in cui sono archiviati i pacchetti di impostazioni. Per abilitare questa ulteriore sicurezza, specificare questa impostazione nell'editor del registro di sistema di Windows Server:

1.  Aggiungere una chiave **reg \ _DWORD** del registro di sistema denominata **"RepositoryOwnerCheckEnabled"** a **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.

2.  Impostare il valore della chiave del registro di sistema su *1*.

## <a href="" id="step3"></a>Passaggio 3: distribuire l'agente UE-V 2


L'agente UE-V sincronizza le impostazioni dell'applicazione e di Windows tra i computer e i dispositivi degli utenti. Per scopi di valutazione, installare l'agente in almeno due computer nell'ambiente di test che appartengono allo stesso utente.

Eseguire il file AgentSetup.exe dalla riga di comando per installare l'agente UE-V. Viene installato nei sistemi operativi 32 bit e 64 bit.

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

Devi specificare il parametro della riga di comando SettingsStoragePath come condivisione di rete del passaggio 2. [Distribuire un agente UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) fornisce informazioni più dettagliate.

## <a href="" id="step4"></a>Passaggio 4: testare la distribuzione della valutazione UE-V 2


È ora possibile eseguire alcuni test sulla distribuzione della valutazione UE-V per vedere come funziona l'UE-V.

****

1.  Nel primo computer (computer A) eseguire una o più delle modifiche seguenti:

    1.  Aprire a Windows desktop e spostarla in una posizione diversa nella finestra.

    2.  Modificare i tipi di carattere predefiniti.

    3.  Aprire la calcolatrice e impostarla su **Scientific**.

    4.  Modificare il comportamento di qualsiasi app di Windows, come descritto in dettaglio nella sezione [gestione dei modelli di posizione delle impostazioni di UE-V 2. x tramite Windows PowerShell e WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).

    5.  Disabilitare la sincronizzazione e i profili di roaming delle impostazioni dell'account Microsoft.

2.  Disconnettersi dal computer A. le impostazioni vengono salvate in un pacchetto di impostazioni di UE-V quando gli utenti bloccano, disconnessione, terminano un'applicazione o quando il provider di sincronizzazione viene eseguito (ogni 30 minuti per impostazione predefinita).

3.  Accedere al secondo computer (computer B) come stesso utente del computer A.

4.  Aprire a Windows desktop e verificare che la posizione della barra delle applicazioni corrisponda a quella del computer A. Verificare che i tipi di carattere predefiniti corrispondano e che la calcolatrice sia impostata su **Scientific**. Verifica anche la modifica apportata a qualsiasi app di Windows.

È possibile modificare le impostazioni del computer B di nuovo nel computer originale in impostazioni. Quindi Disconnetti il computer B ed effettua l'accesso al computer a per verificare le modifiche.

## Altre risorse per questo prodotto


-   [Microsoft User Experience Virtualization (UE-V) 2. x](index.md)

-   [Preparare una distribuzione UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Amministrazione di UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Risoluzione dei problemi relativi a UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Documentazione tecnica su UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





