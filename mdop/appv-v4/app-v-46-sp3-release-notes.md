---
title: Note sulla versione di App-V 4.6 SP3
description: Note sulla versione di App-V 4.6 SP3
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819795"
---
# Note sulla versione di App-V 4.6 SP3


Per cercare queste note sulla versione, premere CTRL + F.

Leggere accuratamente queste note sulla versione prima di installare il sistema di gestione di Microsoft Application Virtualization (App-V). Queste note sulla versione contengono informazioni che consentono di installare correttamente Application Virtualization (App-V) 4.6 SP3. Questo documento contiene informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una differenza tra queste note sulla versione e altre documentazioni di App-V, la modifica più recente deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Protezione da vulnerabilità e virus della sicurezza


Per proteggere le vulnerabilità e i virus della sicurezza, è importante installare gli ultimi aggiornamenti della sicurezza disponibili per qualsiasi nuovo software da installare. Per altre informazioni, vedere il [sito Web Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problemi noti di Application Virtualization 4.6 SP3


Questa sezione fornisce le informazioni più aggiornate sui problemi relativi a Microsoft Application Virtualization (App-V) 4.6 SP3. Questi problemi non vengono visualizzati nella documentazione del prodotto e in alcuni casi potrebbe essere contraddetta la documentazione del prodotto esistente. Quando è possibile, questi problemi verranno risolti in versioni successive.

### Non è possibile aprire collegamenti ipertestuali tramite Internet Explorer11 in Microsoft Windows 8,1 nell'ambiente virtuale

Il tentativo di aprire collegamenti ipertestuali dall'interno di un ambiente virtuale non riesce in Windows 8,1 con Internet Explorer 11. Questo perché Internet Explorer 11 ora viene fornito con la modalità di protezione avanzata abilitata per impostazione predefinita e questo fa sì che App-V non sia in grado di accedere alle chiavi del registro di sistema, ai file e agli oggetti della porta di comunicazione necessari.

SOLUZIONE alternativa: disabilitare EPM in Internet Explorer11 prima di aprire un pacchetto di App-V. In questo modo potrai aprire Internet Explorer dall'ambiente virtuale.

## Argomenti correlati


[Informazioni su Microsoft Application Virtualization 4.6 SP3](about-microsoft-application-virtualization-46-sp3.md)

 

 





