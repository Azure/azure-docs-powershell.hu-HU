---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.openlocfilehash: 7a25270566f5e856ee44c4c191a47a3e7334508b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740252"
---
# <a name="install-azure-powershell"></a>Az Azure PowerShell telepítése

Ez a cikk az Azure PowerShell-modulok a PowerShellGet használatával való telepítését ismerteti. Az útmutatás Windows, macOS és Linux platformon használható.

Az Azure PowerShell az Azure [Cloud Shellben](/azure/cloud-shell/overview) is elérhető, és mostantól a [Docker-rendszerképek](azureps-in-docker.md) előre telepítve tartalmazzák.

## <a name="requirements"></a>Követelmények

Az Azure PowerShell Windows rendszeren a PowerShell 5.1 vagy újabb, más platformon a PowerShell Core 6.x vagy újabb verziójával működik. Telepítenie kell a PowerShell Core-nak az operációs rendszerhez elérhető [legújabb verzióját](/powershell/scripting/install/installing-powershell#powershell-core). Az Azure PowerShell nem támaszt további követelményeket a PowerShell Core használata esetén.

A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:

```powershell-interactive
$PSVersionTable.PSVersion
```

Az Azure PowerShell használata PowerShell 5.1-ben Windows rendszeren:

1. Frissítsen a [Windows PowerShell 5.1-re](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell), ha szükséges. Ha Windows 10 rendszert használ, már telepítve van a PowerShell 5.1.
2. Telepítse a [.NET-keretrendszer 4.7.2-es vagy újabb verzióját](/dotnet/framework/install).
3. Győződjön meg arról, hogy a PowerShellGet legújabb verziójával rendelkezik. Futtassa az `Update-Module PowerShellGet -Force` parancsot.

## <a name="install-the-azure-powershell-module"></a>Az Azure PowerShell-modul telepítése

Az előnyben részesített telepítési módszer a PowerShellGet-parancsmagok használata. Ez a módszer Windows, macOS és Linux platformon ugyanúgy működik. Futtassa az alábbi parancsot egy PowerShell-munkamenetből:

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként. A PSGallery első használatakor a következő üzenet jelenik meg:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.

Az Az modul az Azure PowerShell-parancsmagok összesített modulja. A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.

> [!WARNING]
> Az AzureRM és az Az modul nem lehet egyszerre telepítve a PowerShell 5.1-hez ugyanazon a Windows rendszeren. Ha az AzureRM-nek továbbra is elérhetőnek kell maradnia a rendszeren, telepítse a PowerShell Core 6.x vagy újabb verziójához készült Az modult.

Először [telepítse a PowerShell Core 6.x vagy újabb verzióját](/powershell/scripting/install/installing-powershell-core-on-windows).

Ezután telepítse az Az modult csak az aktuális felhasználó számára egy PowerShell Core-munkamenetből. Ez az ajánlott telepítési hatókör.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

A modulnak a rendszer összes felhasználója számára történő telepítéséhez emelt szintű jogosultságokra van szükség. A PowerShell-munkamenetet a **Futtatás rendszergazdaként** paranccsal indítsa el Windows, illetve a `sudo` paranccsal macOS vagy Linux rendszeren:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

## <a name="install-offline"></a>Offline telepítés

Néhány környezetben nem lehet csatlakozni a PowerShell-galériához. Ezekben a helyzetekben offline telepítést végezhet az alábbi módszerek valamelyikével:

* Töltse le a modulokat a hálózat egy másik helyére, és azt a helyet használja a telepítési forrásként.
  Ez lehetővé teszi, hogy a PowerShell-modulokat egyetlen kiszolgálón vagy fájlmegosztáson gyorsítótárazza, így a PowerShellGet használatával bármely leválasztott rendszeren üzembe helyezheti őket. Megtudhatja, hogyan állíthat be helyi adattárat, és hogyan telepíthet leválasztott rendszerekre [helyi PowerShellGet-adattárakkal](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).
* [Letöltheti az Azure PowerShell MSI-t](install-az-ps-msi.md) a hálózathoz csatlakoztatott egyik gépre, majd a telepítőt olyan rendszerekre másolhatja, amelyek nem férnek hozzá a PowerShell-galériához. Ne feledje, hogy az MSI-telepítő csak a PowerShell 5.1-hez, Windows rendszeren használható.
* A modult a [Save-Module](/powershell/module/PowershellGet/Save-Module) paranccsal egy fájlmegosztásra mentheti, vagy egy másik forrásra mentheti, és más gépekre másolhatja:

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Hibaelhárítás

Az alábbiakban néhány, az Azure PowerShell modul telepítése során gyakran jelentkező problémáról olvashat. Ha itt nem szereplő problémába ütközik, [jelentse be a problémát a GitHubon](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Egy proxy blokkolja a kapcsolatot

Ha `Install-Module`-hibaüzenet jelenik meg, amely jelzi, hogy a PowerShell-galéria nem érhető el, lehetséges, hogy egy proxy mögött van. A különböző operációs rendszerek és hálózati környezetek eltérő követelményeket támasztanak a rendszerszintű proxy konfigurálására vonatkozóan. A proxybeállításokkal és a környezet számára történő konfigurálásukkal kapcsolatban vegye fel a kapcsolatot a rendszergazdával.

Lehetséges, hogy maga a PowerShell nem konfigurálható a proxy automatikus használatára. A PowerShell 5.1-es vagy újabb verziója esetén konfigurálja a PowerShell-munkamenetet egy proxy használatára az alábbi parancsokkal:

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Ha az operációs rendszer hitelesítő adatai megfelelően vannak konfigurálva, ez a konfiguráció a proxyn keresztül irányítja át PowerShell-kéréseket. Ha azt szeretné, hogy ezt a beállítást a munkamenetek között is megőrizze a rendszer, adja hozzá a parancsokat a [PowerShell-profilhoz](/powershell/module/microsoft.powershell.core/about/about_profiles).

A csomag telepítéséhez a proxynak engedélyeznie kell az alábbi címekre irányuló HTTPS-kapcsolatokat:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Bejelentkezés

Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult az `Import-Module Az` segítségével. A modul felépítéséből adódóan ez eltarthat néhány másodpercig.

Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni. Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.

## <a name="update-the-azure-powershell-module"></a>Az Azure PowerShell-modul frissítése

PowerShell-modulok frissítéséhez ugyanazt a módszert használja, mint a modul telepítéséhez. Ha eredetileg például az `Install-Module` parancsmagot használta, akkor használja az [Update-Module](/powershell/module/powershellget/update-module) parancsmagot a legújabb verzió beszerzéséhez. Ha eredetileg az MSI-csomagot használta, akkor töltse le és telepítse az új MSI-csomagot.

A PowerShellGet-parancsmagok nem tudnak MSI-csomagból telepített modulokat frissíteni. Az MSI-csomagok nem frissítenek a PowerShellGettel telepített modulokat. Ha bármilyen problémába ütközik a PowerShellGettel történő frissítés esetén, akkor a **frissítés** helyett **újra kell telepítenie** a modult. Az újratelepítés ugyanúgy történik, mint a telepítés, de hozzá kell adnia a `-Force` paramétert:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

Az MSI-alapú telepítésektől eltérően a PowerShellGettel történő telepítés vagy frissítés nem távolítja el a rendszeren esetlegesen megtalálható régebbi verziókat. Az Azure PowerShell régebbi verzióinak eltávolításáról [az Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszban olvashat. Az MSI-alapú telepítésekkel kapcsolatban [az Azure PowerShell MSI-vel történő telepítését](install-az-ps-msi.md) ismertető témakörben tekinthet meg további információt.

## <a name="use-multiple-versions-of-azure-powershell"></a>Az Azure PowerShell több verziójának használata

Lehetőség van az Azure PowerShell több verziójának telepítésére. Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszt.

Ha a modul több verziója is telepítve van, alapértelmezés szerint a modul automatikus betöltésével és az `Import-Module` használatával töltse be a legújabb verziót.

Az `Az` modul adott verziójának telepítéséhez vagy betöltéséhez használja a `-RequiredVersion` paramétert:

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a>Visszajelzés küldése

Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues). A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.

## <a name="next-steps"></a>Következő lépések

Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt. Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.
