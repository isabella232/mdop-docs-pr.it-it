---
title: Come configurare la pre-installazione dell'immagine
description: Come configurare la pre-installazione dell'immagine
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826406"
---
# Come configurare la pre-installazione dell'immagine


**Nota**  La pre-staging delle immagini è utile solo per il download dell'immagine iniziale. Non è supportata per l'aggiornamento delle immagini.

 

## Come configurare la pre-installazione dell'immagine


**Per configurare la pre-staging delle immagini**

1.  Nel computer client, nella directory dell'archivio immagini, creare una cartella per l'immagine di pre-staging e denominarla *Immagini MED-V*.

    **Nota**  Questa cartella deve essere denominata *Immagini MED-V*.

     

2.  All'interno della cartella Immagini MED-V creare una sottocartella e denominarla *PrestagedImages*.

    **Nota**  Questa cartella deve essere denominata *PrestagedImages*.

     

3.  Per applicare la sicurezza degli elenchi di controllo di accesso (ACL) alla cartella *Immagini MED-V* , impostare l'ACL seguente:

    **Utenti di NT AUTHORITY\\Authenticated: (OI) (CI) (accesso speciale:)**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 FILE \ _APPEND \ _DATA**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **NT AUTHORITY\\SYSTEM: (OI) (CI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **Nota**  È consigliabile applicare la sicurezza ACL alla cartella *Immagini MED-V* .

     

4.  Per applicare la sicurezza ACL alla cartella *PrestagedImages* , impostare l'ACL seguente:

    **Utenti di NT AUTHORITY\\Authenticated: (OI) (CI) (accesso speciale:)**

    **LEGGI \ _CONTROL**

    **SINCRONIZZARE**

    **FILE \ _GENERIC \ _READ**

    **FILE \ _READ \ _DATA**

    **FILE \ _READ \ _EA**

    **FILE \ _READ \ _ATTRIBUTES**

    **NT AUTHORITY\\SYSTEM: (OI) (CI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **Nota**  È consigliabile applicare la sicurezza ACL alla cartella *PrestagedImages* .

     

5.  Premere i file di immagine (CKM e INDEX files) nella cartella *PrestagedImages* .

    **Nota**  Dopo che i file di immagine sono stati spostati nella cartella pre-stage, è consigliabile eseguire un controllo di integrità dei dati e contrassegnare i file come di sola lettura.

     

6.  Includere il parametro seguente nell'installazione del client MED-V: *Client.MSI VMSFOLDER = "C:\\MED-V images"*.

## Come aggiornare la posizione pre-stage


**Per aggiornare la posizione pre-stage**

1.  La chiave del registro di sistema *PrestagedImagesPath*indica la posizione predefinita dell'immagine. Si trova nella directory seguente:

    -   In un x86- `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   In un x64- `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  Se l'immagine si trova in un percorso diverso, modificare il percorso.

 

 





