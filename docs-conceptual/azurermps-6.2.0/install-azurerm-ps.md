---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323101"
---
# <a name="install-azure-powershell-with-powershellget"></a>Az Azure PowerShell telepítése a PowerShellGet segítségével

Ez a cikk az Azure PowerShell-modulok PowerShellGet segítségével való telepítésének lépéseit ismerteti Windows-környezetben.  Ez az Azure PowerShell előnyben részesített telepítési módja, de ha mégis inkább a Webplatform-telepítővel vagy az MSI-csomaggal szeretné telepíteni, tekintse meg az [egyéb telepítési módszerekkel kapcsolatos](other-install.md) szakaszt.

Ha a macOS vagy Linux rendszeren szeretné használni az Azure PowerShellt, tekintse meg a következő cikket: [Az Azure PowerShell telepítése és konfigurálása macOS és Linux rendszeren](install-azurermps-maclinux.md).

## <a name="system-requirements"></a>Rendszerkövetelmények

Az Azure PowerShell 6.1.0-s verziójához szükség van a PowerShell 5.0-s (vagy újabb) verziójára. A PowerShell 5.0-s verziójára történő frissítéssel kapcsolatos információkért lásd a [meglévő Windows PowerShell frissítésével](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell) kapcsolatos szakaszt.

A PowerShellGet automatikusan települ a PowerShell 5.0 részeként.

## <a name="install-or-update-the-azure-powershell-module"></a>Az Azure PowerShell-modul telepítése vagy frissítése

Az Azure Powershell PowerShell-galériából történő telepítéséhez emelt szintű jogosultságok szükségesek. Futtassa a következő parancssort egy emelt szintű PowerShell-munkamenetből:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> Ez a parancs frissíti a meglévő Azure PowerShell-telepítéseket. Ha több verziót kell telepítenie, tekintse meg a gyakori kérdések között a [Telepíthetek több Azure PowerShell-verziót?](#multiple-versions) kérdésre adott választ.

Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként. A PSGallery első használatakor a következő üzenet jelenik meg:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

A telepítés folytatásához válassza az „Igen” vagy az „Igen, mindet” lehetőséget.

> [!NOTE]
> Ha a NuGet 2.8.5.201-esnél régebbi verzióval rendelkezik, a rendszer a legújabb verzió letöltését és telepítését kéri.

Az AzureRM-modul az Azure Resource Manager-parancsmagok összesített modulja. Az AzureRM-modul telepítésekor a rendszer minden korábban nem telepített Azure PowerShell-modult letölt a PowerShell-galériából.

## <a name="load-the-azure-powershell-module"></a>Az Azure PowerShell-modul betöltése

A modul telepítése után be kell tölteni a azt a PowerShell-munkamenetbe. Ezt a lépést normál (nem emelt szintű) PowerShell-munkamenetben kell végrehajtani. A modulok az `Import-Module` parancsmaggal, az alábbi módon tölthetők be:

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a>Hibák jelentése és visszajelzés

Ha az eszköz használata során bármilyen hibát tapasztal, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues). A parancssorból a `Send-Feedback` parancsmaggal küldhet visszajelzést.

## <a name="next-steps"></a>További lépések

Az Azure PowerShell használatával kapcsolatos további információkat az alábbi cikkekben olvashat:

* [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md)

## <a name="frequently-asked-questions"></a>Gyakori kérdések

### <a id="helpmechoose"></a>Hogyan ellenőrizhetem az Azure PowerShell verziószámát?

Habár javasoljuk, hogy a lehető leghamarabb frissítsen a legújabb verzióra, az Azure PowerShell számos verziója támogatott. Az Azure PowerShell telepített verziójának megállapításához futtassa a következő parancsot a parancssorban: `Get-Module AzureRM`.

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a>Használhatom az Azure PowerShellt klasszikus Azure üzemi modell esetében?

Ha van olyan üzemelő példánya, amely a klasszikus telepítési modellt használja, akkor az Azure PowerShell Service Management verzióját telepítheti. További információ: [Az Azure PowerShell Service Management moduljának telepítése](/powershell/azure/servicemanagement/install-azure-ps). Az Azure és AzureRM-modulok ugyanazokat a függőségeket használják. Ha az Azure- és az AzureRM-modult egyaránt használja, minden csomagnak ugyanazt a verzióját kell telepítenie.

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><a name="multiple-versions"/>Telepíthetek több Azure PowerShell-verziót?

A PowerShellGet az egyetlen telepítési módszer, amely támogatja több verzió telepítését. Több verzió telepítéséhez hozzáadhatja a `-RequiredVersion` paramétert az `Install-Module` parancsmaghoz. Például a 6.1.0-s és az 1.2.9-es verzió telepítése:

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Egy PowerShell-munkamenetbe csak egyetlen modulverzió tölthető be. Nyisson meg egy új PowerShell-ablakot, és az `Import-Module` paranccsal importálja az Azure PowerShell-modul egy adott verzióját.

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> A 2.1.0-ás és az 1.2.6-os modulverziók az elsők, amelyeket párhuzamos telepítésre és használatra terveztek. Az Azure PowerShell korábbi verziónak betöltésekor az **AzureRM.Profile**-modul nem kompatibilis verziói töltődnek be. Ezért a parancsmagok minden parancsmag végrehajtásánál bejelentkezést fognak kérni.
