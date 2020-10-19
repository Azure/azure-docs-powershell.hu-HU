---
title: Azure PowerShell-szkriptek áttelepítése az AzureRM modulból az Az modulba
description: Ismerje meg a szkriptek az AzureRM modulból az új Az modulba való áttelepítésére szolgáló lépéseket és eszközöket.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: d0045e283ef062c74a223258fd4d5d6432bac531
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/14/2020
ms.locfileid: "92021091"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Az Azure PowerShell migrálása az AzureRM modulból az Az modulba

Az AzureRM PowerShell-modul minden verziója elavult, de a támogatásuk még nem szűnt meg. Mostantól az [Az PowerShell-modul](install-az-ps.md) használatát javasoljuk az Azure-ral folytatott interakciókhoz.

Az AzureRM-parancsmagokhoz írt szkriptek nem működnek automatikusan az új modullal. A váltás megkönnyítése érdekében lett kifejlesztve az [AzureRM és Az közötti migrálási eszközkészlet](https://github.com/Azure/azure-powershell-migration). Az új parancskészletekre való áttérés soha nem egyszerű, ebben a cikkben azonban segítünk megismerkedni az Az PowerShell-modulra való átállás alapjaival. Ha érdekli, miért jött létre az Az PowerShell-modul, olvassa el [az Azure PowerShell új Az moduljának ismertetését](new-azureps-module-az.md).

Az AzureRM és az Az közötti kompatibilitástörő változások teljes listáját [az AzureRM és az Az közötti változások teljes listájában](migrate-az-1.0.0.md) találja.

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Annak ellenőrzése, hogy a meglévő szkriptek működnek-e az AzureRM legújabb kiadásával

A migrálási lépések előtt ellenőrizze, hogy az AzureRM mely verziói vannak telepítve a rendszeren.
Ezzel biztosíthatja, hogy a szkriptek már a legújabb kiadáson fussanak, és megtudhatja, hogy az AzureRM mely verzióit kell eltávolítania.

Az AzureRM telepített verziója/verziói megtekintéséhez futtassa a következő példaparancsot:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

Az AzureRM **legújabb** elérhető kiadása a **6.13.1-es**. Ha nincs telepítve ez a verzió, a meglévő szkriptek további módosítást is igényelhetnek az ebben a cikkben és a [kompatibilitástörő változások listájában](migrate-az-1.0.0.md) leírtakon túlmenően, hogy használni lehessen őket az Az modullal.

Ha a szkriptek nem működnek az AzureRM 6.13.1-es verziójával, frissítse őket az [AzureRM 5.x és 6.x migrálási útmutatója](/powershell/azure/azurerm/migration-guide.6.0.0) szerint. Ha az AzureRM modul korábbi verzióját használja, mindegyik fő verzióhoz elérhető migrálási útmutató.

## <a name="install-the-azurerm-to-az-migration-toolkit"></a>Az AzureRM és Az közötti migrálási eszközkészlet telepítése

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a>PowerShell-szkriptek automatikus migrálása

Az AzureRM és Az közötti migrálási eszközkészlettel létrehozhat egy tervet, amely megállapítja, milyen módosításokat kell végrehajtani a szkripteken, mielőtt valóban módosítaná azokat és telepítené az Az PowerShell-modult.

A [PowerShell-szkriptek az AzureRM modulból az Az PowerShell-modulba történő automatikus migrálásának](quickstart-migrate-azurerm-to-az-automatically.md) gyorsútmutatója végigvezet a PowerShell-szkriptek AzureRM-ből az Az PowerShell-modulba való automatikus frissítésének teljes folyamatán.

## <a name="next-steps"></a>Következő lépések

[Az Azure PowerShell telepítése](install-az-ps.md)
[Az AzureRM eltávolítása](uninstall-az-ps.md#uninstall-the-azurerm-module)
