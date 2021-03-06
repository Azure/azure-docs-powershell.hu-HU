---
title: Az Azure PowerShell telepítésének egyéb módjai
description: Az Azure PowerShell telepítése a PowerShellGet nélkül
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7148188603e84efbcd784264de4c78819edf6833
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243718"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a>Az Azure PowerShell telepítése Windows rendszeren MSI-vel vagy a Webplatform-telepítővel

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Ez a cikk bemutatja, hogyan telepíthető az Azure PowerShell Windows rendszeren egy MSI-telepítő vagy Webplatform-telepítő (WebPI) használatával.
Csak akkor alkalmazza ezeket a telepítési módszereket, ha a rendszer számára szükséges. Az Azure PowerShell Windows rendszeren való telepítésének ajánlott módja a PowerShellGet használata. Útmutatás az Azure PowerShell PowerShellGet segítségével való telepítéséhez: [Az Azure PowerShell telepítése a PowerShellGet segítségével](install-azurerm-ps.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Telepítés vagy frissítés Windows rendszeren az MSI-csomaggal

Az Azure PowerShell telepíthető a [GitHubról](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018) elérhető MSI-fájllal is. Ha az Azure-modulok korábbi verziói már telepítve vannak MSI-ként, a telepítő automatikusan eltávolítja őket. Az MSI-csomag a következő helyre telepíti a modulokat: `${env:ProgramFiles}\WindowsPowerShell\Modules`. Az `AzureRM` és az `Azure` modul is telepítve lesz.

> [!NOTE]
> Ha a klasszikus Azure üzemi modellt használja, csak az `Azure` modult használja.

Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `AzureRM` modult az aktuális PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni. Az `AzureRM` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.
Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [felhasználói hitelesítő adatok a PowerShell-munkamenetek között történő megőrzését](context-persistence.md) ismertető részt.

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Telepítés vagy frissítés Windows rendszeren a Webplatform-telepítővel

Töltse le az [Azure PowerShell WebPI csomagot](https://aka.ms/webpi-azps), és indítsa el a telepítést. Ha az Azure-modulok korábbi verziói már telepítve vannak MSI-ből vagy WebPI-vel, a telepítő automatikusan eltávolítja őket. A modulok az `${env:ProgramFiles}\WindowsPowerShell\Modules` helyre lesznek telepítve. Az `AzureRM` és az `Azure` modul is telepítve lesz.

> [!NOTE]
> Ha a klasszikus Azure üzemi modellt használja, csak az `Azure` modult használja.

Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `AzureRM` modult az aktuális PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni. Az `AzureRM` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.
Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [felhasználói hitelesítő adatok a PowerShell-munkamenetek között történő megőrzését](context-persistence.md) ismertető részt.
