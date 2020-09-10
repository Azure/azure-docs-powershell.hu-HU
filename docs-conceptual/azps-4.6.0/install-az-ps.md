---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/14/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: a263f1d363b3d1a1cce433a6112c55afe65262a4
ms.sourcegitcommit: 2f1e3c275626fba1c4275cae8ef1d13b11f55735
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/04/2020
ms.locfileid: "89449993"
---
# <a name="install-azure-powershell"></a>Az Azure PowerShell telepítése

Ez a cikk az Azure PowerShell-modulok a [PowerShellGet](/powershell/scripting/gallery/installing-psget) használatával való telepítését ismerteti. Az útmutatás Windows, macOS és Linux platformon használható.

Az Azure PowerShell az Azure [Cloud Shellben](/azure/cloud-shell/overview) is elérhető, és mostantól a [Docker-rendszerképek](azureps-in-docker.md) előre telepítve tartalmazzák.

## <a name="requirements"></a>Követelmények

> [!NOTE]
> A PowerShell az Azure PowerShell-lel történő használatához az összes platformon a PowerShell 7.x vagy újabb verziója javasolt.

Az Azure PowerShell kompatibilis a PowerShell 6.2.4-es vagy újabb verziójával az összes platformon. Windows rendszeren a PowerShell 5.1-es verziójával is támogatott. Telepítse az operációs rendszeréhez elérhető [legújabb PowerShell-verziót](/powershell/scripting/install/installing-powershell). Az Azure PowerShell nem támaszt további követelményeket a PowerShell 6.2.4-es vagy újabb verziója használata esetén.

A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

Az Azure PowerShell használata PowerShell 5.1-ben Windows rendszeren:

1. Frissítsen a [Windows PowerShell 5.1-re](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).
   Ha a Windows 10 1607-es vagy újabb verzióját használja, már telepítve van a PowerShell 5.1.
2. Telepítse a [.NET-keretrendszer 4.7.2-es vagy újabb verzióját](/dotnet/framework/install).
3. Győződjön meg arról, hogy a PowerShellGet legújabb verziójával rendelkezik. Futtassa az `Install-Module -Name PowerShellGet -Force` parancsot.

## <a name="install-the-azure-powershell-module"></a>Az Azure PowerShell-modul telepítése

> [!WARNING]
> Az AzureRM és az Az modul nem lehet egyszerre telepítve a PowerShell 5.1-hez ugyanazon a Windows rendszeren. Ha az AzureRM-nek továbbra is elérhetőnek kell maradnia a rendszeren, telepítse a PowerShell 6.2.4-es vagy újabb verziójához készült Az modult.

Az előnyben részesített telepítési módszer a PowerShellGet-parancsmagok használata. Csak az aktuális felhasználó számára telepítse az Az modult. Ez az ajánlott telepítési hatókör. Ez a módszer Windows, macOS és Linux platformon ugyanúgy működik. Futtassa az alábbi parancsot egy PowerShell-munkamenetből:

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
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

A modulnak a rendszer összes felhasználója számára történő telepítéséhez emelt szintű jogosultságokra van szükség. A PowerShell-munkamenetet a **Futtatás rendszergazdaként** paranccsal indítsa el Windows, illetve a `sudo` paranccsal macOS vagy Linux rendszeren:

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

Az Az modul az Azure PowerShell-parancsmagok összesített modulja. A modul telepítésével letölti az összes általánosan elérhető Az PowerShell-modult, és használatra elérhetővé teszi a parancsmagjaikat.

## <a name="install-offline"></a>Offline telepítés

Néhány környezetben nem lehet csatlakozni a PowerShell-galériához. Ezekben a helyzetekben offline telepítést végezhet az alábbi módszerek valamelyikével:

* Töltse le a modulokat a hálózat egy másik helyére, és azt a helyet használja a telepítési forrásként.
  Ez a módszer lehetővé teszi, hogy a PowerShell-modulokat egyetlen kiszolgálón vagy fájlmegosztáson gyorsítótárazza, így a PowerShellGet használatával bármely leválasztott rendszeren üzembe helyezheti őket. Megtudhatja, hogyan állíthat be helyi adattárat, és hogyan telepíthet leválasztott rendszerekre [helyi PowerShellGet-adattárakkal](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).
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
> Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult az `Import-Module -Name Az` segítségével.
> A modul felépítéséből adódóan ez eltarthat néhány másodpercig.

Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni. Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.

## <a name="update-the-azure-powershell-module"></a>Az Azure PowerShell-modul frissítése

PowerShell-modulok frissítéséhez ugyanazt a módszert használja, mint a modul telepítéséhez. Ha eredetileg például az `Install-Module` parancsmagot használta, akkor használja az [Update-Module](/powershell/module/powershellget/update-module) parancsmagot a legújabb verzió beszerzéséhez. Ha eredetileg az MSI-csomagot használta, akkor töltse le és telepítse az új MSI-csomagot.

A PowerShellGet-parancsmagok nem tudnak MSI-csomagból telepített modulokat frissíteni. Az MSI-csomagok nem frissítenek a PowerShellGettel telepített modulokat. Ha bármilyen problémába ütközik a PowerShellGettel történő frissítés közben, akkor a **frissítés** helyett **újra kell telepítenie** a modult. Az újratelepítés ugyanúgy történik, mint a telepítés, de hozzá kell adnia a `-Force` paramétert:

```powershell
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

Az MSI-alapú telepítésektől eltérően a PowerShellGettel történő telepítés vagy frissítés nem távolítja el a rendszeren esetlegesen megtalálható régebbi verziókat. Az Azure PowerShell régebbi verzióinak eltávolításáról [az Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszban olvashat. Az MSI-alapú telepítésekkel kapcsolatban [az Azure PowerShell MSI-vel történő telepítését](install-az-ps-msi.md) ismertető témakörben tekinthet meg további információt.

## <a name="use-multiple-versions-of-azure-powershell"></a>Az Azure PowerShell több verziójának használata

Lehetőség van az Azure PowerShell több verziójának telepítésére. Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
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

## <a name="use-multiple-repositories-with-powershellget"></a>Több adattár használata a PowerShellGettel

Az **Adattár** paraméter akkor szükséges, ha további adattárakat adott hozzá a PowerShellGethez a rendszeren, és az Az modul egynél több adattárban is megtalálható.

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -Repository PSGallery -AllowClobber -Force
}
```

## <a name="provide-feedback"></a>Visszajelzés küldése

Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues). A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.

## <a name="next-steps"></a>Következő lépések

Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt. Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.
