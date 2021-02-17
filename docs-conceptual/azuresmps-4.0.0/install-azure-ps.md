---
title: Az Azure PowerShell Service Management moduljának telepítése és konfigurálása | Microsoft Docs
description: Az Azure PowerShell telepítése és konfigurálása az első használathoz.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 23ea4bcbd182cf1b063f2ae90921217de74a7044
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401521"
---
# <a name="installing-the-azure-powershell-service-management-module"></a>Az Azure PowerShell Service Management moduljának telepítése

Az Azure PowerShell telepítésének előnyben részesített módszere a [PowerShell-galériából](https://www.powershellgallery.com/) történő telepítés.

## <a name="step-1-install-powershellget"></a>1\. lépés: A PowerShellGet telepítése

Ahhoz, hogy elemeket telepíthessen a PowerShell-galériából, szükség van a PowerShellGet modulra. Győződjön meg arról, hogy rendelkezik a PowerShellGet megfelelő verziójával, és az egyéb rendszerkövetelmények is teljesülnek. A következő parancs futtatásával ellenőrizze, hogy telepítve van-e a PowerShellGet a rendszerben.

```powershell
Get-InstalledModule PowerShellGet -AllVersions | Select-Object Name,Version,Path
```

Az alábbihoz hasonló kimenetnek kell megjelennie:

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Ha a PowerShellGet nincs telepítve, akkor tekintse meg [A PowerShellGet beszerzése](#how-to-get-powershellget) című szakaszt.

## <a name="step-2-install-azure-powershell"></a>2\. lépés: Az Azure PowerShell telepítése

Futtassa az alábbi parancsot rendszergazdaként a Windows PowerShell-konzolból:

```powershell
Install-Module Azure
```

Az Azure-modul az Azure Resource Manager-parancsmagok összesített modulja. Az AzureRM-modul telepítésekor a rendszer minden olyan Azure-modult letölt és telepít a PowerShell-galériából, amely előzőleg nem volt telepítve.

Az Azure PowerShell Service Management modulnak vannak az Azure PowerShell Resource Manager-modulokkal közös függőségei. Ha már telepítette az Azure PowerShell Resource Manager-modulokat, hozzá kell adnia az `-AllowClobber` paramétert a telepítési parancshoz. Ez lehetővé teszi a meglévő közös függőségek frissítését. A paraméter nélkül a modul telepítése sikertelen lesz.

```powershell
Install-Module Azure -AllowClobber
```

A modul telepítése után a modult az alábbi parancs futtatásával importálhatja:

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a>A parancsmagok használata

Az Azure Service Management-parancsmagok használatának megkezdéséhez jelentkezzen be az Azure-fiókjába. A fiókba való bejelentkezéshez futtassa a következő parancsot:

```powershell
Add-AzureAccount
```

Az Azure-ba való bejelentkezés után az Azure PowerShell létrehoz egy környezetet az adott munkamenethez. Ez a környezet tartalmazza az adott munkamenet összes parancsmagjához használt Azure PowerShell-környezetet, -fiókot, -bérlőt és -előfizetést. Most már készen áll az alábbi modulok használatára.

## <a name="azure-service-management-cmdlets"></a>Azure Service Management-parancsmagok

Az Azure PowerShell-modulok rendszeresen frissülnek. Ha a parancsmagokat tárgyaló online súgóban olyan parancsmagokról vagy paraméterekről olvas, amelyek az Ön moduljában nem szerepelnek, töltse le és telepítse a modul legújabb verzióját. A saját modulverziójának az azonosításához írja be a következőt: `(Get-InstalledModule Azure).Version`.

Az Azure-ban gyakran előforduló feladatok némelyikének automatizálását segítő mintaszkripteket lásd a [Microsoft Azure Script Centerben](https://www.windowsazure.com/documentation/scripts/).

Általános információk a Windows PowerShell telepítéséről, megismeréséről, használatáról és testreszabásáról: [Szkriptek használata a Windows PowerShell-lel](/powershell/scripting/learn/ps101/00-introduction).

### <a name="how-to-get-powershellget"></a>A PowerShellGet beszerzése

|Operációs rendszer verziója|Telepítési utasítások|
|---|---|
|Windows 10 vagy Windows Server 2016 rendszert használok|Az operációs rendszer részét képező Windows Management Framework (WMF) 5.0 beépített eleme|
|Frissíteni szeretnék a PowerShell 5-ös verziójára|[A WMF legújabb verziójának telepítése](https://www.microsoft.com/download/details.aspx?id=54616)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a>Az Azure PowerShell verziószámának ellenőrzése

Habár javasoljuk, hogy a lehető leghamarabb frissítsen a legújabb verzióra, az Azure PowerShell számos verziója támogatott. Az Azure PowerShell telepített verziójának megállapításához futtassa a következő parancsot a parancssorban: `Get-InstalledModule Azure`.

```powershell
Get-InstalledModule Azure -AllVersions | Select-Object Name,Version,Path
```
