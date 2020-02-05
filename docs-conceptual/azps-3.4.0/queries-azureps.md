---
title: Azure PowerShell-parancsmagok lekérdezésének kimenete
description: Az erőforrások lekérdezése az Azure-ban, illetve az eredmények formázása.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.openlocfilehash: 9141f5640467722608cb7748f425ce3942668fb8
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002775"
---
# <a name="query-output-of-azure-powershell"></a><span data-ttu-id="2c7a0-103">Az Azure PowerShell lekérdezésének kimenete</span><span class="sxs-lookup"><span data-stu-id="2c7a0-103">Query output of Azure PowerShell</span></span> 

<span data-ttu-id="2c7a0-104">Az egyes Azure PowerShell-parancsmagok eredménye egy-egy Azure PowerShell-objektum.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-104">The results of each Azure PowerShell cmdlet are an Azure PowerShell object.</span></span> <span data-ttu-id="2c7a0-105">Még azok a parancsmagok is, amelyek nem kifejezetten `Get-` műveletek, visszaadhatnak egy megvizsgálható értéket, amely egy létrehozott vagy módosított erőforrásról nyújt információt.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-105">Even cmdlets that aren't explicitly `Get-` operations might return a value that can be inspected, to give information about a resource that was created or modified.</span></span> <span data-ttu-id="2c7a0-106">Bár a legtöbb parancsmag egyetlen objektumot ad vissza, némelyikük egy tömböt, amelyen végig kell haladni.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-106">While most cmdlets return a single object, some return an array that should be iterated through.</span></span>

<span data-ttu-id="2c7a0-107">Az Azure PowerShellből szinte minden esetben a [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) parancsmaggal kérdezheti le a kimenetet, amelynek rövidítése gyakran `select`.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-107">In almost all cases, you query output from Azure PowerShell with the [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet, often abbreviated to `select`.</span></span> <span data-ttu-id="2c7a0-108">A kimenetek a [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) parancsmaggal, illetve annak `where` aliasával szűrhetők.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-108">Output can be filtered with [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), or its alias `where`.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="2c7a0-109">Egyszerű tulajdonságok kiválasztása</span><span class="sxs-lookup"><span data-stu-id="2c7a0-109">Select simple properties</span></span>

<span data-ttu-id="2c7a0-110">Az alapértelmezett táblázatos formátumban az Azure PowerShell-parancsmagok nem jelenítik meg az összes elérhető tulajdonságukat.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-110">In the default table format, Azure PowerShell cmdlets don't display all of their available properties.</span></span> <span data-ttu-id="2c7a0-111">Minden tulajdonság a [Format-List](/powershell/module/microsoft.powershell.utility/format-list) parancsmaggal vagy a kimenet a `Select-Object *` parancshoz való átirányításával érhető el:</span><span class="sxs-lookup"><span data-stu-id="2c7a0-111">You can get the full properties by using the [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet, or by piping output to `Select-Object *`:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

<span data-ttu-id="2c7a0-112">Ha már tudja azoknak a tulajdonságoknak a nevét, amelyekre kíváncsi, ezeket a tulajdonságneveket közvetlenül lekérheti a `Select-Object` használatával:</span><span class="sxs-lookup"><span data-stu-id="2c7a0-112">Once you know the names of the properties that you're interested in, you can use those property names with `Select-Object` to get them directly:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

<span data-ttu-id="2c7a0-113">A `Select-Object` kimenete mindig úgy van formázva, hogy a kért adatokat jelenítse meg.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-113">Output from using `Select-Object` is always formatted to display the requested information.</span></span> <span data-ttu-id="2c7a0-114">Ha többet szeretne megtudni arról, hogyan használható a formázás a parancsmagok által visszaadott eredmények lekérdezésének részeként, tekintse meg az [Azure PowerShell-parancsmag kimenetének formázása](formatting-output.md) című részt.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-114">To learn about using formatting as part of querying cmdlet results, see [Format Azure PowerShell cmdlet output](formatting-output.md).</span></span>

## <a name="select-nested-properties"></a><span data-ttu-id="2c7a0-115">Beágyazott tulajdonságok kiválasztása</span><span class="sxs-lookup"><span data-stu-id="2c7a0-115">Select nested properties</span></span>

<span data-ttu-id="2c7a0-116">Az Azure PowerShell-parancsmagok kimenetének néhány tulajdonsága beágyazott objektumokat használ. Ilyen például a `Get-AzVM` kimenet `StorageProfile` tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-116">Some properties in Azure PowerShell cmdlet output use nested objects, like the `StorageProfile` property of `Get-AzVM` output.</span></span> <span data-ttu-id="2c7a0-117">A beágyazott tulajdonság értékének lekéréséhez adja meg a megjelenítendő nevet és a megvizsgálni kívánt érték teljes elérési útvonalát a `Select-Object` parancshoz tartozó szótárargumentum részeként:</span><span class="sxs-lookup"><span data-stu-id="2c7a0-117">To get a value from a nested property, provide a display name and the full path to the value you want to inspect as part of a dictionary argument to `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

<span data-ttu-id="2c7a0-118">Minden szótárargumentum az objektum egy tulajdonságát választja ki.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-118">Each dictionary argument selects one property from the object.</span></span> <span data-ttu-id="2c7a0-119">A kinyerni kívánt tulajdonságnak egy kifejezés részének kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-119">The property to extract must be part of an expression.</span></span>

## <a name="filter-results"></a><span data-ttu-id="2c7a0-120">Szűrés eredményei</span><span class="sxs-lookup"><span data-stu-id="2c7a0-120">Filter results</span></span> 

<span data-ttu-id="2c7a0-121">A `Where-Object` parancsmag használatával bármely tulajdonságérték alapján szűrheti az eredményeket, a beágyazott tulajdonságokat is beleértve.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-121">The `Where-Object` cmdlet allows you to filter the result based on any property value, including nested properties.</span></span> <span data-ttu-id="2c7a0-122">A következő példa bemutatja, hogyan használható a `Where-Object` egy Linux rendszerű virtuális gép megkeresésére egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-122">The next example shows how to use `Where-Object` to find the Linux VMs in a resource group.</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

<span data-ttu-id="2c7a0-123">A `Select-Object` és a `Where-Object` eredményeit továbbíthatja az egyiktől a másiknak.</span><span class="sxs-lookup"><span data-stu-id="2c7a0-123">You can pipe the results of `Select-Object` and `Where-Object` to each other.</span></span> <span data-ttu-id="2c7a0-124">A teljesítményt szem előtt tartva ajánlott a `Where-Object` műveletet a `Select-Object` elé helyezni:</span><span class="sxs-lookup"><span data-stu-id="2c7a0-124">For performance purposes, it's always recommended to put the `Where-Object` operation before `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```