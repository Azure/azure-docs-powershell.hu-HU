---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 5fe7591855577e083aad5923aed37b18d0b2a40c
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Kibocsátási megjegyzések

Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.

## <a name="version-129"></a>1.2.9-es verzió

A kiadás változásai

* AzureRm.AzureStackAdmin-modul
    + Az Add-AzureRmResourceProviderRegistration parancsmag módosítása a felügyeleti és bérlői Azure Resource Manager-felosztás támogatása érdekében. Új paraméter hozzáadása: -ResourceManagerType
    + Az -AdminUri, -ApiVersion, -SubscriptionId és -Token paraméterek eltávolítása minden parancsmagból. Többször figyelmeztettük a felhasználókat a paraméterek elavulásával kapcsolatban, most pedig eltávolítottuk őket.
* AzureStackStorage-modul
    + Új parancsmagok hozzáadása a tárolóáttelepítési forgatókönyvek támogatása érdekében.
    + A belső összetevőkre és az alapul szolgáló funkciókra hivatkozó parancsmagok eltávolítása.
* AzureRM.BootStrapper
    + Új modul létrehozása az Azure PowerShell-parancsmagok verzióinak a verzióprofilokon keresztül történő kezeléséhez