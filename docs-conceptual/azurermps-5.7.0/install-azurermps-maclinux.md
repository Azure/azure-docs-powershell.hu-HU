---
title: Az Azure PowerShell telepítése és konfigurálása macOS és Linux rendszeren | Microsoft Docs
description: Az Azure PowerShell telepítése és konfigurálása az első használathoz macOS és Linux rendszeren.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 7228ca9791f174cb3554dd359b3723e98589ee17
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/23/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a>Az Azure PowerShell telepítése és konfigurálása macOS és Linux rendszeren

A PowerShell Core 6-os verziója és az Azure PowerShell most már nem Windows rendszerű platformokra is telepíthető.
Az Azure PowerShell macOS és Linux rendszeren való telepítése nem sokban tér el a Windows rendszeren való telepítéstől, először azonban telepítenie kell a PowerShell Core 6-os verzióját is.

> [!NOTE]

> Jelenleg a PowerShell Core 6-os verziója és a .NET Core-hoz készült Azure PowerShell csak bétaverzióban érhető el.
> A termékek korlátozott támogatással rendelkeznek. Ha problémákba ütközik vagy hibákat észlel, kérjük, a GitHubon keresztül jelentse.
>
> * [A PowerShell Core 6-os verziójának problémái](https://github.com/PowerShell/PowerShell/issues)
> * [Az Azure PowerShell problémái](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a>1. lépés: A PowerShell Core 6-os verziójának telepítése

A PowerShell Core 6-os verziójának telepítési folyamata attól függően változik, hogy milyen operációs rendszerre telepíti.
Bár a PowerShell Core 6-os verziója a Windows rendszeren is telepíthető, ez a cikk a macOS és a Linux rendszerre összpontosít. Ha Windows rendszeren szeretné használni az Azure PowerShellt, tekintse meg a Windowsra vonatkozó [telepítési](./install-azurerm-ps.md) cikket.

A **PowerShell Core 6-os verziójának** telepítése Linux vagy macOS rendszeren a Linux-disztribúciótól és az operációs rendszer verziójától függően változik.
Részletes útmutatásokat a következő cikkben talál:

- [A PowerShell Core telepítése macOS és Linux rendszeren](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a>2. lépés: A .NET Core-hoz készült Azure PowerShell telepítése

A PowerShell Core 6-os verziója tartalmazza az előre telepített PowerShellGet modult. Ez megkönnyíti a PowerShell-galériában közzétett modulok telepítését. Az Azure PowerShell telepítéséhez nyisson meg egy új PowerShell-munkamenetet, majd futtassa az alábbi parancsot:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a>3. lépés: Az AzureRM.Netcore modul betöltése

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
