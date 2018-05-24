---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: b42ad6f22f47e10c9190cf5a919f781375ff26f2
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/23/2018
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