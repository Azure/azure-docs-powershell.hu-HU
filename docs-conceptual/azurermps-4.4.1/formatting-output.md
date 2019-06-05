---
title: Lekérdezési eredmények formázása | Microsoft Docs
description: Az erőforrások lekérdezése az Azure-ban, illetve az eredmények formázása.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 0e94d30467c5a11bccfa71630f736bedf0d93112
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/11/2019
ms.locfileid: "65535052"
---
# <a name="formatting-query-results"></a>Lekérdezési eredmények formázása

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Alapértelmezés szerint minden PowerShell-parancsmag kimenete előre meghatározott formátummal rendelkezik, hogy könnyen olvasható legyen.  A PowerShell lehetővé teszi a parancsmag kimenetének rugalmas állítását, vagy más formátumba való átalakítását a következő parancsmagokkal:

| Formátum      | Átalakítás       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a>Példák a formázásra

Ebben a példában lekérjük az Azure-beli virtuális gépek listáját az alapértelmezett előfizetésben.  A Get-AzureRmVM parancs kimenete alapértelmezés szerint táblázatos formában jelenik meg.

```powershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

A táblázat visszaadott oszlopainak korlátozásához használja a `Format-Table` parancsmagot. A következő példában a virtuális gépek ugyanezen listáját kérjük le, de a kimenetet a virtuális gépek nevére, az erőforráscsoportra és a virtuális gép helyére korlátozzuk.  Az `-Autosize` paraméterrel az oszlopok mérete az adatok méretéhez igazítható.

```powershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

Az adatokat igény szerint lista formájában is megjelenítheti. Az alábbi példa ezt mutatja be a `Format-List` parancsmag használatával.

```powershell-interactive
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="converting-to-other-data-types"></a>Konvertálás egyéb adattípusokká

A PowerShell többféle formátumot is biztosít, amelyekkel igényeire szabhatja a kimenetet.  A következő példában a `Select-Object` parancsmaggal lekérjük az előfizetésben lévő virtuális gépek attribútumait, majd átalakítjuk a kimenetet CSV formátumba, hogy könnyen importálható legyen adatbázisokba vagy táblázatokba.

```powershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

A kimenet JSON formátumba is konvertálható.  A következő példában ugyanezt a listát hozzuk létre a virtuális gépekről, azonban a kimenetet JSON formátumba alakítjuk.

```powershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
