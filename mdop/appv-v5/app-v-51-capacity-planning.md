---
title: Pianificazione della capacità di App-V 5.1
description: Pianificazione della capacità di App-V 5.1
author: dansimp
ms.assetid: 7a98062f-5a60-49d6-ab40-dc6057e1dd5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b152536b3c61e47f3fda84489b1e102c285e01c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805986"
---
# Pianificazione della capacità di App-V 5.1


I suggerimenti seguenti possono essere usati come previsione per determinare informazioni sulla pianificazione della capacità appropriate per l'infrastruttura dell'App-V 5,1 dell'organizzazione.

**Importante**  Usare le informazioni in questa sezione solo come guida generale per la pianificazione della distribuzione di App-V 5,1. I requisiti di capacità del sistema dipendono dai dettagli specifici dell'ambiente hardware e dell'applicazione. Inoltre, i numeri di prestazioni visualizzati in questo documento sono esempi e i risultati possono variare.

 

## Determinare l'ambito del progetto


Prima di progettare l'infrastruttura App-V 5,1, devi determinare l'ambito del progetto. L'ambito è costituito dalla determinazione delle applicazioni che saranno disponibili virtualmente e per identificare anche gli utenti di destinazione e le rispettive posizioni. Queste informazioni consentiranno di determinare il tipo di infrastruttura App-V 5,1 da implementare. Le decisioni relative all'ambito del progetto devono essere basate sulle esigenze specifiche dell'organizzazione.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Determinare l'ambito dell'applicazione</p></td>
<td align="left"><p>A seconda delle applicazioni da virtualizzare, l'infrastruttura App-V 5,1 può essere configurata in modi diversi. La prima attività consiste nel definire le applicazioni che si desidera virtualizzare.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Determinare l'ambito della posizione</p></td>
<td align="left"><p>L'ambito della posizione si riferisce alle posizioni fisiche, ad esempio a livello aziendale o a una specifica posizione geografica, in cui si prevede di eseguire le applicazioni virtualizzate. Può anche riferirsi alla popolazione degli utenti, ad esempio un singolo reparto, che eseguirà le applicazioni virtuali. Devi ottenere una mappa di rete che includa i percorsi di connessione e la larghezza di banda disponibile per ogni posizione e il numero di utenti che usano applicazioni virtualizzate e la velocità di collegamento WAN.</p></td>
</tr>
</tbody>
</table>

 

## Determinare l'infrastruttura di App-V 5,1 necessaria


**Importante**  Entrambi i modelli seguenti richiedono l'installazione del client App-V 5,1 nel computer in cui si prevede di eseguire applicazioni virtuali.

Puoi anche gestire l'ambiente App-V 5,1 usando una soluzione ESD (Electronic Software Distribution), come Microsoft Systems Center Configuration Manager. Per altre informazioni [, Vedi come distribuire pacchetti App-V 5,1 usando la distribuzione elettronica del software](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).

 

-   **Modello autonomo** : il modello autonomo consente alle applicazioni virtuali di essere abilitate per Windows Installer per la distribuzione senza flusso. App-V 5,1 in modalità autonoma è costituito dal sequencer e dal client; non sono necessari componenti aggiuntivi. Le applicazioni vengono preparate per la virtualizzazione usando un processo denominato sequenziamento. Per altre informazioni, Vedi [pianificazione per l'App-V 5,1 sequencer e la distribuzione del client](planning-for-the-app-v-51-sequencer-and-client-deployment.md). Per gli scenari seguenti è consigliabile il modello autonomo:

    -   Con gli utenti remoti disconnessi che non possono connettersi all'infrastruttura App-V 5,1.

    -   Quando si esegue un sistema di gestione software, ad esempio Configuration Manager 2012.

    -   Quando limitazioni della larghezza di banda della rete inibiscono la distribuzione elettronica del software.

-   **Modello di infrastruttura completa** : il modello di infrastruttura completa offre funzionalità di distribuzione, gestione e Reporting del software; include anche lo streaming di applicazioni in rete. Il modello di infrastruttura completa App-V 5,1 è costituito da uno o più server di gestione di App-V 5,1. Il server di gestione può essere usato per pubblicare applicazioni in tutti i client. Il processo di pubblicazione posiziona le icone e i tasti di scelta rapida dell'applicazione virtuale nel computer di destinazione. Può anche eseguire il flusso delle applicazioni agli utenti locali. Per altre informazioni sull'installazione di server di gestione, vedere [pianificazione per la distribuzione del server App-V 5,1](planning-for-the-app-v-51-server-deployment.md). Il modello di infrastruttura completa è consigliato per gli scenari seguenti:

    **Importante**  Il modello di infrastruttura completa App-V 5,1 richiede che Microsoft SQL Server memorizzi i dati di configurazione. Per altre informazioni, Vedi [configurazioni supportate in App-V 5,1](app-v-51-supported-configurations.md).

     

    -   Quando si vuole usare il server di gestione per pubblicare l'applicazione in computer di destinazione.

    -   Per il provisioning rapido delle applicazioni per i computer di destinazione.

    -   Quando si vuole usare la creazione di report di App-V 5,1.

## Linee guida per il ridimensionamento del server end-to-end


La sezione seguente contiene informazioni sulle dimensioni e la pianificazione di app end-to-end-V 5,1. Per informazioni più specifiche, vedere le sezioni successive.

**Nota**  Tempo di risposta di andata e ritorno nel client è il tempo impiegato dal computer che ha eseguito il client App-V 5,1 per ricevere una notifica corretta dal server di pubblicazione. Tempo di risposta di andata e ritorno nel server di pubblicazione è il tempo impiegato dal computer che ha eseguito il server di pubblicazione per ricevere un aggiornamento dei metadati del pacchetto riuscito dal server di gestione.

 

-   i client di 20.000 possono essere destinati a un singolo server di pubblicazione per ottenere il pacchetto aggiornato in un periodo di tempo di andata e ritorno accettabile. ( &lt; 3 secondi)

-   Un singolo server di gestione può supportare fino a 50 server di pubblicazione per l'aggiornamento dei metadati del pacchetto in un periodo di tempo di andata e ritorno accettabile. ( &lt; 5 secondi)

## <a href="" id="---------app-v-5-1-management-server-capacity-planning-recommendations"></a> Suggerimenti per la pianificazione della capacità di gestione del server di App-V 5,1


I server di pubblicazione App-V 5,1 richiedono il server di gestione per le richieste di aggiornamento del pacchetto e le risposte di aggiornamento del pacchetto. Il server di gestione invia quindi le informazioni al database di gestione per recuperare le informazioni. Per altre informazioni sulle configurazioni supportate in App-V 5,1, vedere [configurazioni supportate in App-v 5,1](app-v-51-supported-configurations.md).

**Nota**  Il tempo di aggiornamento predefinito nel server di pubblicazione App-V 5,1 è di 10 minuti.

 

Quando più server di pubblicazione simultanei contattano un singolo server di gestione per aggiornare i metadati dei pacchetti, i tre fattori seguenti influenzano il tempo di risposta di andata e ritorno sul server di pubblicazione:

1.  Numero di server di pubblicazione che effettuano richieste simultanee.

2.  Numero di gruppi di connessioni configurati nel server di gestione.

3.  Numero di gruppi di Access configurati nel server di gestione.

Nella tabella seguente vengono visualizzate altre informazioni su ogni fattore che impatta sul tempo di andata e ritorno.

**Nota**  Tempo di risposta di andata e ritorno è il tempo impiegato dal computer che ha eseguito il server di pubblicazione App-V 5,1 per ricevere un aggiornamento dei metadati del pacchetto riuscito dal server di gestione.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Fattori che influiscono sul tempo di risposta di round trip</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Il numero di server di pubblicazione che richiedono contemporaneamente l'aggiornamento dei metadati del pacchetto.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Un singolo server di gestione può rispondere a un massimo di 320 server di pubblicazione che richiedono contemporaneamente la pubblicazione dei metadati.</p></li>
<li><p>Tempo di risposta di andata e ritorno per i server di 320 pub è di ~ 40 secondi.</p></li>
<li><p>Per &lt; i server di pubblicazione di 50 che richiedono metadati contemporaneamente, il tempo di risposta di andata e ritorno è di &lt; 5 secondi.</p></li>
<li><p>Da 50 a 320 Publishing Servers, il tempo di risposta aumenta linearmente (circa 2x).</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Numero di gruppi di connessioni configurati nel server di gestione.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Per i gruppi di connessioni fino a 100 non sono presenti cambiamenti significativi nel tempo di risposta di andata e ritorno nel server di pubblicazione.</p></li>
<li><p>Per i gruppi di connessioni di 100-400, il tempo di risposta di andata e ritorno è minore.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Numero di gruppi di Access configurati nel server di gestione.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Per un massimo di 40 gruppi di Access, c'è un aumento lineare (circa 3x) nel tempo di risposta di andata e ritorno sul server di pubblicazione.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Nella tabella seguente vengono visualizzati i valori di esempio per ognuno dei fattori precedenti. In ogni variante i pacchetti di 120 vengono aggiornati dal server di gestione di App-V 5.1.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scenario</th>
<th align="left">Variante</th>
<th align="left">Numero di gruppi di connessioni</th>
<th align="left">Numero di gruppi di Access</th>
<th align="left">Numero di server di pubblicazione</th>
<th align="left">Server di pubblicazione/server di gestione del tipo di connessione di rete</th>
<th align="left">Tempo di risposta di andata e ritorno nel server di pubblicazione (in secondi)</th>
<th align="left">Utilizzo della CPU in server di gestione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Server di pubblicazione che contattano simultaneamente server di gestione per la pubblicazione dei metadati.</p></td>
<td align="left"><p>Numero di server di pubblicazione</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>50</p></li>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>300</p></li>
<li><p>315</p></li>
<li><p>320</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>5</p></li>
<li><p>10</p></li>
<li><p>19</p></li>
<li><p>32</p></li>
<li><p>30</p></li>
<li><p>37</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>17</p></li>
<li><p>17</p></li>
<li><p>17</p></li>
<li><p>15</p></li>
<li><p>17</p></li>
<li><p>15</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>I metadati di pubblicazione contengono gruppi di connessioni</p></td>
<td align="left"><p>Numero di gruppi di connessioni</p></td>
<td align="left"><p></p>
<ul>
<li><p>10</p></li>
<li><p>50</p></li>
<li><p>100</p></li>
<li><p>150</p></li>
<li><p>300</p></li>
<li><p>400</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>10</p></li>
<li><p>11</p></li>
<li><p>11</p></li>
<li><p>16</p></li>
<li><p>22</p></li>
<li><p>25</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>17</p></li>
<li><p>19</p></li>
<li><p>22</p></li>
<li><p>19</p></li>
<li><p>20</p></li>
<li><p>20</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>I metadati di pubblicazione contengono gruppi di Access</p></td>
<td align="left"><p>Numero di gruppi di Access</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>10</p></li>
<li><p>20</p></li>
<li><p>40</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>10</p></li>
<li><p>43</p></li>
<li><p>153</p></li>
<li><p>535</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>17</p></li>
<li><p>26</p></li>
<li><p>24</p></li>
<li><p>24</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

L'utilizzo della CPU del computer che gestisce il server di gestione è di circa il 25%, indipendentemente dal numero di server di pubblicazione che ne fanno riferimento. Le transazioni del database di Microsoft SQL Server al secondo, le richieste batch/sec e le connessioni utente sono identiche indipendentemente dal numero di server di pubblicazione. Ad esempio: transazioni/sec è ~ 30, richieste batch ~ 200 e l'utente si connette a ~ 6.

Usando una distribuzione geograficamente distribuita, in cui il server di gestione & i server di pubblicazione utilizzano una rete di collegamento lenta tra di essi, il tempo di risposta di andata e ritorno nei server di pubblicazione è entro limiti di tempo accettabili ( &lt; 5 secondi), anche per le richieste simultanee di 100 su un singolo server di gestione.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scenario</th>
<th align="left">Variante</th>
<th align="left">Numero di gruppi di connessioni</th>
<th align="left">Numero di gruppi di Access</th>
<th align="left">Numero di server di pubblicazione</th>
<th align="left">Server di pubblicazione/server di gestione del tipo di connessione di rete</th>
<th align="left">Tempo di risposta di andata e ritorno nel server di pubblicazione (in secondi)</th>
<th align="left">Utilizzo della CPU in server di gestione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Connessione di rete tra il server di pubblicazione e il server di gestione</p></td>
<td align="left"><p>Rete di collegamento lenta di 1,5 Mbps</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>50</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Cavo DSL a 1,5 Mbps</p></li>
<li><p>Cavo DSL a 1,5 Mbps</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>4</p></li>
<li><p>5</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>2</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Connessione di rete tra il server di pubblicazione e il server di gestione</p></td>
<td align="left"><p>Rete LAN/WIFI</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>1</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Wifi</p></li>
<li><p>Wifi</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>11</p></li>
<li><p>20</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>15</p></li>
<li><p>17</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Se il server di gestione e i server di pubblicazione sono connessi tramite una rete a collegamento lento o una rete ad alta velocità, il server di gestione può gestire circa 15.000 richieste di aggiornamento dei pacchetti in 30 minuti.

## <a href="" id="---------app-v-5-1-reporting-server-capacity-planning-recommendations"></a> Suggerimenti per la pianificazione della capacità di Reporting Server di App-V 5,1


I client App-V 5,1 inviano i dati dei report al server di report. Il server di Reporting registra quindi le informazioni nel database di Microsoft SQL Server e restituisce una notifica corretta al computer che ha eseguito App-V 5,1 client. Per altre informazioni sulle configurazioni supportate in App-V 5,1, vedere [configurazioni supportate in App-v 5,1](app-v-51-supported-configurations.md).

**Nota**  Tempo di risposta di andata e ritorno è il tempo impiegato dal computer che ha eseguito il client App-V 5,1 per inviare le informazioni di segnalazione al server di report e ricevere una notifica corretta dal server di report.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scenario</th>
<th align="left">Riepilogo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Più client App-V 5,1 inviano contemporaneamente informazioni di report al server di report.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Il tempo di risposta di andata e ritorno dal server di report è di 2,6 secondi per i client 500.</p></li>
<li><p>Il tempo di risposta di andata e ritorno dal server di report è di 5,65 secondi per i client 1000.</p></li>
<li><p>Il tempo di risposta di andata e ritorno aumenta linearmente a seconda del numero di client.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Richieste al secondo elaborate dal server di report.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Un singolo server di report e un singolo database possono elaborare un massimo di 139 richieste al secondo. La media è 121 richieste al secondo.</p></li>
<li><p>Se si usano due report server di report nello stesso database di Microsoft SQL Server, la media delle richieste/secondo è simile a un singolo server di report = ~ 127, con un massimo di 278 richieste al secondo.</p></li>
<li><p>Un singolo server di report può elaborare connessioni simultanee/attive di 500.</p></li>
<li><p>Un singolo server di report può elaborare un massimo di connessioni simultanee di 1500.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Database di report.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Bloccare il conflitto nel computer che ha eseguito Microsoft SQL Server è il fattore limitante per le richieste al secondo.</p></li>
<li><p>La velocità effettiva e i tempi di risposta sono indipendenti dalle dimensioni del database.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Calcolo del ritardo casuale**:

Il ritardo casuale specifica il ritardo massimo (in minuti) per l'invio dei dati al server di report. Quando l'attività pianificata viene avviata, il client genera un ritardo casuale compreso tra **0** e **ReportingRandomDelay** e attenderà la durata specificata prima di inviare i dati.

Ritardo casuale = 4 \ * numero di richieste client/media al secondo.

Esempio: per i client di 500, con 120 richieste al secondo, il ritardo casuale è, 4 \ * 500/120 = ~ 17 minuti.

## <a href="" id="---------app-v-5-1-publishing-server-capacity-planning-recommendations"></a> Suggerimenti per la pianificazione della capacità del server di pubblicazione App-V 5,1


I computer che eseguono il client App-V 5,1 si connettono al server di pubblicazione App-V 5,1 per inviare una richiesta di aggiornamento della pubblicazione e per ricevere una risposta. Il tempo di risposta di andata e ritorno viene misurato nel computer che gestisce il client App-V 5,1. Il tempo del processore viene misurato nel server di pubblicazione. Per altre informazioni sulle configurazioni supportate da App-V 5,1, vedere [configurazioni supportate in App-v 5,1](app-v-51-supported-configurations.md).

**Importante**  L'elenco seguente mostra i fattori principali da tenere in considerazione durante la configurazione del server di pubblicazione App-V 5,1:

-   Numero di client che si connettono contemporaneamente a un singolo server di pubblicazione.

-   Numero di pacchetti in ogni aggiornamento.

-   Larghezza di banda di rete disponibile nell'ambiente tra il client e il server di pubblicazione App-V 5,1.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scenario</th>
<th align="left">Riepilogo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Più client App-V 5,1 si connettono contemporaneamente a un singolo server di pubblicazione.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Un server di pubblicazione che gestisce processori dual core può rispondere alla maggior parte dei client di 5000 che richiedono un aggiornamento simultaneo.</p></li>
<li><p>Per i client di 5000-10000, il server di pubblicazione richiede un quad core minimo.</p></li>
<li><p>Per i client di 10000-20000, il server di pubblicazione dovrebbe avere nuclei Quad duali per i tempi di risposta più efficienti.</p></li>
<li><p>Un server di pubblicazione con un quad-core può aggiornare fino a 10000 pacchetti entro 3 secondi. (Supporto di client simultanei di 10000)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Numero di pacchetti in ogni aggiornamento.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Il numero crescente di pacchetti aumenterà il tempo di risposta di ~ 40% (fino a 1000 pacchetti).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Rete tra il client App-V 5,1 e il server di pubblicazione.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>In una rete lenta (larghezza di banda di 1,5 Mbps) è aumentato il 97% del tempo di risposta rispetto alla LAN (fino a 1000 utenti).</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Nota**  L'utilizzo della CPU del server di pubblicazione è sempre elevato durante l'intervallo di tempo in cui è necessario elaborare le richieste simultanee ( &gt; 90% nella maggior parte dei casi). Il server di pubblicazione può gestire le richieste client ~ 1500 in un secondo.

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scenario</th>
<th align="left">Variante</th>
<th align="left">Numero di client App-V 5,1</th>
<th align="left">Numero di pacchetti</th>
<th align="left">Configurazione del processore nel server di pubblicazione</th>
<th align="left">Tipo di connessione di rete Publishing Server/App-V 5,1 client</th>
<th align="left">Tempo di andata e ritorno nel client App-V 5,1 (in secondi)</th>
<th align="left">Utilizzo della CPU nel server di pubblicazione (in%)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,1 client invia la richiesta di aggiornamento della pubblicazione &amp; riceve la risposta, ogni richiesta contenente i pacchetti di 120</p></td>
<td align="left"><p>Numero di client</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>1000</p></li>
<li><p>5000</p></li>
<li><p>10000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Dual Core</p></li>
<li><p>Dual Core</p></li>
<li><p>Quad Core</p></li>
<li><p>Quad Core</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>2</p></li>
<li><p>2</p></li>
<li><p>3</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>99</p></li>
<li><p>89</p></li>
<li><p>77</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Più pacchetti in ogni aggiornamento</p></td>
<td align="left"><p>Numero di pacchetti</p></td>
<td align="left"><p></p>
<ul>
<li><p>1000</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>500</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Quad Core</p></li>
<li><p>Quad Core</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>2</p></li>
<li><p>3</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>92</p></li>
<li><p>91</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Rete tra il client e il server di pubblicazione</p></td>
<td align="left"><p>rete di collegamento lenta di 1,5 Mbps</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>500</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Quad Core</p></li>
<li><p>Quad Core</p></li>
<li><p>Quad Core</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1,5 Mbps intra-Continental Network</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3</p></li>
<li><p>10 (con tasso di errore 0,2%)</p></li>
<li><p>17 (con tasso di errore dell'1%)</p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-1-streaming-capacity-planning-recommendations"></a> Suggerimenti per la pianificazione della capacità di streaming in App-V 5,1


I computer che eseguono il client App-V 5,1 esegue il flusso del pacchetto dell'applicazione virtuale dal server di streaming. Il tempo di risposta di andata e ritorno viene misurato nel computer che gestisce il client App-V 5,1 ed è il tempo impiegato per trasmettere l'intero pacchetto.

**Importante**  L'elenco seguente identifica i fattori principali da tenere in considerazione durante la configurazione del server di streaming App-V 5,1:

-   Il numero di client che esegue lo streaming di pacchetti di applicazioni contemporaneamente da un singolo server di flusso.

-   Dimensioni del pacchetto in streaming.

-   Larghezza di banda di rete disponibile nell'ambiente tra il client e il server di streaming.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scenario</th>
<th align="left">Riepilogo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Più client App-V 5,1 lo streaming di applicazioni da un singolo server di flusso simultaneo.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Se il numero di client in streaming simultaneamente dallo stesso server aumenta, esiste una relazione lineare con il tempo di download/flusso del pacchetto.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Dimensioni del pacchetto in streaming.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Le dimensioni del pacchetto hanno un impatto significativo sul tempo di streaming/download solo per i pacchetti più grandi con una dimensione di ~ 1GB. Per le dimensioni del pacchetto comprese tra 3 MB e 100 MB, il tempo di flusso varia da 20 secondi a 100 secondi, con 100 client simultanei.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Rete tra il client App-V 5,1 e il server di streaming.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>In una rete lenta (larghezza di banda di 1,5 Mbps) è aumentato il 70-80% del tempo di risposta rispetto alla LAN (fino a 100 utenti).</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Nella tabella seguente vengono visualizzati i valori di esempio per ogni fattore nell'elenco precedente:

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
<th align="left">Scenario</th>
<th align="left">Variante</th>
<th align="left">Numero di client App-V 5,1</th>
<th align="left">Dimensioni di ogni pacchetto</th>
<th align="left">Tipo di connessione di rete streaming server/App-V 5,1 client</th>
<th align="left">Tempo di andata e ritorno nel client App-V 5,1 (in secondi)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Più client App-V 5,1 in streaming di pacchetti di applicazioni virtuali da un server di streaming.</p></td>
<td align="left"><p>Numero di client.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>1000</p></li>
<li><p></p></li>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3,5 MB</p></li>
<li><p>3,5 MB</p></li>
<li><p>3,5 MB</p></li>
<li><p></p></li>
<li><p>5 MB</p></li>
<li><p>5 MB</p></li>
<li><p>5 MB</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p></p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>29</p></li>
<li><p>39</p></li>
<li><p>391</p></li>
<li><p></p></li>
<li><p>35</p></li>
<li><p>68</p></li>
<li><p>461</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Dimensioni di ogni pacchetto in streaming.</p></td>
<td align="left"><p>Dimensioni di ogni pacchetto.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p></p></li>
<li><p>100</p></li>
<li><p>200</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>21 MB</p></li>
<li><p>21 MB</p></li>
<li><p></p></li>
<li><p>109</p></li>
<li><p>109</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p></p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<p>33</p>
<p>83</p>
<p></p>
<p>100</p>
<p>160</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Connessione di rete tra client e App-V 5,1 streaming server.</p></td>
<td align="left"><p>rete di collegamento lenta di 1,5 Mbps.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p></p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3,5 MB</p></li>
<li><p></p></li>
<li><p>5 MB</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1,5 Mbps intra-Continental Network</p></li>
</ul></td>
<td align="left"><p></p>
<p>102</p>
<p></p>
<p>121</p></td>
</tr>
</tbody>
</table>

 

Ogni app-V 5,1 streaming server dovrebbe essere in grado di gestire almeno 200 client simultaneamente in streaming applicazioni virtualizzate.

**Nota**  Il tempo effettivo che verrà impiegato per lo streaming viene determinato principalmente dal numero di client in streaming simultaneamente, dal numero di pacchetti, dalle dimensioni del pacchetto, dall'attività di rete del server e dalle condizioni di rete.

 

Ad esempio, un utente medio può trasmettere un pacchetto di 100 MB in meno di 2 minuti, quando i client simultanei di 100 sono in streaming dal server. Tuttavia, un pacchetto di dimensioni da 1 GB può richiedere fino a 30 minuti. Nella maggior parte dei casi reali la richiesta di streaming non viene distribuita in modo uniforme, sarà necessario comprendere i requisiti di picco di flusso approssimativo presenti nell'ambiente per ridimensionare correttamente il numero di server di flusso necessari.

Il numero di client che un server di streaming può supportare può essere notevolmente aumentato e i requisiti di flusso di picco sono ridotti se si prememorizzano le applicazioni. Puoi anche aumentare il numero di client che un server di streaming può supportare usando pacchetti di distribuzione su richiesta e flussi ottimizzati.

## Combinazione dei ruoli del server App-V 5,1


Riduzione dei requisiti di scalabilità e tolleranza d'errore, il numero minimo di server necessari per una posizione con connettività ad Active Directory è uno. Questo server ospiterà il server di gestione, il servizio server di gestione e i ruoli di Microsoft SQL Server. I ruoli del server possono quindi essere organizzati in qualsiasi combinazione desiderata, perché non sono in conflitto tra loro.

Ignorando i requisiti di ridimensionamento, il numero minimo di server necessari per l'implementazione a tolleranza d'errore è quattro. Il server di gestione e il supporto dei ruoli di Microsoft SQL Server vengono inseriti nelle configurazioni a tolleranza d'errore. Il servizio server di gestione può essere combinato con uno qualsiasi dei ruoli, ma rimane un singolo punto di errore.

Anche se sono disponibili diverse strategie e tecnologie di tolleranza d'errore, non tutte sono applicabili a un servizio specifico. Inoltre, se vengono combinati i ruoli di App-V 5,1, alcune opzioni di tolleranza di errore potrebbero non essere più applicabili a causa di incompatibilità.






## Argomenti correlati


[Configurazioni supportate di App-V 5.1](app-v-51-supported-configurations.md)

[Pianificazione della disponibilità elevata con App-V 5.1](planning-for-high-availability-with-app-v-51.md)

[Pianificazione della distribuzione di App-V](planning-to-deploy-app-v51.md)

 

 





