---
title: Az Azure PowerShell telepítése MSI-vel
description: Az Azure PowerShell telepítése a PowerShellGet nélkül, MSI használatával
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 1ca6f71bc25ceb9d05f78d77b090480005539ec2
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409833"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Az Azure PowerShell telepítése Windows rendszeren MSI-vel

Ez a cikk bemutatja, hogyan telepíthető az Azure PowerShell Windows rendszeren egy MSI-telepítő használatával. Az MSI-telepítő olyan környezetekhez érhető el, ahol a PowerShell-galériát tűzfal blokkolhatja, vagy ha offline telepítőre van szükség. Az Azure PowerShell telepítésének ajánlott módja a PowerShellGet használata. Útmutatás az Azure PowerShell PowerShellGet segítségével való telepítéséhez: [Az Azure PowerShell telepítése a PowerShellGet segítségével](install-az-ps.md).

## <a name="requirements"></a>Követelmények

A Windows MSI-telepítője csak a PowerShell 5.1-hez telepíti az Azure PowerShellt. Nem Windows-platformokon vagy a PowerShell újabb verzióival való telepítéshez a [telepítést a PowerShellGet használatával](install-az-ps.md) végezze el. A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:

```powershell-interactive
$PSVersionTable.PSVersion
```

Az Azure PowerShell PowerShell 5.1-ben való használatához a következőkre van szükség:

1. Frissítsen a [Windows PowerShell 5.1-re](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell), ha szükséges. Ha Windows 10 rendszert használ, már telepítve van a PowerShell 5.1.
2. Telepítse a [.NET-keretrendszer 4.7.2-es vagy újabb verzióját](/dotnet/framework/install).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Telepítés vagy frissítés Windows rendszeren az MSI-csomaggal

Az Azure PowerShell MSI-csomagja a [GitHubon](https://github.com/Azure/azure-powershell/releases/latest) érhető el. Ha az MSI-vel telepítette az Azure PowerShell korábbi verzióit, a telepítő automatikusan eltávolítja őket. Az MSI-csomag a következő helyre telepíti a modulokat: `${env:ProgramFiles}\WindowsPowerShell\Modules`.

Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult a(z) `Import-Module Az` segítségével. A modul felépítéséből adódóan ez akár egy percig is eltarthat.

Ezt a lépést minden új PowerShell-munkamenet esetében meg kell ismételni. Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.

## <a name="provide-feedback"></a>Visszajelzés küldése

Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues). A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.

## <a name="next-steps"></a>Következő lépések

Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt. Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.
