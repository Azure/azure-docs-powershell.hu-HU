---
title: Az Azure PowerShell Az modul bemutatása
description: Bemutatkozik az új Azure PowerShell-modul, az Az, amely az AzureRM modult váltja le.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: cff9a6ef64907c7ff493dbc9c83dd20a82f297d9
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594871"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Az új Azure PowerShell Az modul bemutatása

2018 decemberétől az Azure PowerShell Az modul általánosan elérhetővé vált, és mostantól az Azure-ral való kommunikációhoz használható PowerShell modul is elérhető. Az Az rövidebb parancsokat és nagyobb stabilitást kínál, valamint több platformot is támogat. Emellett funkcióparitást és egyszerű áttelepítési útvonalat biztosít az AzureRM-ről.

Az Az a .NET Standard-kódtárat használja, ami azt jelenti, hogy fut a PowerShell 5.x és PowerShell 6.x verziókon is.
Mivel a PowerShell 6.x Linux, macOS és Windows rendszeren is fut, az Azure PowerShell mostantól minden platformon elérhető.
A .NET Standard használatával az Azure PowerShell kódbázisa egységesíthető, és mindez csak minimális hatással van a felhasználókra.

Az Az egy új modul, ezért a verziószámozás vissza lett állítva 1.0.0-ra.

## <a name="upgrade-to-az"></a>Frissítés az Az modulra

Minden felhasználónak javasoljuk, hogy frissítsen az új Az modulra. Ehhez tegye a következőket:

* __AJÁNLOTT__: [Távolítsa el az Azure PowerShell AzureRM modult.](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
* [Telepítse az Azure PowerShell Az modult.](/powershell/azure/install-az-ps)
* Engedélyezze a kompatibilitási módot, hogy aliasokat adjon az AzureRM-parancsmagokhoz az `Enable-AzureRMAlias` paranccsal, amíg meg nem ismeri az új parancskészletet. __Csak__ akkor engedélyezze az aliasokat, ha nincs telepítve az AzureRM.

## <a name="migrate-existing-scripts-to-az"></a>Meglévő szkriptek áttelepítése az Az modulba

A jelentősebb frissítések kényelmetlenek tudnak lenni. Az Az modul kompatibilitási módjával azonban továbbra is használhatja a meglévő szkripteket, miközben az új szintaxis frissítésein dolgozik. Az `Enable-AzureRmAlias` parancsmaggal engedélyezheti az AzureRM kompatibilitási módját. Ez a parancsmag az AzureRM-parancsmagneveket az új Az-parancsmagnevek aliasaként definiálja.

Az új parancsmagnevek úgy lettek kidolgozva, hogy könnyen megjegyezhetők legyenek. A parancsmagnevekben az `AzureRm` és az `Azure` helyett az `Az` használható. Például a régi `New-AzureRMVm` parancs megfelelője a `New-AzVm` parancs lett.

Az áttelepítési folyamat teljes leírását [az AzureRM modulból az Az modulba való áttelepítést ismertető szakaszban találja](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>Az AzureRM jövőbeli támogatottsága

A meglévő AzureRM modul nem bővül újabb parancsmagokkal vagy funkciókkal. Azonban az AzureRM hivatalos karbantartása és hibajavítása nem szűnik meg. Az Azure legfrissebb szolgáltatásainak és funkcióinak használatához érdemes áttérnie az Az modul használatára.