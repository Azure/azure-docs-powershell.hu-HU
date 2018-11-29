---
title: Az Azure PowerShell telepítése macOS vagy Linux rendszeren
description: Az Azure PowerShell telepítése macOS vagy Linux rendszeren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/29/2018
ms.locfileid: "52588111"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Az Azure PowerShell telepítése macOS vagy Linux rendszeren

Nem Windows rendszerű platformokon az Azure PowerShell futtatható a PowerShell Core 6-os verziójában. A PowerShell e verziója bármely, .NET Core-t támogató platformon történő használatra készült. Ezen platformokon történő használatra elérhető az Azure PowerShell egy .NET Standard-verziója.

> [!NOTE]
> Jelenleg a .NET Standardhez készült Azure PowerShell csak bétaverzióban érhető el.
> Ha problémákba ütközik vagy hibát észlel, jelentse be a problémát a GitHubon.
>
> * [Az Azure PowerShell problémái](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>A PowerShell Core telepítése

A PowerShell Core telepítési útmutatása eltér a macOS- és a Linux-disztribúciók esetében.
Részletes útmutatásokat a következő cikkekben talál:

* [A PowerShell Core telepítése macOS rendszeren](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [A PowerShell Core telepítése Linux rendszeren](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a>A .NET Standardhez készült Azure PowerShell telepítése

> [!IMPORTANT]
> A más cikkekben ismertetett `AzureRM` modul nem működik a PowerShell Core-ral.
> Telepítenie kell az `Az` modult, ha az Azure PowerShell minden funkcióját használni szeretné a PowerShell Core-ban.

A PowerShell Core tartalmazza az előre telepített PowerShellGet modult. Indítsa el a PowerShellt a következő paranccsal:

```bash
pwsh
```

Az Azure PowerShell telepítéséhez futtassa az alábbi parancsot:

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> Ha egy engedélyekkel kapcsolatos problémája akad, amikor megpróbálja telepíteni a modult, elképzelhető, hogy superuser-módban kell futtatnia a PowerShellt modulok telepítéséhez.
>
> ```bash
> sudo pwsh
> ```

Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként. A PSGallery első használatakor a következő üzenet jelenik meg:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.

## <a name="enable-aliases"></a>Aliasok engedélyezése

A meglévő `AzureRM` modullal való kompatibilitás érdekében az új `Az` modul képes visszamenőlegesen kompatibilis aliasokat létrehozni az `AzureRM` parancsmagokhoz. A modul első használata előtt állítsa be az aliasokat a következő paranccsal:

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

Ez csak a jelenlegi felhasználó aliasait állítja be. A parancsmagsúgóból megtudhatja, hogy milyen egyéb értékeket lehet megadni a `-Scope`-hoz az aliasok beállításának céljából.

> [!NOTE]
> Ha egy elérési úttal kapcsolatos problémája akad, bizonyosodjon meg róla, hogy az elérési út megtalálható a helyi rendszeren. A `CurrentUser` hatókör esetében ez a probléma a következő parancs `bash`-ban való futtatásával oldható meg:
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a>Bejelentkezés

Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `Az` modult a PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal. A modul importálásához __nincs__ szükség megemelt jogosultsági szintre.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni. Az `Az` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.
macOS és Linux rendszeren a `$Profile` környezeti változó segítségével használja a profilját. Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című részt.

## <a name="next-steps"></a>További lépések

Az Azure PowerShell használatával kapcsolatos további információkért tekintse meg az [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md) című cikket.
