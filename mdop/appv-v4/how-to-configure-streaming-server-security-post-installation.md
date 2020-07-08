---
title: Come configurare la sicurezza di Streaming Server dopo l'installazione
description: Come configurare la sicurezza di Streaming Server dopo l'installazione
author: dansimp
ms.assetid: 9bde3677-d1aa-4dcc-904e-bb49a268d748
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1945b38da5dd50c0bd2fb0c741bd92012e78586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817905"
---
# Come configurare la sicurezza di Streaming Server dopo l'installazione


Configurare App-V Streaming Server per una maggiore sicurezza tramite il registro di sistema. Come per l'App-V Management Server, un certificato deve essere correttamente provisioning con l'identificatore EKU corretto per l'autenticazione del server prima di completare la procedura di post-installazione seguente.

**Per configurare la post-installazione di Streaming Server Security**

1.  Creare una console MMC, aggiungere lo snap-in **certificati** e selezionare **archivio certificati computer locale**.

2.  Aprire i certificati **personali** per il computer e aprire il provisioning del certificato per App-V.

3.  Nella scheda **Dettagli** scorrere verso il basso fino all'identificazione personale e copiare l'hash nel riquadro dei dettagli.

4.  Aprire l'editor del registro di sistema e passare a `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server` .

5.  Modificare il `X509CertHash` valore, incollare l'hash delle identificazioni personali nel campo valore e rimuovere tutti gli spazi. Fare clic su **OK** per accettare la modifica.

6.  Nell'editor del registro di sistema passare a `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts` .

7.  Creare un nuovo valore **DWORD** denominato "322" e quindi immettere il valore decimale come 322 o il valore esadecimale come 142.

8.  Riavviare il servizio di streaming.

## Argomenti correlati


[Come configurare la sicurezza di Management Server dopo l'installazione](how-to-configure-management-server-security-post-installation.md)

[Risoluzione dei problemi di autorizzazione dei certificati](troubleshooting-certificate-permission-issues.md)

 

 





