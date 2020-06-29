---
title: Come negare l'accesso a un'applicazione
description: Come negare l'accesso a un'applicazione
author: dansimp
ms.assetid: 14f5e201-7265-462c-b738-57938dc3fc30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a89669ea8c6323023b585d6d58620cd203fc00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817516"
---
# Come negare l'accesso a un'applicazione


Gli utenti devono essere nell'elenco **delle autorizzazioni di accesso** di un'applicazione per caricare e usare l'applicazione. Anche se la console di gestione server Application Virtualization non supporta esplicitamente la negazione di un gruppo di utenti per l'accesso a un'applicazione, è possibile rimuovere i gruppi di utenti dalle proprietà di un'applicazione per ottenere questo risultato.

**Per negare l'accesso a un'applicazione**

1.  Per un'applicazione esistente, fare clic sul nodo **applicazioni** nel riquadro sinistro.

2.  Fare clic con il pulsante destro del mouse su un'applicazione nel riquadro destro e scegliere **Proprietà**. Quindi selezionare la scheda **autorizzazioni di accesso** .

3.  Per rimuovere l'accesso per un gruppo di utenti, evidenziare il gruppo di utenti e fare clic su **Rimuovi**.

4.  Fai clic su **OK**.

    **Nota**  Per controllare l'accesso alle applicazioni, puoi anche limitare le licenze dell'applicazione. La configurazione dei gruppi di utenti appropriati in servizi di dominio Active Directory offre il modo più semplice per concedere e negare l'accesso a set di utenti specifici.

     

## Argomenti correlati


[Come concedere l'accesso a un'applicazione](how-to-grant-access-to-an-application.md)

[Come gestire le licenze dell'applicazione in Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[Come gestire le applicazioni in Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

 

 





