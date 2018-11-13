---
title: Az Azure PowerShell Az modul bemutatása
description: Bemutatkozik az új Azure PowerShell-modul, az Az, amely az AzureRM modult váltja le.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/08/2018
ms.locfileid: "51276076"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Az új Azure PowerShell Az modul bemutatása

2018 novemberétől az Azure PowerShell `Az` modul teljes nyilvános előzetes verzióban érhető el
Az Az rövidebb parancsokat és nagyobb stabilitást kínál, továbbá a Windows, macOS és Linux rendszert egyaránt támogatja. Emellett funkcióparitást és egyszerű áttelepítési útvonalat biztosít az AzureRM-ről.

Az Az a .NET Standard-kódtárat használja, ami azt jelenti, hogy fut a PowerShell 5.x és PowerShell 6.x verziókon is.
Mivel a PowerShell 6.x a Linux, a macOS és a Windows alatt egyaránt képes futni, ez azt jelenti, hogy az Az minden platformon elérhető.
A .NET Standard használatával az Azure PowerShell kódbázisa egységesíthető, és mindez csak minimális hatással van a felhasználókra.

Az Az egy új modul, ezért a verziószámozás vissza lett állítva. Az első stabil kiadás az 1.0 lesz, de a modul 2018 novemberétől biztosítja a funkcióparitást az AzureRm-mel.

## <a name="upgrade-to-az"></a>Frissítés az Az modulra

Javasoljuk, hogy a felhasználók frissítsenek az új `Az` modulra. Ehhez tegye a következőket:

* [Távolítsa el az Azure PowerShell AzureRM modult.](/powershell/azure/uninstall-azurerm-ps)
* [Telepítse az Azure PowerShell Az modult.](/powershell/azure/install-az-ps)
* Engedélyezze a kompatibilitási módot az AzureRM-hez az `Enable-AzureRMAlias` paranccsal, amíg meg nem ismeri az új parancskészletet.

## <a name="migrate-existing-scripts-to-az"></a>Meglévő szkriptek áttelepítése az Az modulba

A jelentősebb frissítések kényelmetlenek tudnak lenni. Az `Az` modul kompatibilitási módjával azonban továbbra is használhatja a meglévő szkripteket, miközben az új szintaxis frissítésein dolgozik. Az `Enable-AzureRmAlias` parancsmaggal engedélyezheti az `AzureRM`-kompatibilitási módot. Ez a parancsmag az `AzureRM`-parancsmagneveket az új `Az`-parancsmagnevek aliasaiként definiálja.

Az új parancsmagnevek úgy lettek kidolgozva, hogy könnyen megjegyezhetők legyenek. A parancsmagnevekben az `AzureRm` és az `Azure` helyett az `Az` használható. Például a régi `New-AzureRmVm` parancs megfelelője a `New-AzVm` parancs lett.

Az áttelepítési folyamat teljes leírását [az AzureRM modulból az Az modulba való áttelepítést ismertető szakaszban találja](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>Az AzureRM jövőbeli támogatottsága

Az `Az` 1.0-s verziójának 2018 decemberi kiadásával a meglévő `AzureRM` modul nem bővül majd újabb parancsmagokkal vagy funkciókkal. Azonban az `AzureRM` hivatalos karbantartása és hibajavítása nem szűnik meg. Az Azure legfrissebb szolgáltatásainak és funkcióinak használatához érdemes áttérnie az `Az` modul használatára.