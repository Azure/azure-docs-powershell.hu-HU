---
title: Azure-erőforrások lekérdezése és az eredmények formázása | Microsoft Docs
description: Az erőforrások lekérdezése az Azure-ban, illetve az eredmények formázása.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 9a7627a25f9bbd196b1d615229e45a6e1ce7a7d9
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/07/2018
ms.locfileid: "51213001"
---
# <a name="querying-for-azure-resources"></a><span data-ttu-id="a5a7c-103">Azure-erőforrások lekérdezése</span><span class="sxs-lookup"><span data-stu-id="a5a7c-103">Querying for Azure resources</span></span>

<span data-ttu-id="a5a7c-104">A lekérdezés a PowerShellben a beépített parancsmagokkal hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="a5a7c-105">A PowerShellben a parancsmagok angol neve az **_állítmány-tárgy_** sémát követi.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="a5a7c-106">A **_Get_** (lekérés) állítmányt használó parancsmagok a lekérdező parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="a5a7c-107">A parancsmag tárgya az az Azure-erőforrástípus, amelyen a parancsmag állítmánya által jelzett művelet végre lesz hajtva.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="selecting-simple-properties"></a><span data-ttu-id="a5a7c-108">Egyszerű tulajdonságok kiválasztása</span><span class="sxs-lookup"><span data-stu-id="a5a7c-108">Selecting simple properties</span></span>

<span data-ttu-id="a5a7c-109">Az Azure PowerShellben az egyes parancsmagok megadott alapértelmezett formátummal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="a5a7c-110">Az egyes erőforrástípusok leggyakoribb tulajdonságai automatikusan megjelennek táblázatos vagy listaformátumban.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="a5a7c-111">További információ a kimenetek formázásáról: [Lekérdezési eredmények formázása](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="a5a7c-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="a5a7c-112">A `Get-AzureRmVM` parancsmaggal listázhatja a fiókban lévő virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```powershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="a5a7c-113">Az alapértelmezett kimenet automatikusan táblázatos formában jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="a5a7c-114">A `Select-Object` parancsmaggal kiválaszthatja az Ön számára érdekes konkrét tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```powershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="a5a7c-115">Összetett beágyazott tulajdonságok kiválasztása</span><span class="sxs-lookup"><span data-stu-id="a5a7c-115">Selecting complex nested properties</span></span>

<span data-ttu-id="a5a7c-116">Ha a kiválasztani kívánt tulajdonság mélyen van beágyazva a JSON-kimenetbe, meg kell adnia a beágyazott tulajdonság teljes elérési útját.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="a5a7c-117">A következő példa a virtuális gép nevének és operációsrendszer-típusának kiválasztását mutatja be a `Get-AzureRmVM` parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```powershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a><span data-ttu-id="a5a7c-118">Eredmények szűrése a Where-Object parancsmaggal</span><span class="sxs-lookup"><span data-stu-id="a5a7c-118">Filter result using the Where-Object cmdlet</span></span>

<span data-ttu-id="a5a7c-119">A `Where-Object` parancsmag használatával bármely tulajdonságérték alapján szűrheti az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="a5a7c-120">A következő példában a szűrő csak azokat a virtuális gépeket választja ki, amelyeknek a neve tartalmazza az „RGD” karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```powershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="a5a7c-121">A következő példában a rendszer eredményként azokat a virtuális gépeket adja vissza, amelyeknek a mérete (vmSize) „Standard_DS1_V2”.</span><span class="sxs-lookup"><span data-stu-id="a5a7c-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```powershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
