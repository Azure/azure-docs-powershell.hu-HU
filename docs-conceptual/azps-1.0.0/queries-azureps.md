---
title: Azure PowerShell-parancsmagok lekérdezésének kimenete
description: Az erőforrások lekérdezése az Azure-ban, illetve az eredmények formázása.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: fd0135f981452a2425f4dc8b9c9708d4907eff2a
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594969"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a>Azure PowerShell-parancsmagok lekérdezésének kimenete

A lekérdezés a PowerShellben a beépített parancsmagokkal hajtható végre. A PowerShellben a parancsmagok angol neve az **_állítmány-tárgy_** sémát követi. A **_Get_** (lekérés) állítmányt használó parancsmagok a lekérdező parancsmagok. A parancsmag tárgya az az Azure-erőforrástípus, amelyen a parancsmag állítmánya által jelzett művelet végre lesz hajtva.

## <a name="select-simple-properties"></a>Egyszerű tulajdonságok kiválasztása

Az Azure PowerShellben az egyes parancsmagok megadott alapértelmezett formátummal rendelkeznek. Az egyes erőforrástípusok leggyakoribb tulajdonságai automatikusan megjelennek táblázatos vagy listaformátumban. További információ a kimenetek formázásáról: [Lekérdezési eredmények formázása](formatting-output.md).

A `Get-AzVM` parancsmaggal listázhatja a fiókban lévő virtuális gépeket.

```azurepowershell-interactive
Get-AzVM
```

Az alapértelmezett kimenet automatikusan táblázatos formában jelenik meg.

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

A `Select-Object` parancsmaggal kiválaszthatja az Ön számára érdekes konkrét tulajdonságokat.

```azurepowershell-interactive
Get-AzVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a>Összetett beágyazott tulajdonságok kiválasztása

Ha a kívánt tulajdonság be van ágyazva a JSON-kimenetbe, meg kell adnia a tulajdonság teljes elérési útját. A következő példa a virtuális gép nevének és operációsrendszer-típusának kiválasztását mutatja be a `Get-AzVM` parancsmagból.

```azurepowershell-interactive
Get-AzVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a>Az eredmények szűrése a Where-Object parancsmaggal

A `Where-Object` parancsmag használatával bármely tulajdonságérték alapján szűrheti az eredményeket. A következő példában a szűrő csak azokat a virtuális gépeket választja ki, amelyeknek a neve tartalmazza az „RGD” karakterláncot.

```azurepowershell-interactive
Get-AzVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

A következő példában a rendszer eredményként azokat a virtuális gépeket adja vissza, amelyeknek a mérete (vmSize) „Standard_DS1_V2”.

```azurepowershell-interactive
Get-AzVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```