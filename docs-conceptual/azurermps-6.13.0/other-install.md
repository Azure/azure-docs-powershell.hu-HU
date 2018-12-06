---
title: Az Azure PowerShell telepítésének egyéb módjai
description: Az Azure PowerShell telepítése a PowerShellGet nélkül, MSI használatával
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: b442da364a01cd6022c14cbb32a9b633676ca8c7
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828858"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Az Azure PowerShell telepítése Windows rendszeren MSI-vel

Ez a cikk bemutatja, hogyan telepíthető az Azure PowerShell Windows rendszeren egy MSI-telepítő használatával.  
Csak akkor alkalmazza ezeket a telepítési módszereket, ha a rendszer számára szükséges. Az Azure PowerShell Windows rendszeren való telepítésének ajánlott módja a PowerShellGet használata. Útmutatás az Azure PowerShell PowerShellGet segítségével való telepítéséhez: [Az Azure PowerShell telepítése a PowerShellGet segítségével](install-azurerm-ps.md).

> [!NOTE]
> A Webplatform-telepítőt használó telepítési módszer már nem érhető el az Azure PowerShell 6.x-es vagy újabb verzióihoz. Ha a Webplatform-telepítőt kell használnia, fontolja meg helyette az MSI használatát, vagy telepítheti az Azure PowerShell egy korábbi verzióját.

Ha Linux- vagy macOS-környezetben végzi a telepítést, tekintse meg [Az Azure PowerShell telepítése macOS vagy Linux rendszeren](install-azurermps-maclinux.md) szakaszt.

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Telepítés vagy frissítés Windows rendszeren az MSI-csomaggal

Az Azure PowerShell telepíthető a [GitHubról](https://github.com/Azure/azure-powershell/releases/latest) elérhető MSI-fájllal is. Ha az Azure-modulok korábbi verziói már telepítve vannak MSI-ként, a telepítő automatikusan eltávolítja őket. Az MSI-csomag a következő helyre telepíti a modulokat: `${env:ProgramFiles}\WindowsPowerShell\Modules`. Az `AzureRM` és az `Azure` modul is telepítve lesz.

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
