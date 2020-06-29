---
title: Note sulla versione di MBAM 2.5
description: Note sulla versione di MBAM 2.5
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824985"
---
# Note sulla versione di MBAM 2.5


Per cercare queste note sulla versione, premere CTRL + F.

Leggere queste note sulla versione accuratamente prima di installare Microsoft BitLocker Administration and Monitoring (MBAM) 2,5. Queste note sulla versione contengono informazioni necessarie per installare correttamente MBAM e possono contenere informazioni che non sono disponibili nella documentazione del prodotto. Se queste note sulla versione differiscono da altre documentazioni di MBAM 2,5, tenere presente che la modifica più recente è autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## <a href="" id="---------mbam-2-5-known-issues"></a> Problemi noti di MBAM 2,5


Questa sezione contiene le note sulla versione per MBAM 2,5.

### Web browser eseguito involontariamente come amministratore

I collegamenti della guida nello strumento di configurazione di MBAM server possono causare l'apertura delle finestre del browser con i diritti di amministratore.

**Soluzione alternativa:** Abilitare la configurazione di sicurezza avanzata di Internet Explorer (IESC) o chiudere il Web browser prima di spostarsi in altri siti.

**Nota**  Questo problema è stato risolto in MBAM 2,5 SP1.

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> I report di MBAM sono conformi ai client crittografati con le chiavi di crittografia e il diffusore AES a 256 bit

Se un computer ha installato il client MBAM 2,5 e viene crittografato usando l'AES 256 bit con la forza di cifratura del diffusore, il client MBAM viene segnalato come non conforme nei report di conformità di MBAM.

**Soluzione alternativa:** Installare l'hotfix su [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> MBAM non riesce a crittografare un volume e segnala un errore se si imposta una protezione TPM + PIN in un dispositivo Tablet

Se gli utenti finali provano a impostare una protezione TPM + PIN in un dispositivo tablet, MBAM non riesce a crittografare e segnala un errore. Questo problema si verifica perché i dispositivi tablet non dispongono di una tastiera dell'ambiente di avvio preliminare.

**Soluzione alternativa:** Abilitare l' **uso dell'autenticazione di BitLocker che richiede l'immissione di Preboot da tastiera nell'impostazione di criteri di gruppo Tablet** . Questa impostazione è un'impostazione di criteri di gruppo di BitLocker e non è disponibile nei modelli di criteri di gruppo di MBAM.

### Il nome dell'entità utente è obbligatorio per tutti gli account del servizio

Il nome dell'entità utente (UPN) deve essere impostato per tutti gli account del servizio in MBAM. Se non si riesce a creare un UPN per un account, durante il processo di configurazione viene visualizzato un messaggio di errore che indica che non è stato possibile trovare l'utente o il gruppo in Active Directory.

**Soluzione alternativa:** Aggiungere l'UPN all'account del servizio.

### Il portale self-service richiede una configurazione aggiuntiva se i computer client non possono accedere alla rete di distribuzione del contenuto Microsoft AJAX

Se i computer client non hanno accesso alla rete CDN (Microsoft AJAX Content Delivery Network), che fornisce al portale self-service l'accesso necessario per determinati file JavaScript, è necessario configurare il portale self-service in modo che faccia riferimento ai file JavaScript da un'origine accessibile. Se non si configura il portale self-service quando i computer client non riescono ad accedere alla rete CDN, viene visualizzato solo il nome della società e l'account in cui è stato effettuato l'accesso. Non viene visualizzato alcun messaggio di errore.

**Soluzione alternativa:** Installare MBAM 2,5 SP1. o configura il portale self-service seguendo queste istruzioni: [come configurare il portale self-service quando i computer client non possono accedere alla rete di distribuzione del contenuto Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).

### Il portale self-service e il sito Web di amministrazione e monitoraggio non si aprono dopo l'aggiornamento di IIS a .NET Framework 4,5

Quando si aggiorna Internet Information Services (IIS) a Microsoft .NET Framework 4,5, il portale self-service e il sito Web di amministrazione e monitoraggio non si aprono.

**Soluzione alternativa:** Vedere l'articolo [messaggio di errore dopo l'installazione di .NET Framework 4,0: "Impossibile caricare il tipo" System. ServiceModel. Activation. HttpModule "](https://go.microsoft.com/fwlink/?LinkId=393568).

### Il sito Web di amministrazione e monitoraggio Visualizza un messaggio di errore "Impossibile trovare il report" quando i report non sono configurati

Se si configura il sito Web amministrazione e monitoraggio e quindi si prova a visualizzare un report senza configurare prima la caratteristica report, viene visualizzato un messaggio di errore che indica che non è possibile trovare il report.

**Soluzione alternativa:** Configurare la caratteristica report prima di configurare le applicazioni Web.

### I report nel sito Web amministrazione e monitoraggio visualizzano un avviso se SSL non è configurato in SSRS

Se SQL Server Reporting Services (SSRS) non è stato configurato per l'uso di Secure Socket Layer (SSL), l'URL della caratteristica report verrà impostato su HTTP anziché su HTTPS quando si configura il server MBAM. Se si apre il sito Web amministrazione e monitoraggio e si seleziona un report, viene visualizzato il messaggio di errore seguente: "viene visualizzato solo il contenuto protetto".

**Soluzione alternativa:** Per visualizzare il report, fare clic su **Mostra tutto il contenuto**. Per risolvere il problema, passare al computer MBAM in cui è installato SQL Server Reporting Services, eseguire **Gestione configurazione di Reporting Services**e quindi fare clic su **URL servizio Web**. Selezionare il certificato SSL appropriato per il server, immettere la porta SSL appropriata (la porta predefinita è 443) e quindi fare clic su **applica**.

### Se si fa clic su "back" nel report Riepilogo conformità di BitLocker, potrebbe essere generato un errore

Se si esegue il drill-down in un report di riepilogo conformità di BitLocker e quindi si fa clic sul collegamento a **ritroso** nel report SSRS, potrebbe essere generato un errore.

**Soluzione alternativa:** Nessuno.

### Solo spazio usato la crittografia non funziona correttamente

Se si crittografa un computer per la prima volta dopo l'installazione del client MBAM e si è configurata un'impostazione di criteri di gruppo per implementare la crittografia solo spazio usato, MBAM crittografa erroneamente l'intero disco invece di crittografare solo lo spazio usato del disco. Se un computer è già crittografato con lo spazio usato solo quando si installa il client MBAM e si è configurata la stessa impostazione di criteri di gruppo, MBAM segnala che l'unità è crittografata correttamente e non tenta di ricrittografare l'unità.

**Soluzione alternativa:** Nessuno.

### La forza di crittografia viene visualizzata in modo non corretto nel report conformità computer BitLocker

Se non si imposta un valore di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di criteri di gruppo forza di crittografia, il report conformità computer BitLocker nella topologia di integrazione di Configuration Manager Visualizza sempre "sconosciuto" per il livello di cifratura, anche quando l'intensità della cifratura usa l'impostazione predefinita della crittografia a 128 bit. Il report Visualizza il livello di crittografia corretto se si imposta uno specifico livello di crittografia nell'oggetto Criteri di gruppo.

**Soluzione alternativa:** Imposta sempre un livello di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di gruppo forza di crittografia.

### La distribuzione dello stato di conformità tramite il tipo di unità Visualizza dati obsoleti dopo l'aggiornamento degli elementi di configurazione

Dopo aver aggiornato gli elementi di configurazione di MBAM in SystemCenter2012 ConfigurationManager, la distribuzione dello stato di conformità tramite il grafico a barre del tipo di unità nel dashboard conformità Enterprise di BitLocker Mostra i dati basati sulle informazioni di versioni precedenti degli elementi di configurazione.

**Soluzione alternativa:** Nessuno. La modifica degli elementi di configurazione di MBAM non è supportata e il report potrebbe non essere visualizzato come previsto.

### La configurazione di sicurezza avanzata può causare la visualizzazione errata di un messaggio di errore

Se la configurazione di sicurezza avanzata di Internet Explorer (ESC) è attivata, potrebbe essere visualizzato un messaggio di errore "accesso negato" quando si prova a visualizzare i report nel server MBAM. Per impostazione predefinita, ESC è attivato per proteggere il server diminuendo l'esposizione del server a potenziali attacchi che possono verificarsi tramite il contenuto Web e gli script delle applicazioni.

**Soluzione alternativa:** Se viene visualizzato il messaggio di errore "accesso negato" quando si prova a visualizzare i report nel server MBAM, è possibile impostare un oggetto Criteri di gruppo o modificare manualmente l'impostazione predefinita nell'immagine per disabilitare la configurazione di sicurezza avanzata. È anche possibile visualizzare in alternativa i report di un altro computer in cui ESC non è abilitato.

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a>Aggiornamenti rapidi e articoli della Knowledge base per MBAM 2,5


Questa tabella elenca gli articoli relativi a hotfix e KB per MBAM 2,5.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Articolo KB</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2975636</p></td>
<td align="left"><p>Pacchetto hotfix 1 per l'amministrazione e il monitoraggio di Microsoft BitLocker 2,5</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)">support.microsoft.com/kb/2975636/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>3015477</p></td>
<td align="left"><p>Pacchetto hotfix 2 per l'amministrazione e il monitoraggio di BitLocker 2,5</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)">support.microsoft.com/kb/3015477</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>3011022</p></td>
<td align="left"><p>I report di installazione o Gestione configurazione di MBAM 2,5 non riescono se il nome dell'istanza SSRS contiene un carattere di sottolineatura</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)">support.microsoft.com/kb/3011022/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2756402</p></td>
<td align="left"><p>Il client MBAM fallirebbe con l'ID evento 4 e il codice di errore 0x8004100E nella descrizione dell'evento</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Errore durante l'apertura di report di conformità Enterprise o computer in MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>La configurazione di MBAM 2,0 non riesce durante lo scenario di integrazione di Configuration Manager con SQL Server 2008</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2975472</p></td>
<td align="left"><p>Deadlock SQL quando molti client MBAM si connettono al database di ripristino MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)">support.microsoft.com/kb/2975472/EN-US</a></p></td>
</tr>
</tbody>
</table>

 


## Argomenti correlati


[Informazioni su MBAM 2.5](about-mbam-25.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





