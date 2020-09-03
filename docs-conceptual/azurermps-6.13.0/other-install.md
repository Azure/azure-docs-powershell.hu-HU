---
title: Az Azure PowerShell telepítésének egyéb módjai
description: Az Azure PowerShell telepítése a PowerShellGet nélkül, MSI használatával
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 41edefe96ecebf0a7276cdc3b4510acd7e8098f4
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241594"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Az Azure PowerShell telepítése Windows rendszeren MSI-vel

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Ez a cikk bemutatja, hogyan telepíthető az Azure PowerShell Windows rendszeren egy MSI-telepítő használatával.
Csak akkor alkalmazza ezeket a telepítési módszereket, ha a rendszer számára szükséges. Az Azure PowerShell Windows rendszeren való telepítésének ajánlott módja a PowerShellGet használata. Útmutatás az Azure PowerShell PowerShellGet segítségével való telepítéséhez: [Az Azure PowerShell telepítése a PowerShellGet segítségével](install-azurerm-ps.md).

> [!NOTE]
> A Webplatform-telepítőt használó telepítési módszer már nem érhető el az Azure PowerShell 6.x-es vagy újabb verzióihoz. Ha a Webplatform-telepítőt kell használnia, fontolja meg helyette az MSI használatát, vagy telepítheti az Azure PowerShell egy korábbi verzióját.

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Telepítés vagy frissítés Windows rendszeren az MSI-csomaggal

A Windows PowerShell 5.x verziójához készült Azure PowerShell telepíthető a [GitHubról](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018) elérhető MSI-fájllal is. Ha az Azure-modulok korábbi verziói már telepítve vannak MSI-ként, a telepítő automatikusan eltávolítja őket. Az MSI-csomag a következő helyre telepíti a modulokat: `${env:ProgramFiles}\WindowsPowerShell\Modules`. Az `AzureRM` és az `Azure` modul is telepítve lesz.

> [!NOTE]
> Ha a klasszikus Azure üzemi modellt használja, csak az `Azure` modult használja.

Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult a(z) `Import-Module AzureRM` segítségével. A modul felépítéséből adódóan ez eltarthat néhány másodpercig.

Ezt a lépést minden új PowerShell-munkamenet esetében meg kell ismételni. Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.
