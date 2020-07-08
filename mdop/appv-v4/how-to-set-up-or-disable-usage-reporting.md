---
title: Come configurare o disabilitare la creazione di report di utilizzo
description: Come configurare o disabilitare la creazione di report di utilizzo
author: dansimp
ms.assetid: 8587003a-128d-4b5d-ac70-5b9eddddd3dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f8f6c44d4060581f1ebe435875bc2f105cb93d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816546"
---
# Come configurare o disabilitare la creazione di report di utilizzo


È possibile usare le procedure seguenti nella console di gestione di Application Virtualization Server per specificare la durata (in mesi) delle informazioni sull'uso del sistema di virtualizzazione delle applicazioni che si desidera archiviare nel database.

**Nota**  Per archiviare le informazioni sull'utilizzo, è necessario selezionare la casella di controllo **registra informazioni sull'utilizzo** nella scheda **Pipeline provider** . Per visualizzare questa scheda, fare clic con il pulsante destro del mouse sui criteri del provider nel riquadro **dei risultati dei criteri del provider** e scegliere **Proprietà**.

 

**Per configurare la creazione di report sull'utilizzo**

1.  Fare clic con il pulsante destro del mouse sul nodo Application Virtualization System nel riquadro sinistro e scegliere **Opzioni di sistema**.

2.  Selezionare la scheda **database** .

3.  Selezionare il pulsante **di opzione Mantieni l'utilizzo per (mesi)** o **Mantieni tutto l'uso** .

4.  Se si sceglie di specificare la durata dell'utilizzo in mesi, immettere un numero da 1 a 120 (il valore predefinito è di 6 mesi). Se si seleziona **Mantieni tutto l'utilizzo**, il database si svilupperà fino a raggiungere il limite di dimensioni specificato.

5.  Fare clic su **applica** o **OK**.

**Per disabilitare la creazione di report sull'utilizzo**

1.  Fare clic sul nodo **criteri provider** .

2.  Fare clic con il pulsante destro del mouse su **criteri provider** e scegliere **Proprietà**.

3.  Selezionare la scheda **Pipeline provider** .

4.  Deselezionare la casella di controllo **registra informazioni sull'utilizzo** .

5.  Fare clic su **applica** o **OK**.

## Argomenti correlati


[Come personalizzare un sistema di Application Virtualization in Server Management Console](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[Come configurare o disabilitare le dimensioni dei database](how-to-set-up-or-disable-database-size.md)

 

 





