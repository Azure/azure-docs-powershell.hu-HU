---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azscomputequota
schema: 2.0.0
ms.openlocfilehash: efbd141d5ba41afa51c57f05df96840a81ab4fa1
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015371"
---
# <span data-ttu-id="aef8e-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="aef8e-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="aef8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aef8e-102">SYNOPSIS</span></span>
<span data-ttu-id="aef8e-103">Számítási kvótát hoz létre vagy frissít a megadott kvóta-paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="aef8e-103">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="aef8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aef8e-104">SYNTAX</span></span>

### <span data-ttu-id="aef8e-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aef8e-105">CreateExpanded (Default)</span></span>
```
New-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="aef8e-106">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="aef8e-106">Create</span></span>
```
New-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aef8e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aef8e-107">DESCRIPTION</span></span>
<span data-ttu-id="aef8e-108">Számítási kvótát hoz létre vagy frissít a megadott kvóta-paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="aef8e-108">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="aef8e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aef8e-109">EXAMPLES</span></span>

### <span data-ttu-id="aef8e-110">Példa 1: számítási kvóta létrehozása alapértelmezett paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="aef8e-110">Example 1: Create a Compute Quota with Default Parameters</span></span>
```powershell
PS C:\> New-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="aef8e-111">A nem meghatározott paraméterek a fenti alapértelmezett paraméternek megfelelőek lesznek.</span><span class="sxs-lookup"><span data-stu-id="aef8e-111">Any parameters that are not specified will be set to their default parameter, shown above.</span></span>

### <span data-ttu-id="aef8e-112">2. példa: számítási kvóta létrehozása egyéni paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="aef8e-112">Example 2: Create a Compute Quota with Custom Parameters</span></span>
```powershell
PS C:\>  New-AzsComputeQuota -Name ExampleComputeQuotaWithCustomParameters -Location local -AvailabilitySetCount 9 -CoresCount 99 -PremiumManagedDiskAndSnapshotSize 1024 -StandardManagedDiskAndSnapshotSize 1024 -VirtualMachineCount 99 -VMScaleSetCount 2

AvailabilitySetCount               : 9
CoresLimit                         : 99
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locat
                                     ions/local/quotas/ExampleComputeQuotaWithCustomParameters
Location                           : local
Name                               : ExampleComputeQuotaWithCustomParameters
PremiumManagedDiskAndSnapshotSize  : 1024
StandardManagedDiskAndSnapshotSize : 1024
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 2
VirtualMachineCount                : 99
```

<span data-ttu-id="aef8e-113">A kvótákat a paraméterekkel testre szabhatja.</span><span class="sxs-lookup"><span data-stu-id="aef8e-113">Customize Quota with parameters.</span></span> <span data-ttu-id="aef8e-114">A nem meghatározott paraméterek alapértelmezett értékkel rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="aef8e-114">Any parameters not specified will have default value.</span></span>

## <span data-ttu-id="aef8e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aef8e-115">PARAMETERS</span></span>

### <span data-ttu-id="aef8e-116">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="aef8e-116">-AvailabilitySetCount</span></span>
<span data-ttu-id="aef8e-117">A rendelkezésre álló elérhetőségi készletek maximális száma</span><span class="sxs-lookup"><span data-stu-id="aef8e-117">Maximum number of availability sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-118">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="aef8e-118">-CoresCount</span></span>
<span data-ttu-id="aef8e-119">Az engedélyezett magok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="aef8e-119">Maximum number of cores allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases: CoresLimit

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef8e-120">-DefaultProfile</span></span>
<span data-ttu-id="aef8e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aef8e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="aef8e-122">-Location</span></span>
<span data-ttu-id="aef8e-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="aef8e-123">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-124">-Location1</span><span class="sxs-lookup"><span data-stu-id="aef8e-124">-Location1</span></span>
<span data-ttu-id="aef8e-125">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="aef8e-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aef8e-126">-Name</span></span>
<span data-ttu-id="aef8e-127">A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="aef8e-127">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-128">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="aef8e-128">-NewQuota</span></span>
<span data-ttu-id="aef8e-129">Megtartja az erőforrás-hozzárendelés szabályozásához használt kvóta-információkat.</span><span class="sxs-lookup"><span data-stu-id="aef8e-129">Holds Compute quota information used to control resource allocation.</span></span>
<span data-ttu-id="aef8e-130">A kivitelezéshez tekintse meg a NEWQUOTA tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="aef8e-130">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-131">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="aef8e-131">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="aef8e-132">A felügyelt lemezek és a prémium típusú Pillanatképek maximális száma</span><span class="sxs-lookup"><span data-stu-id="aef8e-132">Maximum number of managed disks and snapshots of type premium allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-133">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="aef8e-133">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="aef8e-134">A felügyelt lemezek és a standard típusú Pillanatképek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="aef8e-134">Maximum number of managed disks and snapshots of type standard allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aef8e-135">-SubscriptionId</span></span>
<span data-ttu-id="aef8e-136">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="aef8e-136">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aef8e-137">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="aef8e-137">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-138">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="aef8e-138">-VirtualMachineCount</span></span>
<span data-ttu-id="aef8e-139">Engedélyezett virtuális gépek maximális száma</span><span class="sxs-lookup"><span data-stu-id="aef8e-139">Maximum number of virtual machines allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-140">-VMScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="aef8e-140">-VMScaleSetCount</span></span>
<span data-ttu-id="aef8e-141">A méretarány maximális száma engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="aef8e-141">Maximum number of scale sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aef8e-142">-Confirm</span></span>
<span data-ttu-id="aef8e-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aef8e-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aef8e-144">-WhatIf</span></span>
<span data-ttu-id="aef8e-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aef8e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aef8e-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aef8e-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aef8e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef8e-147">CommonParameters</span></span>
<span data-ttu-id="aef8e-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aef8e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef8e-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aef8e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef8e-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aef8e-150">INPUTS</span></span>

### <span data-ttu-id="aef8e-151">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="aef8e-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="aef8e-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aef8e-152">OUTPUTS</span></span>

### <span data-ttu-id="aef8e-153">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="aef8e-153">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="aef8e-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aef8e-154">NOTES</span></span>

<span data-ttu-id="aef8e-155">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="aef8e-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aef8e-156">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="aef8e-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="aef8e-157">NEWQUOTA <IQuota> : az erőforrás-hozzárendelés szabályozásához használt kvóta-információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="aef8e-157">NEWQUOTA <IQuota>: Holds Compute quota information used to control resource allocation.</span></span>
  - <span data-ttu-id="aef8e-158">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="aef8e-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="aef8e-159">`[AvailabilitySetCount <Int32?>]`: A rendelkezésre álló elérhetőségek száma maximálisan engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="aef8e-159">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="aef8e-160">`[CoresLimit <Int32?>]`: Engedélyezett magok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="aef8e-160">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="aef8e-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: A felügyelt lemezek és a prémium típusú Pillanatképek maximális száma</span><span class="sxs-lookup"><span data-stu-id="aef8e-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="aef8e-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: A felügyelt lemezek és a standard típusú Pillanatképek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="aef8e-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="aef8e-163">`[VMScaleSetCount <Int32?>]`: A méretarány-készletek maximális száma engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="aef8e-163">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="aef8e-164">`[VirtualMachineCount <Int32?>]`: Engedélyezett virtuális gépek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="aef8e-164">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="aef8e-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aef8e-165">RELATED LINKS</span></span>

