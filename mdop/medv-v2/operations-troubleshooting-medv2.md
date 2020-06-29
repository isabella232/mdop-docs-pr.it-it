---
title: Risoluzione dei problemi relativi alle operazioni
description: Risoluzione dei problemi relativi alle operazioni
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804455"
---
# Risoluzione dei problemi relativi alle operazioni


Questo argomento include le informazioni che è possibile usare per risolvere i problemi di funzionamento generali in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Risoluzione dei problemi nelle operazioni MED-V


Di seguito sono riportati alcuni problemi che gli utenti finali potrebbero incontrare durante l'esecuzione di MED-V e soluzioni per risolvere i problemi seguenti:

Il **Reindirizzamento della documentazione non riesce**. Questo problema si verifica in genere quando la cartella documenti di un utente finale punta a un percorso di rete. Windows non supporta la creazione di una condivisione da un'altra cartella condivisa. Quando un'unità o una cartella viene reindirizzata al Guest, RDP\\Windows Virtual PC crea una condivisione per tale cartella. Pertanto, se la cartella documenti nell'host fa già riferimento a una condivisione, RDP\\Windows Virtual PC non può creare una condivisione di una condivisione.

Un'altra possibile causa di questo problema è che le credenziali necessarie per connettersi alla risorsa di rete potrebbero essere diverse dalle credenziali di dominio dell'utente. MED-V potrebbe rilevare che i documenti vengono reindirizzati nell'host, inviare tali informazioni al Guest e quindi provare a riconnettere la risorsa di rete. Se le credenziali dell'utente non eseguono l'autenticazione, MED-V potrebbe smettere di provare a eseguire l'autenticazione.

**Soluzione**

Per risolvere il problema, provare a eseguire una delle operazioni seguenti:

-   Impostare la directory radice dell'utente all'interno di Active Directory. Il Guest e l'host devono quindi connettersi alla stessa risorsa di rete.

-   Invece di reindirizzare la cartella documenti in un percorso UNC, mapparla a una lettera di unità (nell'host, eseguire il mapping di un'unità che punta alla risorsa di rete). La cartella documenti può quindi essere impostata per usare la lettera dell'unità invece del percorso UNC. Il Guest verrà quindi reindirizzato alla stessa unità mappata come previsto.

-   Creare uno script di avvio nel guest che reindirizza la cartella documenti alla risorsa di rete e fornisca le credenziali aggiuntive in base alle esigenze.

Il **Reindirizzamento degli URL non riesce**. Un URL specificato per il reindirizzamento dall'host al Guest non viene reindirizzato come previsto o sta restituendo un messaggio di errore che indica che il sito Web non esiste.

**Soluzione**

Questo errore può verificarsi quando si verifica un errore di ortografia o un uso errato di caratteri, ad esempio Asterisk (\ *), nelle informazioni sul reindirizzamento degli URL. Controllare il valore del registro di sistema per il reindirizzamento degli URL e correggere eventuali errori.

La chiave del registro di sistema viene chiamata `RedirectUrls` e si trova in genere in:

Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

**Icona nella barra delle applicazioni ingannevole**. Per impostazione predefinita, l'icona visualizzata nella barra delle applicazioni di un utente finale per l'applicazione pubblica e gli URL reindirizzati è l'icona per Windows Virtual PC. Se un utente finale non è a conoscenza di questo comportamento predefinito, possono essere confusi quando si guarda la barra delle applicazioni per individuare l'applicazione.

**Soluzione**

L'unico modo per evitare questo comportamento predefinito consiste nel modificare le impostazioni utente per le proprietà della barra delle applicazioni come indicato di seguito:

1.  Fare clic con il pulsante destro del mouse sulla barra delle applicazioni e quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo **delle proprietà del menu Start e della barra** delle applicazioni fare clic sulla scheda della **barra delle applicazioni** .

3.  Nella barra a discesa della finestra di dialogo **pulsanti della barra delle applicazioni** selezionare **non combinare mai**.

4.  Fai clic su **OK**.

Vengono visualizzate le icone previste per le applicazioni pubblicate e gli URL reindirizzati.

**Avviso emesso se il secondo utente tenta di accedere o se la macchina virtuale è in uso**. Viene emesso un messaggio di avviso quando un secondo utente accede a un'area di lavoro MED-V mentre un primo utente esegue ancora MED-V. L'avviso viene emesso anche se MED-V viene avviato durante l'uso della macchina virtuale, ad esempio se la macchina virtuale è stata avviata tramite Windows Virtual PC nel menu **Start** . Quando l'utente finale accetta il messaggio di avviso, viene arrestato MED-V.

**Soluzione**

Un utente finale deve verificare che tutti gli altri utenti abbiano eseguito la disconnessione da MED-V prima di provare a eseguire l'accesso. In questo modo si garantisce che non sia in corso nessun'altra istanza di MED-V e che Windows Virtual PC non sia in controllo della macchina virtuale.

**Bip sentiti durante la configurazione per la prima volta**. Occasionalmente viene emesso un segnale acustico mentre MED-V esegue la configurazione per la prima volta. Questo può creare confusione per un utente finale. I segnali acustici provengono dalla macchina virtuale quando eseguono determinate azioni, ad esempio l'arresto.

**Soluzione**

È possibile arrestare il servizio bip specificando il comando "net stop beep" all'inizio di ogni sequenza di inizio della macchina virtuale. In alternativa, è possibile disabilitare il servizio bip specificando il comando "sc config beep start = disabled". Puoi specificare questi comandi prima di chiudere l'immagine o come parte di Sysprep.

**Più connessioni di rete create per le aree di lavoro MED-V in modalità Bridged**. Se la configurazione per la prima volta crea un'area di lavoro MED-V configurata per la modalità NAT, crea solo una singola connessione di rete in Windows Virtual PC. Tuttavia, se la configurazione per la prima volta crea un'area di lavoro MED-V configurata per la modalità a BRIDGE, crea una connessione di rete separata per ogni scheda di rete installata nel computer, perché MED-V non può determinare la scheda di rete attiva. Questo assicura inoltre che gli utenti mobili abbiano sempre una scheda di rete disponibile per le connessioni cablate e wireless.

**Soluzione**

Nessuna.

L' **applicazione MED-V non risponde troppo a lungo quando si chiude**. In alcuni casi, un'applicazione MED-V smette di rispondere quando sta provando a chiudersi.

**Soluzione**

Puoi specificare il periodo di tempo in cui MED-V attende di chiudere le applicazioni che non rispondono impostando la chiave del registro di sistema WaitToKillAppTimeout nella macchina virtuale guest. Per altre informazioni, vedere [come aumentare il tempo di arresto in modo che i processi possano uscire correttamente in Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) ( https://go.microsoft.com/fwlink/?LinkId=206819) .

La **ridenominazione di un collegamento a un'applicazione pubblicata nella macchina virtuale guest non modifica il nome pubblicato nell'host**. Quando si pubblica un'applicazione creando un collegamento e quindi rinominando il collegamento nella macchina virtuale Guest, il nome dell'applicazione originale rimane nel menu **Start** dell'host. Il programma continuerà a essere eseguito come previsto, ma il programma manterrà sempre il nome originale.

**Soluzione**

Nessuna. Si tratta di un comportamento noto di Windows Virtual PC.

Lo **spostamento di un collegamento nella macchina virtuale guest non consente di aggiornare la posizione nel menu Start del computer host**. I tasti di scelta rapida dell'applicazione MED-V pubblicati nel menu **Start** del computer host sono catalogati nel registro di sistema. Se sposti un collegamento a un'applicazione in una sottocartella, il registro di sistema non viene aggiornato per riflettere la modifica.

**Soluzione**

Seguire questa procedura per modificare la posizione di un collegamento a un'applicazione MED-V:

1.  Quando è in corso l'installazione di MED-V, aprire Esplora risorse nella macchina virtuale guest MED-V.

2.  Passare alla directory "%ALLUSERSPROFILE%\\Start Menu\\Programs".

3.  Rimuovere le scelte rapide dall'applicazione dalle cartelle di StartMenu o Programs.

4.  Dopo circa 30 secondi, verificare che i tasti di scelta rapida vengano rimossi dal menu **Start** del computer host.

5.  Riportare i tasti di scelta rapida delle applicazioni nelle nuove cartelle programmi nella directory Start Menu\\Programs.

6.  Dopo circa 30 secondi, verificare che i tasti di scelta rapida vengano aggiornati nel menu **Start** del computer host.

**Le applicazioni pubblicate possono essere disattivate dopo il soggiorno**. In alcuni casi, le applicazioni pubblicate verranno disattivate per un periodo di tempo inattivo. Questa situazione si verifica solo se IPsec è abilitato e l'area di lavoro MED-V è configurata per la modalità NAT. Questa situazione non si verifica se l'operazione viene eseguita in modalità BRIDGEd.

**Soluzione**

Disabilitare IPsec quando si esegue l'area di lavoro MED-V in modalità NAT.

**L'aggiunta di un'applicazione pubblicata alla barra delle applicazioni consente di ignorare MED-V**. Se un utente finale aggiunge un'applicazione pubblicata alla barra delle applicazioni e quindi chiude l'applicazione, MED-V viene ignorato la volta successiva che l'applicazione viene aperta dall'icona della barra delle applicazioni. L'applicazione viene invece aperta direttamente in una finestra di VMSAL.

**Soluzione**

Non aggiungere le applicazioni pubblicate in MED-V alla barra delle domande.

## Argomenti correlati


[Procedure consigliate per le operazioni MED-V](security-best-practices-for-med-v-operations.md)

[Risoluzione dei problemi relativi alla distribuzione](deployment-troubleshooting.md)

 

 





