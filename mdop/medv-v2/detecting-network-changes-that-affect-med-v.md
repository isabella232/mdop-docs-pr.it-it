---
title: Rilevamento delle modifiche di rete che influiscono su MED-V
description: Rilevamento delle modifiche di rete che influiscono su MED-V
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823375"
---
# Rilevamento delle modifiche di rete che influiscono su MED-V


La soluzione Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 consente di configurare l'ambiente per rilevare alcune modifiche di rete che potrebbero verificarsi dopo la distribuzione delle aree di lavoro MED-V e che possono influire su MED-V.

La caratteristica include un componente in uso nel sistema operativo guest notificato delle modifiche alla configurazione della rete nel computer host. Consente a un utente non Microsoft ESD o a un'altra applicazione che viene eseguita nel guest di risolvere gli stessi endpoint di rete a cui si risolvono gli host ESD o l'applicazione.

**Nota**  Questa caratteristica è disponibile solo se la macchina virtuale è configurata per la modalità NAT (Network Address Translation). Se la macchina virtuale è configurata per la modalità a BRIDGE, non vengono generate indicazioni per la modifica.

 

In questa sezione vengono fornite informazioni e istruzioni per facilitare il monitoraggio delle modifiche apportate alla rete che possono influire su MED-V.

## Per rilevare le modifiche di rete per MED-V


Dopo aver distribuito le aree di lavoro MED-V, è possibile monitorare le modifiche apportate a determinate configurazioni di rete preformando le attività seguenti:

1. Creare un file MOF (Managed Object Format) che cercherà le modifiche alla configurazione della rete che si desidera monitorare. Il codice seguente mostra un esempio del file MOF che è possibile creare.

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. Compilare il file MOF.

3. Installare il file MOF nell'ospite.

Dopo aver installato il file MOF, è possibile creare un abbonamento agli eventi che sottoscrive gli eventi di creazione, modifica o eliminazione di Strumentazione gestione Windows (WMI) per la classe **CCM \ _NetworkAdapters** . In questo articolo vengono rilevate le modifiche seguenti all'host:

Ci sono modifiche di configurazione alla rete, ad esempio le modifiche apportate all'indirizzo IP o alla scheda di rete?

La rete è disponibile o non disponibile?

La configurazione della rete è stata cambiata dalla modalità BRIDGEd alla modalità NAT?

La configurazione della rete è stata modificata dalla modalità NAT alla modalità BRIDGEd?

Un componente MED-V nell'host monitora la rete per queste modifiche e quindi segnala l'ospite della modifica. Un componente del Guest crea un'istanza WMI per monitorare l'area di lavoro MED-V per queste modifiche.

L'abbonamento a un evento creato fornisce una notifica tramite il sistema WMI quando si verifica una o più di queste modifiche alla rete, ovvero creazione, modifica o eliminazione.

## Argomenti correlati


[Monitorare le aree di lavoro MED-V](monitor-med-v-workspaces.md)

[Gestire le impostazioni dell'area di lavoro MED-V](manage-med-v-workspace-settings.md)

 

 





