---
title: "Az Azure PowerShell telepítése és konfigurálása | Microsoft Docs"
description: "Az Azure PowerShell telepítése és konfigurálása az első használathoz."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/17/2017
ms.openlocfilehash: 86bf3ab84b706d44b46f420d07570069f65bde72
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/29/2017
---
# <a name="install-and-configure-azure-powershell"></a>Az Azure PowerShell telepítése és konfigurálása

Az Azure PowerShell-t a PowerShell-galériából javasolt telepíteni.

## <a name="step-1-install-powershellget"></a>1. lépés: A PowerShellGet telepítése

Ahhoz, hogy elemeket telepíthessen a PowerShell-galériából, szükség van a PowerShellGet modulra. Győződjön meg arról, hogy rendelkezik a PowerShellGet megfelelő verziójával, és az egyéb rendszerkövetelmények is teljesülnek. A következő parancs futtatásával ellenőrizze, hogy telepítve van-e a PowerShellGet a rendszerben.

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

Az alábbihoz hasonló kimenetnek kell megjelennie:

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Ha a PowerShellGet nincs telepítve, akkor tekintse meg a jelen cikk [A PowerShellGet-modul beszerzése](#how-to-get-powershellget) című szakaszát.

> [!NOTE]
> A PowerShellGet használatához olyan végrehajtási szabályzatra van szükség, amely lehetővé teszi a szkriptek futtatását. A PowerShell végrehajtási házirendjével kapcsolatos további információk: [A végrehajtási házirendek áttekintése](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies).

## <a name="step-2-install-azure-powershell"></a>2. lépés: Az Azure PowerShell telepítése

Az Azure Powershell PowerShell-galériából történő telepítéséhez emelt szintű jogosultságok szükségesek. Futtassa a következő parancssort egy emelt szintű PowerShell-munkamenetből:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM
```

Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható tárházaként. A PSGallery első használatakor a következő üzenet jelenik meg:

```
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

A telepítés folytatásához válassza az „Igen” vagy az „Igen, mindet” lehetőséget.

> [!NOTE]
> Ha a NuGet 2.8.5.201-esnél régebbi verzióval rendelkezik, a rendszer a legújabb verzió letöltését és telepítését kéri.

Az AzureRM-modul az Azure Resource Manager-parancsmagok összesített modulja. Az AzureRM modul telepítésekor a rendszer minden korábban nem telepített Azure PowerShell modult letölt a PowerShell-galériából.

Ha az Azure PowerShell korábbi verziójával rendelkezik, hibaüzenetet kaphat. A probléma megoldásához tekintse meg a cikk [Frissítés az Azure PowerShell új verziójára ](#update-azps) című részét.

## <a name="step-3-load-the-azurerm-module"></a>3. lépés: Az AzureRM-modul betöltése
A modul telepítése után be kell tölteni a azt a PowerShell-munkamenetbe. Ezt a lépést normál (nem emelt szintű) PowerShell-munkamenetben kell végrehajtani. A modulok az `Import-Module` parancsmaggal, az alábbi módon tölthetők be:

```powershell
Import-Module AzureRM
```

## <a name="next-steps"></a>Következő lépések

Az Azure PowerShell használatával kapcsolatos további információkat az alábbi cikkekben olvashat:

* [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a>Hibák jelentése és visszajelzés

Ha az eszköz használata során bármilyen hibát tapasztal, jelentse be a problémát a GitHub-adattár [Hibák](https://github.com/Azure/azure-powershell/issues) szakaszában. A parancssorból a `Send-Feedback` parancsmaggal küldhet visszajelzést.

## <a name="frequently-asked-questions"></a>Gyakori kérdések

### <a name="how-to-get-powershellget"></a>A PowerShellGet beszerzése

|Operációs rendszer verziója|Telepítési utasítások|
|---|---|
|Windows 10 vagy Windows Server 2016 rendszert használok|Az operációs rendszer részét képező Windows Management Framework (WMF) 5.0 beépített eleme|
|Frissíteni szeretnék a PowerShell 5-ös verziójára|[A WMF legújabb verziójának telepítése](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|A PowerShell 3-as vagy 4-es verziójával rendelkező Windows-verziót használok|[A PackageManagement-modulok beszerzése](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>Az Azure PowerShell verziószámának ellenőrzése

Habár javasoljuk, hogy a lehető leghamarabb frissítsen a legújabb verzióra, az Azure PowerShell számos verziója támogatott. Az Azure PowerShell telepített verziójának megállapításához futtassa a következő parancsot a parancssorban: `Get-Module AzureRM`.

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>Klasszikus telepítési módszerek támogatása

Ha van olyan üzemelő példánya, amely a klasszikus telepítési modellt használja, akkor az Azure PowerShell Service Management verzióját telepítheti. További információ: [Az Azure PowerShell Service Management moduljának telepítése](/powershell/azure/servicemanagement/install-azure-ps). Az Azure és AzureRM-modulok ugyanazokat a függőségeket használják. Ha az Azure- és az AzureRM-modult egyaránt használja, minden csomagnak ugyanazt a verzióját kell telepítenie.

### <a id="update-azps"></a>Frissítés az Azure PowerShell új verziójára

Ha az Azure PowerShell olyan korábbi verziója van telepítve, amely a Szolgáltatáskezelési modult tartalmazza, akkor a következő hibaüzenetet kaphatja:

```
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

Ahogy a hibaüzenetben is olvasható, a modul telepítéséhez az -AllowClobber paramétert kell használnia. Használja az alábbi parancsot:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM -AllowClobber
```

További információért tekintse meg az [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) súgótémakört.

### <a name="installing-module-versions-side-by-side"></a>Modulverziók párhuzamos telepítése

A PowerShellGet-metódus az egyetlen módszer, amely támogatja több verzió telepítését. Előfordulhat például, hogy rendelkezik az Azure PowerShell előző verziójával írt szkriptekkel, amelyek frissítésére nincs ideje vagy erőforrása. A következő parancsok bemutatják, hogy telepítheti az Azure PowerShell több verzióját:

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Egy PowerShell-munkamenetbe csak egyetlen modulverzió tölthető be. Meg kell nyitnia egy új PowerShell-ablakot, és az `Import-Module` parancs használatával importálnia kell az AzureRM-parancsmagok egy adott verzióját:

```powershell
Import-Module AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> A 2.1.0-ás és az 1.2.6-os modulverziók az elsők, amelyeket párhuzamos telepítésre és használatra terveztek. Az Azure PowerShell korábbi verziónak betöltésekor az **AzureRM.Profile**-modul nem kompatibilis verziói töltődnek be. Ezért a parancsmagok minden parancsmag végrehajtásánál bejelentkezést fognak kérni.

### <a name="other-installation-methods"></a>Egyéb telepítési módszerek

A Webplatform-telepítő vagy az MSI-csomag használatával történő telepítéssel kapcsolatos további információkért lásd: [Egyéb telepítési módszerek](other-install.md)
