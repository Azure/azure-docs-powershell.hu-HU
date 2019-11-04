---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 7f22a420068db87fa2c3c007bd36f515384162fb
ms.sourcegitcommit: ad7677d703a8512d371d3123dc7e541156b95cb8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/23/2019
ms.locfileid: "72814382"
---
# <a name="install-the-azure-powershell-module"></a>Az Azure PowerShell-modul telepítése

Ez a cikk az Azure PowerShell-modulok a PowerShellGet használatával való telepítését mutatja be. Az útmutatás Windows, macOS és Linux platformon használható. Az Az modulhoz jelenleg nem támogatottak más telepítési módszerek.

## <a name="requirements"></a>Követelmények

Az Azure PowerShell Windows rendszeren a PowerShell 5.1 vagy újabb, más platformon a PowerShell Core 6.x vagy újabb verziójával működik. Ha nem biztos abban, hogy rendelkezik-e PowerShell-lel, illetve macOS vagy Linux rendszert használ, [telepítse a PowerShell Core legújabb verzióját](/powershell/scripting/install/installing-powershell#powershell-core).

A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:

```powershell-interactive
$PSVersionTable.PSVersion
```

Az Azure PowerShell futtatása PowerShell 5.1-ben Windows rendszeren:

1. Frissítsen a [Windows PowerShell 5.1-re](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell), ha szükséges. Ha Windows 10 rendszert használ, már telepítve van a PowerShell 5.1.
2. Telepítse a [.NET-keretrendszer 4.7.2-es vagy újabb verzióját](/dotnet/framework/install).

Nincsenek további követelmények az Azure PowerShellhez a PowerShell Core használata esetén.

## <a name="install-the-azure-powershell-module"></a>Az Azure PowerShell-modul telepítése

> [!WARNING]
> Az AzureRM és az Az modul __nem__ lehet egyszerre telepítve a PowerShell 5.1-hez ugyanazon a Windows rendszeren. Ha az AzureRM-nek továbbra is elérhetőnek kell maradnia a rendszeren, telepítse a PowerShell Core 6.x vagy újabb verziójához készült Az modult. Ehhez [telepítse a PowerShell Core 6.x vagy újabb](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) verzióját, majd kövesse az itt ismertetett utasításokat a PowerShell Core-terminálban.

Ajánlott csak az aktív felhasználó számára telepíteni:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Ha a rendszer összes felhasználója számára szeretné telepíteni, akkor rendszergazdai jogosultságokra lesz szüksége. Egy rendszergazdaként, illetve macOS vagy Linux rendszeren a `sudo` paranccsal indított, emelt szintű PowerShell-munkamenetben:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként. A PSGallery első használatakor a következő üzenet jelenik meg:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.

Az Az modul az Azure PowerShell-parancsmagok összesített modulja. A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.

## <a name="install-offline"></a>Offline telepítés

Néhány környezetben nem lehet csatlakozni a PowerShell-galériához. Ezekben a helyzetekben offline telepítést végezhet az alábbi módszerek valamelyikével:

* Töltse le a modulokat egy másik helyre, és azt a helyet használja a hálózat telepítési forrásaként. Ez bonyolult folyamat lehet, de lehetővé teszi, hogy a PowerShell-modulokat egyetlen kiszolgálón vagy fájlmegosztáson gyorsítótárazza, így a PowerShellGet használatával bármely leválasztott rendszeren üzembe helyezheti őket. Megtudhatja, hogyan állíthat be helyi adattárat, és hogyan telepíthet leválasztott rendszerekre [helyi PowerShellGet-adattárakkal](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).
* [Letöltheti az Azure PowerShell MSI-t](install-az-ps-msi.md) a hálózathoz csatlakoztatott egyik gépre, majd a telepítőt olyan rendszerekre másolhatja, amelyek nem férnek hozzá a PowerShell-galériához. Ne feledje, hogy az MSI-telepítő csak a PowerShell 5.1-hez, Windows rendszeren használható.
* A modult a [Save-Module](/powershell/module/PowershellGet/Save-Module) paranccsal egy fájlmegosztásra mentheti, vagy egy másik forrásra mentheti, és más gépekre másolhatja:
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Hibaelhárítás

Az alábbiakban néhány, az Azure PowerShell modul telepítése során gyakran jelentkező problémáról olvashat. Ha itt nem szereplő problémába ütközik, [jelentse be a problémát a GitHubon](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Egy proxy blokkolja a kapcsolatot

Ha `Install-Module`-hibaüzenet jelenik meg, amely jelzi, hogy a PowerShell-galéria nem érhető el, lehetséges, hogy egy proxy mögött van. A különböző operációs rendszereknek eltérő követelményei vannak a rendszerszintű proxy konfigurálásához, amelynek részleteit itt most nem tárgyaljuk. A proxybeállításokkal és az operációs rendszer beállításaival kapcsolatban vegye fel a kapcsolatot a rendszergazdával.

Lehetséges, hogy maga a PowerShell nem konfigurálható a proxy automatikus használatára. PowerShell 5.1 vagy újabb változat esetén konfigurálja a proxyt PowerShell-munkamenet használatára az alábbi paranccsal:

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Ha az operációs rendszer hitelesítő adatai megfelelően vannak konfigurálva, a PowerShell-kéréseket a proxyn keresztül irányítja át.
Ha azt szeretné, hogy ezt a beállítást a munkamenetek között is megőrizze a rendszer, adja hozzá ezt a parancsot egy [PowerShell-profilhoz](/powershell/module/microsoft.powershell.core/about/about_profiles).

A csomag telepítéséhez a proxynak engedélyeznie kell az alábbi címekre irányuló HTTPS-kapcsolatokat:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Bejelentkezés

Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult az `Import-Module Az` segítségével. A modul felépítéséből adódóan ez eltarthat néhány másodpercig.

Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni. Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.

## <a name="update-the-azure-powershell-module"></a>Az Azure PowerShell-modul frissítése

Az Az modul csomagolásának módja miatt az [Update-Module](/powershell/module/powershellget/update-module) parancs nem fogja megfelelően frissíteni a telepítést. Az Az modul telepítésekor a modul összegyűjti és telepíti az összes függő almodult, és megadja az egyes szolgáltatások parancsmagjait.
Ez azt jelenti, hogy az Azure PowerShell-modul frissítéséhez nem elég __frissíteni__ azt, hanem __újra kell telepítenie__. Ez ugyanúgy történik, mint a telepítés, de előfordulhat, hogy hozzá kell adnia a `-Force` argumentumot:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

Bár ez felülírhatja a telepített modulokat, még így is előfordulhat hogy maradnak régebbi verziók a rendszeren.
Az Azure PowerShell régebbi verzióinak eltávolításáról [Az Azure PowerShell-modul eltávolítása](uninstall-az-ps.md) című szakaszban olvashat.

## <a name="use-multiple-versions-of-azure-powershell"></a>Az Azure PowerShell több verziójának használata

Lehetőség van az Azure PowerShell több verziójának telepítésére. Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszt.

Az `Az` modul adott verziójának telepítéséhez vagy betöltéséhez használja a `-RequiredVersion` argumentumot:

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

Ha a modul több verziója is telepítve van, alapértelmezés szerint a modul automatikus betöltésével és az `Import-Module` használatával töltse be a legújabb verziót.

## <a name="provide-feedback"></a>Visszajelzés küldése

Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).
A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.

## <a name="next-steps"></a>További lépések

Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.
Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.
