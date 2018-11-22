---
title: Azure PowerShell-parancsmag kimenetének formázása
description: Az Azure PowerShell-parancsmagok kimenetének formázása.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 390285bcf483e75b7a2b77d345ccb108669f66e5
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259791"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="3c58c-103">Azure PowerShell-parancsmag kimenetének formázása</span><span class="sxs-lookup"><span data-stu-id="3c58c-103">Format AzurePowerShell cmdlet output</span></span>

<span data-ttu-id="3c58c-104">Alapértelmezés szerint minden Azure PowerShell-parancsmag kimenete előre meghatározott formátummal rendelkezik, hogy könnyen olvasható legyen.</span><span class="sxs-lookup"><span data-stu-id="3c58c-104">By default each Azure PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="3c58c-105">A PowerShell lehetővé teszi a parancsmag kimenetének rugalmas állítását, vagy más formátumba való átalakítását a következő parancsmagokkal:</span><span class="sxs-lookup"><span data-stu-id="3c58c-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="3c58c-106">Formátum</span><span class="sxs-lookup"><span data-stu-id="3c58c-106">Formatting</span></span>      | <span data-ttu-id="3c58c-107">Átalakítás</span><span class="sxs-lookup"><span data-stu-id="3c58c-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="3c58c-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="3c58c-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="3c58c-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="3c58c-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="3c58c-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="3c58c-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="3c58c-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="3c58c-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="3c58c-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="3c58c-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="3c58c-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="3c58c-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="3c58c-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="3c58c-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="3c58c-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="3c58c-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a><span data-ttu-id="3c58c-116">Példák formázásra</span><span class="sxs-lookup"><span data-stu-id="3c58c-116">Format examples</span></span>

<span data-ttu-id="3c58c-117">Ebben a példában lekérjük az Azure-beli virtuális gépek listáját az alapértelmezett előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="3c58c-117">In this example, we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="3c58c-118">A `Get-AzureRmVM` parancs kimenete alapértelmezés szerint táblázatos formában jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="3c58c-118">The `Get-AzureRmVM` command defaults output into a table format.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="3c58c-119">A táblázat visszaadott oszlopainak korlátozásához használja a `Format-Table` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3c58c-119">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="3c58c-120">A következő példában a virtuális gépek ugyanezen listáját kérjük le, de a kimenetet a virtuális gépek nevére, az erőforráscsoportra és a virtuális gép helyére korlátozzuk.</span><span class="sxs-lookup"><span data-stu-id="3c58c-120">In the following example, we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="3c58c-121">Az `-Autosize` paraméterrel az oszlopok mérete az adatok méretéhez igazítható.</span><span class="sxs-lookup"><span data-stu-id="3c58c-121">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="3c58c-122">A kimenet formázható listaként is.</span><span class="sxs-lookup"><span data-stu-id="3c58c-122">Output can also be formatted into a list.</span></span> <span data-ttu-id="3c58c-123">Az alábbi példa ezt mutatja be a `Format-List` parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="3c58c-123">The following example shows this using the`Format-List` cmdlet.</span></span>

```azurepowershell-interactive
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

## <a name="convert-to-other-data-types"></a><span data-ttu-id="3c58c-124">Konvertálás egyéb adattípusokká</span><span class="sxs-lookup"><span data-stu-id="3c58c-124">Convert to other data types</span></span>

<span data-ttu-id="3c58c-125">A PowerShell lehetővé teszi a parancskimenetek különféle adatformátumokba konvertálását is.</span><span class="sxs-lookup"><span data-stu-id="3c58c-125">PowerShell also allows taking command output and converting it into multiple data formats.</span></span> <span data-ttu-id="3c58c-126">A következő példában a `Select-Object` parancsmaggal lekérjük az előfizetésben lévő virtuális gépek attribútumait, majd átalakítjuk a kimenetet CSV formátumba, hogy könnyen importálható legyen adatbázisokba vagy táblázatokba.</span><span class="sxs-lookup"><span data-stu-id="3c58c-126">In the following example, the `Select-Object` cmdlet is used to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="3c58c-127">A kimenet konvertálható JSON formátumúra is.</span><span class="sxs-lookup"><span data-stu-id="3c58c-127">Output can also be converted into the JSON format.</span></span>  <span data-ttu-id="3c58c-128">A következő példában ugyanezt a listát hozzuk létre a virtuális gépekről, azonban a kimenetet JSON formátumba alakítjuk.</span><span class="sxs-lookup"><span data-stu-id="3c58c-128">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```azurepowershell-interactive
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
