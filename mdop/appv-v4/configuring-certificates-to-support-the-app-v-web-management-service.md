---
title: Configurazione dei certificati per supportare il Servizio gestione Web di App-V
description: Configurazione dei certificati per supportare il Servizio gestione Web di App-V
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821886"
---
# Configurazione dei certificati per supportare il Servizio gestione Web di App-V


Il servizio di gestione Web App-V deve essere configurato per supportare le connessioni basate su SSL per proteggere la comunicazione. Questo processo richiede che il server Web o il computer in cui è installato il servizio di gestione disponga di un certificato rilasciato al servizio o al computer.

Gli scenari seguenti illustrano come ottenere un certificato a questo scopo:

1.  Nell'infrastruttura aziendale è già presente un'infrastruttura a chiave pubblica (PKI) che emette automaticamente i certificati per i computer.

2.  L'infrastruttura aziendale ha già una PKI in posizione, anche se non rilascia automaticamente certificati ai computer.

3.  L'infrastruttura aziendale non ha una PKI in posizione.

In ognuno degli scenari precedenti, il metodo per ottenere un certificato è diverso, ma il risultato finale è lo stesso. L'amministratore deve assegnare un certificato al sito Web predefinito di IIS e configurare il servizio di gestione Web App-V per richiedere comunicazioni sicure.

**Importante**  Il nome del certificato deve corrispondere al nome del server. È consigliabile usare nomi di dominio completi (FQDN) per il nome comune del certificato.

 

App-V può usare i server IIS per supportare diverse configurazioni di infrastruttura. Per altre informazioni sulla configurazione dei server IIS per il supporto di HTTPS, vedere <https://go.microsoft.com/fwlink/?LinkId=151972> .

## Argomenti correlati


[Come installare e configurare App-V Management Console per un ambiente più sicuro](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 





