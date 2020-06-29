---
title: Configurazione di UE-V 2. x con System Center Configuration Manager 2012
description: Configurazione di UE-V 2. x con System Center Configuration Manager 2012
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824406"
---
# Configurazione di UE-V 2. x con System Center Configuration Manager 2012


Dopo l'installazione di Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 o 2,1 SP1 e le relative caratteristiche necessarie, è necessario configurare UE-V. Il pacchetto di configurazione UE-V consente agli amministratori di usare la caratteristica Impostazioni conformità di System Center Configuration Manager 2012 SP1 o versioni successive per applicare configurazioni coerenti tra i siti in cui sono installati i sistemi UE-V e Configuration Manager.

## Funzionalità supportate di Configuration Pack di UE-V


Il pacchetto di configurazione UE-V include strumenti per eseguire le attività seguenti:

-   Creare o aggiornare le previsioni di distribuzione del modello di posizione delle impostazioni UE-V.

    -   Definire i modelli UE-V da registrare o annullare la registrazione

    -   Aggiornare gli elementi di configurazione e le previsioni del modello UE-V come vengono aggiunti o aggiornati i modelli

    -   Distribuire e registrare modelli UE-V usando la correzione standard degli elementi di configurazione

-   Creare o aggiornare un elemento della configurazione dei criteri dell'agente UE-V per impostare o deselezionare queste impostazioni.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Dimensione massima del pacchetto</p></td>
    <td align="left"><p>Abilitare/disabilitare la sincronizzazione delle app di Windows</p></td>
    <td align="left"><p>Attendere la sincronizzazione all'avvio dell'applicazione</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Impostazione del ritardo di importazione</p></td>
    <td align="left"><p>Sincronizzare le app di Windows non in elenco</p></td>
    <td align="left"><p>Attendere la sincronizzazione all'accesso</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Notifica di importazione delle impostazioni</p></td>
    <td align="left"><p>URL del contatto IT</p></td>
    <td align="left"><p>Attendere il timeout della sincronizzazione</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Percorso di archiviazione delle impostazioni</p></td>
    <td align="left"><p>Contattare il testo descrittivo</p></td>
    <td align="left"><p>Percorso catalogo di modelli di impostazioni</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Attivazione della sincronizzazione</p></td>
    <td align="left"><p>Icona del vassoio abilitata</p></td>
    <td align="left"><p>Start/Stop UE-servizio agente V</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Metodo di sincronizzazione</p></td>
    <td align="left"><p>Notifica primo utilizzo</p></td>
    <td align="left"><p>Definire le app di Windows che andranno in roaming</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Timeout sincronizzazione</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   Verificare la conformità confermando che UE-V è in esecuzione.

## Generare un elemento di configurazione dei criteri dell'agente UE-V


Tutti i criteri e la configurazione dell'agente UE-V vengono distribuiti tramite un singolo elemento di configurazione generato tramite lo strumento UevAgentPolicyGenerator.exe. Questo strumento legge la configurazione desiderata da un file di configurazione XML e crea un IC contenente le impostazioni di individuazione e correzione necessarie per conferire al computer la conformità.

Il file CAB dell'elemento di configurazione dei criteri dell'agente UE-V viene creato usando lo strumento della riga di comando UevTemplateBaselineGenerator.exe, che contiene questi parametri:

-   &lt;Codice sito sito&gt;

-   PolicyName &lt; Name &gt; facoltativo: impostazione predefinita "criteri agente UE-V" se non è presente

-   &lt;Descrizione PolicyDescription &gt; facoltativa: se non è presente, viene fornita una descrizione

-   &lt;Percorso completo di CabFilePath per l'elemento di configurazione. File CAB&gt;

-   &lt;Percorso completo di ConfigurationFile al file XML di configurazione dell'agente&gt;

**Nota**  Potrebbe essere necessario modificare i criteri di esecuzione di PowerShell per consentire l'esecuzione di questi script nell'ambiente. Eseguire questi passaggi nella console di Configuration Manager:

1.  Selezionare ** &gt; le &gt; proprietà delle impostazioni del client di amministrazione**

2.  Nella scheda **agente utente** impostare i criteri di **esecuzione di PowerShell** su **Ignora**

<a href="" id="create"></a>**Creare il primo elemento di configurazione dei criteri UE-V**

1.  Copiare il file di configurazione delle impostazioni predefinite dalla directory di installazione di UE-V config Pack in una posizione visibile alla console di amministrazione di ConfigMgr:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    Il file di configurazione predefinito contiene cinque sezioni:

    <a href="" id="computer-policy"></a>**Criteri computer**  
    Tutte le impostazioni di livello computer UE-V. L'attributo DesiredState può essere

    -   **Impostare** il valore assegnato nel registro di sistema

    -   **Deselezionare** per rimuovere l'impostazione

    -   **Non gestito** per avere l'elemento di configurazione lasciato allo stato corrente

    Non rimuovere le righe da questa sezione. Imposta invece la DesiredState su "non gestito" se non vuoi che Configuration Manager modifichi i valori correnti o predefiniti.

    <a href="" id="currentcomputeruserpolicy"></a>**CurrentComputerUserPolicy**  
    Tutte le impostazioni di livello utente di UE-V. Queste voci eseguono l'override delle impostazioni del computer per un utente. L'attributo DesiredState può essere

    -   **Impostare** il valore assegnato nel registro di sistema

    -   **Deselezionare** per rimuovere l'impostazione

    -   **Non gestito** per avere l'elemento di configurazione lasciato allo stato corrente

    Non rimuovere le righe da questa sezione. Imposta invece la DesiredState su "non gestito" se non vuoi che Configuration Manager modifichi i valori correnti o predefiniti.

    <a href="" id="services"></a>**Servizi**  
    Le voci in questa sezione controllano l'operazione del servizio. Il file di configurazione predefinito contiene una singola voce per UevAgentService. L'attributo DesiredState può essere impostato su **in corso** o **interrotto**.

    <a href="" id="windows8appscomputerpolicy"></a>**Windows8AppsComputerPolicy**  
    Tutte le impostazioni di sincronizzazione delle app di Windows a livello di computer. Ogni PackageFamilyName elencato in questa sezione può essere assegnato un DesiredState di

    -   **Abilitato** per il roaming delle impostazioni

    -   **Disabilitata** per impedire il roaming delle impostazioni

    -   **Deselezionata** per rimuovere la voce dal controllo UE-V

    È possibile aggiungere altre righe a questa sezione in base all'elenco delle app di Windows installate che possono essere visualizzate usando il cmdlet di GetAppxPackage.

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**Windows8AppsCurrentComputerUserPolicy**  
    Identico a Windows8AppsComputerPolicy con le impostazioni che eseguono l'override delle impostazioni del computer per un singolo utente.

2.  Modificare il file di configurazione modificando i campi stato e valore desiderati.

3.  Eseguire questo comando in un computer che esegue la console di amministrazione di ConfigMgr:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  Importare il file CAB usando la console ConfigMgr o l'importazione di PowerShell-CMConfigurationItem

**Aggiornare un elemento di configurazione dei criteri UE-V**

1.  Modificare il file di configurazione modificando i campi stato e valore desiderati.

2.  Eseguire il comando del passaggio 3 in [creare il primo elemento di configurazione dei criteri UE-V](#create). Se il nome è stato modificato con il parametro PolicyName, verificare di aver immesso lo stesso nome.

3.  Reimportare il file CAB. La versione in ConfigMgr verrà aggiornata.

## Generare un modello di previsione UE-V
I modelli UE-V vengono distribuiti usando una previsione contenente più elementi di configurazione. Ogni elemento di configurazione contiene gli script di individuazione e correzione necessari per installare un modello UE-V. L'effettivo modello UE-V è incorporato nello script di correzione per la distribuzione tramite la funzionalità degli elementi di configurazione standard.

Il modello di previsione UE-V viene creato usando lo strumento della riga di comando UevTemplateBaselineGenerator.exe, che contiene questi parametri:

-   &lt;Codice sito sito&gt;

-   &lt;Nome BaselineName &gt; (facoltativo: impostazione predefinita "linea di base distribuzione modello UE-V" se non presente)

-   &lt;Descrizione &gt; di BaselineDescription (facoltativo: viene fornita una descrizione se non è presente)

-   &lt;Cartella modello TemplateFolder UE-V&gt;

-   Registrare l' &lt; elenco dei file di modello separati da virgola&gt;

-   Annullamento della registrazione di un &lt; elenco di modelli separati da virgola&gt;

-   CabFilePath &lt; percorso completo del file CAB previsto per la generazione&gt;

Il risultato è un file CAB previsto pronto per l'importazione in Gestione configurazione. Se in una data futura si aggiorna o si aggiunge un modello, è possibile rieseguire il comando usando lo stesso nome previsto. L'importazione del CAB restituisce gli aggiornamenti della versione CI nei modelli modificati.

### <a href="" id="create2"></a>Creare la prima previsione del modello UE-V

1.  Creare un set "Master" di modelli UE-V in una posizione di cartella stabile visibile al computer in cui è in uso la console di amministrazione di ConfigMgr. Quando si aggiungono o si aggiornano i modelli, questa cartella è la posizione in cui vengono estratte per la distribuzione. L'elenco iniziale dei modelli può essere copiato da un computer con l'installazione di UE-V. Il percorso predefinito del modello è C:\\Programmi \\Programmi\\microsoft User Experience Virtualization\\Templates.

2.  Creare un file di text.bat in cui è possibile aggiungere il comando generatore di modelli. Questa opzione è facoltativa, ma rende più semplice la rigenerazione se si salvano i parametri del comando.

3.  Aggiungere il comando e i parametri al file con estensione bat che genererà la linea di base. L'esempio seguente crea una previsione che distribuisce il blocco note e la calcolatrice:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  Eseguire il file bat per creare UevTemplateBaseline.cab pronto per l'importazione in Gestione configurazione.

### Aggiornare una previsione del modello UE-V

Il generatore di modelli USA la versione modello per determinare se un modello deve essere aggiornato. Se si apporta una modifica al modello e si aggiorna la versione, il generatore di previsione confronta il modello nella cartella master con il modello contenuto nel server di ConfigMgr. Se viene rilevata una differenza, vengono aggiornate le versioni di previsione generate e di CI modificate.

Per distribuire un nuovo modello di blocco note, eseguire la procedura seguente:

1.  Aggiornare il modello e la versione del modello presenti &lt; nell' &gt; elemento Version del modello.

2.  Copiare il modello nella directory del modello master.

3.  Eseguire il comando nel file con estensione bat creato nel passaggio 3 in [creare la prima previsione del modello UE-V](#create2).

4.  Importare il file CAB generato in ConfigMgr usando la console o Import-CMBaseline di PowerShell.

## Ottenere il pacchetto di configurazione UE-V


Il pacchetto di configurazione UE-V per Configuration Manager 2012 SP1 o versioni successive può essere scaricato [qui](https://go.microsoft.com/fwlink/?LinkId=317263).






## Argomenti correlati


[Gestire le configurazioni per UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





