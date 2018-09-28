---
title: Azure PowerShell-parancsmagok lekérdezésének kimenete
description: Az erőforrások lekérdezése az Azure-ban, illetve az eredmények formázása.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: da8c8f37d8c60e9555b4627a7b5c3d1d6e7888fa
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/27/2018
ms.locfileid: "47179173"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a><span data-ttu-id="2743f-103">Azure PowerShell-parancsmagok lekérdezésének kimenete</span><span class="sxs-lookup"><span data-stu-id="2743f-103">Query output of Azure PowerShell cmdlets</span></span>

<span data-ttu-id="2743f-104">A lekérdezés a PowerShellben a beépített parancsmagokkal hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="2743f-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="2743f-105">A PowerShellben a parancsmagok angol neve az **_állítmány-tárgy_** sémát követi.</span><span class="sxs-lookup"><span data-stu-id="2743f-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="2743f-106">A **_Get_** (lekérés) állítmányt használó parancsmagok a lekérdező parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="2743f-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="2743f-107">A parancsmag tárgya az az Azure-erőforrástípus, amelyen a parancsmag állítmánya által jelzett művelet végre lesz hajtva.</span><span class="sxs-lookup"><span data-stu-id="2743f-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="2743f-108">Egyszerű tulajdonságok kiválasztása</span><span class="sxs-lookup"><span data-stu-id="2743f-108">Select simple properties</span></span>

<span data-ttu-id="2743f-109">Az Azure PowerShellben az egyes parancsmagok megadott alapértelmezett formátummal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="2743f-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="2743f-110">Az egyes erőforrástípusok leggyakoribb tulajdonságai automatikusan megjelennek táblázatos vagy listaformátumban.</span><span class="sxs-lookup"><span data-stu-id="2743f-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="2743f-111">További információ a kimenetek formázásáról: [Lekérdezési eredmények formázása](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="2743f-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="2743f-112">A `Get-AzureRmVM` parancsmaggal listázhatja a fiókban lévő virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="2743f-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="2743f-113">Az alapértelmezett kimenet automatikusan táblázatos formában jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="2743f-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="2743f-114">A `Select-Object` parancsmaggal kiválaszthatja az Ön számára érdekes konkrét tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2743f-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a><span data-ttu-id="2743f-115">Összetett beágyazott tulajdonságok kiválasztása</span><span class="sxs-lookup"><span data-stu-id="2743f-115">Select complex nested properties</span></span>

<span data-ttu-id="2743f-116">Ha a kívánt tulajdonság be van ágyazva a JSON-kimenetbe, meg kell adnia a tulajdonság teljes elérési útját.</span><span class="sxs-lookup"><span data-stu-id="2743f-116">If the property you want is nested in the JSON output, you need to supply the full path to the property.</span></span> <span data-ttu-id="2743f-117">A következő példa a virtuális gép nevének és operációsrendszer-típusának kiválasztását mutatja be a `Get-AzureRmVM` parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="2743f-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a><span data-ttu-id="2743f-118">Az eredmények szűrése a Where-Object parancsmaggal</span><span class="sxs-lookup"><span data-stu-id="2743f-118">Filter results with the Where-Object cmdlet</span></span>

<span data-ttu-id="2743f-119">A `Where-Object` parancsmag használatával bármely tulajdonságérték alapján szűrheti az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="2743f-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="2743f-120">A következő példában a szűrő csak azokat a virtuális gépeket választja ki, amelyeknek a neve tartalmazza az „RGD” karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="2743f-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="2743f-121">A következő példában a rendszer eredményként azokat a virtuális gépeket adja vissza, amelyeknek a mérete (vmSize) „Standard_DS1_V2”.</span><span class="sxs-lookup"><span data-stu-id="2743f-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```