---
title: Procedure consigliate MED-V 2.0
description: Procedure consigliate MED-V 2.0
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826115"
---
# Procedure consigliate MED-V 2.0


Durante la pianificazione, la distribuzione e la gestione di MED-V nell'organizzazione, è possibile che siano utili le procedure consigliate.

### Configurare la configurazione per la prima volta per l'esecuzione automatica

Anche se è possibile specificare le impostazioni preferite, è consigliabile creare il file Sysprep. inf in modo che sia possibile eseguire la configurazione per la prima volta in modalità **automatica** . In questo modo è necessario specificare tutte le informazioni sulle impostazioni necessarie mentre si continua con la procedura guidata di **Setup Manager** . Per altre informazioni su come configurare l'immagine MED-V, vedere [configurazione di un'immagine di PC virtuale Windows per MED-v](configuring-a-windows-virtual-pc-image-for-med-v.md).

### Disabilitare i punti di ripristino nella macchina virtuale

Prima di creare il pacchetto dell'area di lavoro MED-V, è consigliabile disabilitare i punti di ripristino nella macchina virtuale per evitare che il disco differenze cresca in modo non associato. Per altre informazioni, vedere [come disattivare e attivare Ripristino configurazione di sistema in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .

### Configurare l'immagine MED-V per usare i profili locali

È consigliabile applicare solo i criteri che hanno senso in un ambiente di compatibilità delle applicazioni per Windows XP. I criteri di personalizzazione desktop, ad esempio, in genere non devono essere applicati e devono essere disabilitati. Per altre informazioni su come consentire solo i profili locali, vedere [impostazioni di criteri di gruppo per i profili utente mobili](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .

### Configurare un aggiornamento delle prestazioni di criteri di gruppo

Per impostazione predefinita, i criteri di gruppo vengono scaricati in un computer un byte alla volta. Ciò causa ritardi quando MED-V viene aggiunto al dominio. Per aumentare le prestazioni dei criteri di gruppo, è consigliabile impostare il valore della chiave del registro di sistema seguente nel registro di sistema:

Sottochiave del registro di sistema: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon

Voce: BufferPolicyReads

Digitare: DWORD

Valore: 1

### Distribuire l'avviso legale tramite criteri di gruppo anziché nell'immagine MED-V

Se si vuole che gli utenti finali vedano un contratto di servizio (SLA) prima di accedere a MED-V, è consigliabile applicare lo SLA tramite criteri di gruppo in un secondo momento in modo che l'SLA venga visualizzato all'utente finale al termine della prima configurazione.

**Attenzione**  Anche se è consigliabile eseguire la configurazione per la prima volta in modalità **automatica** , se si decide di impostare il criterio locale o la voce del registro di sistema per includere un contratto di SLA nell'immagine (disco rigido virtuale), è necessario specificare anche che la configurazione per la prima volta viene eseguita in modalità **assistita** oppure la configurazione iniziale può non riuscire.

 

### Compattare il disco rigido virtuale

È consigliabile compattare il disco rigido virtuale per recuperare spazio su disco vuoto e ridurre le dimensioni del disco rigido virtuale. Per altre informazioni su come compattare il disco rigido virtuale, vedere [compattazione del disco rigido virtuale MED-V](compacting-the-med-v-virtual-hard-disk.md).

### Configurare la macchina virtuale per riavviare l'arresto anomalo della schermata blu

È consigliabile configurare la macchina virtuale dell'area di lavoro MED-V per riavviare automaticamente quando incontra un arresto anomalo della schermata blu. Per configurare questa impostazione nel guest, imposta il valore di riavvio autoboot nella HKEY \ _LOCAL \ _MACHINE chiave \\SYSTEM\\CurrentControlSet\\Control\\CrashControl su "1".

Per configurare questa impostazione, è anche possibile fare clic sul pulsante **Start**, scegliere **Pannello di controllo**e quindi fare clic su **sistema**. Quindi, nell'area **avvio e ripristino** della scheda **Avanzate** , fare clic su **Impostazioni**. Selezionare la casella di controllo **Riavvia automaticamente** e fare clic su **OK**.

### Eseguire il backup dell'immagine MED-V prima di sigillarla

È consigliabile creare una copia di backup dell'immagine MED-V prima di chiuderla. Per altre informazioni sulla chiusura dell'immagine MED-V, vedere [configurazione di un'immagine di PC virtuale Windows per MED-v](configuring-a-windows-virtual-pc-image-for-med-v.md).

### Installare Windows Virtual PC per ultimo durante l'installazione da un file batch

Quando si installano i componenti MED-V usando un file batch, specificare che Windows Virtual PC e Windows Virtual PC hotfix vengono installati dopo l'agente host MED-V e i file del pacchetto dell'area di lavoro MED-V. Questo garantisce che Windows Update non causi interferenze con il processo di installazione richiedendo un riavvio.

### Installare l'area di lavoro MED-V dalla cartella locale

A causa di problemi che possono verificarsi durante l'installazione di MED-V da un percorso di rete, è consigliabile copiare i file di configurazione dell'area di lavoro MED-V localmente e quindi eseguire setup.exe.

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a>Gestire il reindirizzamento della stampante in un solo modo

Se una stampante è installata manualmente nella macchina virtuale guest MED-V e la stessa stampante viene installata in seguito nel computer host, il risultato è che viene installata due volte nel guest. Per evitare questa situazione, è consigliabile usare le procedure consigliate per MED-V per gestire il reindirizzamento della stampante in un solo modo: disabilitare il reindirizzamento e installare le stampanti manualmente nell'ospite oppure abilitare il reindirizzamento e non installare le stampanti manualmente nell'ospite.

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a>Configurare le impostazioni per le patch guest MED-V

È possibile controllare quando e per quanto tempo la macchina virtuale MED-V si risveglia per ricevere gli aggiornamenti automatici definendo i valori di configurazione rilevanti nel registro di sistema. Una procedura consigliata per MED-V consiste nell'impostare l'intervallo di riattivazione in modo che corrisponda al momento in cui sono stati pianificati aggiornamenti regolari per le macchine virtuali MED-V. Inoltre, ti consigliamo di configurare queste impostazioni per assomigliare al comportamento del computer host.

Per altre informazioni su come configurare le impostazioni per le patch guest MED-V, vedere [gestire gli aggiornamenti automatici per le aree di lavoro MED-v](managing-automatic-updates-for-med-v-workspaces.md).

### Configurare il software antivirus/backup

Per evitare che l'attività antivirus incida sulle prestazioni del desktop virtuale, è consigliabile escludere i tipi di file della macchina virtuale seguenti da qualsiasi processo antivirus o di backup in esecuzione nel computer host MED-V:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. VHD

## Argomenti correlati


[Sicurezza e protezione per MED-V](security-and-protection-for-med-v.md)

 

 





