---
title: Az Azure PowerShell telepítése macOS vagy Linux rendszeren
description: Az Azure PowerShell telepítése macOS vagy Linux rendszeren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323169"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Az Azure PowerShell telepítése macOS vagy Linux rendszeren

Nem Windows rendszerű platformokon az Azure PowerShell futtatható a PowerShell Core 6-os verzióján. A Windowshoz készült .NET-keretrendszerre épülő standard Azure PowerShelltől eltérően ez a termék a .NET Core-ra épül, és bármely, a .Net Core futtatókörnyezetet támogató platformon futtatható.

> [!NOTE]
> Jelenleg a PowerShell Core 6-os verziója és a .NET Core-hoz készült Azure PowerShell csak bétaverzióban érhető el.
> A termékek korlátozott támogatással rendelkeznek. Ha problémákba ütközik vagy hibát észlel, jelentse be a problémát a GitHubon.
>
> * [A PowerShell Core 6-os verziójának problémái](https://github.com/PowerShell/PowerShell/issues)
> * [Az Azure PowerShell problémái](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a>A PowerShell Core 6-os verziójának telepítése

A PowerShell Core 6-os verziójának telepítése Linux vagy macOS rendszeren a Linux-disztribúciótól és az operációs rendszer verziójától függően változik.
Részletes útmutatásokat a következő cikkekben talál:

- [A PowerShell Core telepítése macOS rendszeren](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [A PowerShell Core telepítése Linux rendszeren](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>A .NET Core-hoz készült Azure PowerShell telepítése

A PowerShell Core 6-os verziója tartalmazza az előre telepített PowerShellGet modult. Ez megkönnyíti a PowerShell-galériában közzétett modulok telepítését. Az Azure PowerShell telepítéséhez nyisson meg egy új PowerShell-munkamenetet, majd futtassa az alábbi parancsot:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a>Az AzureRM.Netcore-modul betöltése

A modul telepítése után be kell tölteni a azt a PowerShell-munkamenetbe. A modulok az `Import-Module` parancsmaggal, az alábbi módon tölthetők be:

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

Amikor az importálás befejeződött, tesztelheti az újonnan telepített modult. Ehhez próbáljon meg bejelentkezni az Azure-ba az alábbi paranccsal:

```powershell
Connect-AzureRmAccount
```

A fenti parancsnak fel kell kérnie, hogy lépjen a `https://aka.ms/devicelogin` oldalra, és adja meg a megadott kódot.

## <a name="available-cmdlets"></a>Elérhető parancsmagok

A .NET Standardhoz elérhető Azure PowerShell-modulok még fejlesztés alatt állnak. Ezek a modulok nem tartalmazzák a modulok Windows verziójához elérhető teljes parancsmagkészletét. Az AzureRM.Netcore-modulokban az alábbi funkciók érhetők el:

* Fiókkezelés
  - Bejelentkezés Microsoft-fiókkal, szervezeti fiókkal vagy egyszerű szolgáltatásnévvel a Microsoft Azure Active Directoryn keresztül
  - Hitelesítő adatokat mentése lemezre a Save-AzureRmContext parancsmaggal és a mentett hitelesítő adatok betöltése az Import-AzureRmContext parancsmaggal
* Környezet
  - Különböző nem beépített Microsoft Azure-környezetek beszerzése
  - Testre szabott környezetek (például az Azure Stack- vagy a Windows Azure Pack-környezetek) hozzáadása/beállítása/eltávolítása
* Felügyeletisík-parancsmagok az Azure-szolgáltatásokhoz a Resource Manager és a Service Manager felületeinek használatával.
  - Virtuális gép
  - App Service (webhelyek)
  - SQL Database
  - Storage
  - Network (Hálózat)

## <a name="next-steps"></a>További lépések

Az Azure PowerShell használatával kapcsolatos további információkért tekintse meg az [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md) című cikket.
