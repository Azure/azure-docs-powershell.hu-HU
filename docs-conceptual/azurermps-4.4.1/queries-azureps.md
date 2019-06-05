---
title: Azure-erőforrások lekérdezése és az eredmények formázása | Microsoft Docs
description: Az erőforrások lekérdezése az Azure-ban, illetve az eredmények formázása.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: db161bb0ec1b25b1cb7445724cc5758599dbc674
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/11/2019
ms.locfileid: "65534663"
---
# <a name="querying-for-azure-resources"></a>Azure-erőforrások lekérdezése

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

A lekérdezés a PowerShellben a beépített parancsmagokkal hajtható végre. A PowerShellben a parancsmagok angol neve az **_állítmány-tárgy_** sémát követi. A **_Get_** (lekérés) állítmányt használó parancsmagok a lekérdező parancsmagok. A parancsmag tárgya az az Azure-erőforrástípus, amelyen a parancsmag állítmánya által jelzett művelet végre lesz hajtva.

## <a name="selecting-simple-properties"></a>Egyszerű tulajdonságok kiválasztása

Az Azure PowerShellben az egyes parancsmagok megadott alapértelmezett formátummal rendelkeznek. Az egyes erőforrástípusok leggyakoribb tulajdonságai automatikusan megjelennek táblázatos vagy listaformátumban. További információ a kimenetek formázásáról: [Lekérdezési eredmények formázása](formatting-output.md).

A `Get-AzureRmVM` parancsmaggal listázhatja a fiókban lévő virtuális gépeket.

```powershell-interactive
Get-AzureRmVM
```

Az alapértelmezett kimenet automatikusan táblázatos formában jelenik meg.

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

A `Select-Object` parancsmaggal kiválaszthatja az Ön számára érdekes konkrét tulajdonságokat.

```powershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a>Összetett beágyazott tulajdonságok kiválasztása

Ha a kiválasztani kívánt tulajdonság mélyen van beágyazva a JSON-kimenetbe, meg kell adnia a beágyazott tulajdonság teljes elérési útját. A következő példa a virtuális gép nevének és operációsrendszer-típusának kiválasztását mutatja be a `Get-AzureRmVM` parancsmagból.

```powershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a>Eredmények szűrése a Where-Object parancsmaggal

A `Where-Object` parancsmag használatával bármely tulajdonságérték alapján szűrheti az eredményeket. A következő példában a szűrő csak azokat a virtuális gépeket választja ki, amelyeknek a neve tartalmazza az „RGD” karakterláncot.

```powershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

A következő példában a rendszer eredményként azokat a virtuális gépeket adja vissza, amelyeknek a mérete (vmSize) „Standard_DS1_V2”.

```powershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
