---
title: Lekérdezési eredmények formázása | Microsoft Docs
description: Az erőforrások lekérdezése az Azure-ban, illetve az eredmények formázása.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 916cf8590de89762bade4f01ce5a502383d51796
ms.sourcegitcommit: 15bf69bf95eceb936b3a429e741add95c308826a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/28/2018
---
# <a name="formatting-query-results"></a><span data-ttu-id="323d5-103">Lekérdezési eredmények formázása</span><span class="sxs-lookup"><span data-stu-id="323d5-103">Formatting query results</span></span>

<span data-ttu-id="323d5-104">Alapértelmezés szerint minden PowerShell-parancsmag kimenete előre meghatározott formátummal rendelkezik, hogy könnyen olvasható legyen.</span><span class="sxs-lookup"><span data-stu-id="323d5-104">By default each PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="323d5-105">A PowerShell lehetővé teszi a parancsmag kimenetének rugalmas állítását, vagy más formátumba való átalakítását a következő parancsmagokkal:</span><span class="sxs-lookup"><span data-stu-id="323d5-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="323d5-106">Formátum</span><span class="sxs-lookup"><span data-stu-id="323d5-106">Formatting</span></span>      | <span data-ttu-id="323d5-107">Átalakítás</span><span class="sxs-lookup"><span data-stu-id="323d5-107">Conversion</span></span>       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a><span data-ttu-id="323d5-108">Példák a formázásra</span><span class="sxs-lookup"><span data-stu-id="323d5-108">Formatting examples</span></span>

<span data-ttu-id="323d5-109">Ebben a példában lekérjük az Azure-beli virtuális gépek listáját az alapértelmezett előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="323d5-109">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="323d5-110">A Get-AzureRmVM parancs kimenete alapértelmezés szerint táblázatos formában jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="323d5-110">The Get-AzureRmVM command defaults output into a table format.</span></span>

```powershell
Get-AzureRmVM
```

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="323d5-111">A táblázat visszaadott oszlopainak korlátozásához használja a `Format-Table` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="323d5-111">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="323d5-112">A következő példában a virtuális gépek ugyanezen listáját kérjük le, de a kimenetet a virtuális gépek nevére, az erőforráscsoportra és a virtuális gép helyére korlátozzuk.</span><span class="sxs-lookup"><span data-stu-id="323d5-112">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="323d5-113">Az `-Autosize` paraméterrel az oszlopok mérete az adatok méretéhez igazítható.</span><span class="sxs-lookup"><span data-stu-id="323d5-113">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```powershell
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="323d5-114">Az adatokat igény szerint lista formájában is megjelenítheti.</span><span class="sxs-lookup"><span data-stu-id="323d5-114">If you would prefer you can view information in a list format.</span></span> <span data-ttu-id="323d5-115">Az alábbi példa ezt mutatja be a `Format-List` parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="323d5-115">The following example shows this using the`Format-List` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="converting-to-other-data-types"></a><span data-ttu-id="323d5-116">Konvertálás egyéb adattípusokká</span><span class="sxs-lookup"><span data-stu-id="323d5-116">Converting to other data types</span></span>

<span data-ttu-id="323d5-117">A PowerShell többféle formátumot is biztosít, amelyekkel igényeire szabhatja a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="323d5-117">PowerShell also offers multiple output format you can use to meet your needs.</span></span>  <span data-ttu-id="323d5-118">A következő példában a `Select-Object` parancsmaggal lekérjük az előfizetésben lévő virtuális gépek attribútumait, majd átalakítjuk a kimenetet CSV formátumba, hogy könnyen importálható legyen adatbázisokba vagy táblázatokba.</span><span class="sxs-lookup"><span data-stu-id="323d5-118">In the following example we use the `Select-Object` cmdlet to get attributes of the virtual machines in our subscription and and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="323d5-119">A kimenet JSON formátumba is konvertálható.</span><span class="sxs-lookup"><span data-stu-id="323d5-119">You can also convert the output into JSON format.</span></span>  <span data-ttu-id="323d5-120">A következő példában ugyanezt a listát hozzuk létre a virtuális gépekről, azonban a kimenetet JSON formátumba alakítjuk.</span><span class="sxs-lookup"><span data-stu-id="323d5-120">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```
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
