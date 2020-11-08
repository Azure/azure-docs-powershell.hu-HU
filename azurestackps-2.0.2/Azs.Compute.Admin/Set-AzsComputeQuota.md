---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/set-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 3229a6383d7159b31bf542add7374326d0de4ac4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016716"
---
# <span data-ttu-id="48e53-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="48e53-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="48e53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48e53-102">SYNOPSIS</span></span>


## <span data-ttu-id="48e53-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48e53-103">SYNTAX</span></span>

### <span data-ttu-id="48e53-104">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48e53-104">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="48e53-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48e53-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -NewQuota <IQuota> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="48e53-106">UpdateExpanded</span><span class="sxs-lookup"><span data-stu-id="48e53-106">UpdateExpanded</span></span>
```
Set-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```
## <span data-ttu-id="48e53-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="48e53-107">DESCRIPTION</span></span>
<span data-ttu-id="48e53-108">Számítási kvóta frissítése</span><span class="sxs-lookup"><span data-stu-id="48e53-108">Update a Compute Quota</span></span>

## <span data-ttu-id="48e53-109">Példák</span><span class="sxs-lookup"><span data-stu-id="48e53-109">EXAMPLES</span></span>

### <span data-ttu-id="48e53-110">Példa 1: meglévő számítási kvóta tulajdonságainak beállítása</span><span class="sxs-lookup"><span data-stu-id="48e53-110">Example 1: Set Properties on an Existing Compute Quota</span></span>
```powershell
PS C:\> $myComputeQuota = Get-AzsComputeQuota -Name MyComputeQuota

PS C:\> $myComputeQuota.CoresLimit = 99; 

PS C:\> Set-AzsComputeQuota -NewQuota $myComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 99
Id                                 : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/northwest/quotas/MyComputeQuota
Location                           : northwest
Name                               : MyComputeQuota
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="48e53-111">Adja meg a parancssorban megadott paramétereket.</span><span class="sxs-lookup"><span data-stu-id="48e53-111">Set the parameters specified on the command line.</span></span>
<span data-ttu-id="48e53-112">A nem beállított paraméterek értéke alapértelmezés szerint 0 lesz</span><span class="sxs-lookup"><span data-stu-id="48e53-112">Any parameters not set will default to 0</span></span>

## <span data-ttu-id="48e53-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48e53-113">PARAMETERS</span></span>

### <span data-ttu-id="48e53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48e53-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="48e53-115">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="48e53-115">-NewQuota</span></span>
<span data-ttu-id="48e53-116">A kivitelezéshez tekintse meg a NEWQUOTA tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="48e53-116">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="48e53-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48e53-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="48e53-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48e53-118">-Confirm</span></span>
<span data-ttu-id="48e53-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48e53-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48e53-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48e53-120">-WhatIf</span></span>
<span data-ttu-id="48e53-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48e53-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48e53-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48e53-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48e53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e53-123">CommonParameters</span></span>
<span data-ttu-id="48e53-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48e53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e53-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="48e53-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e53-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48e53-126">INPUTS</span></span>

### <span data-ttu-id="48e53-127">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="48e53-127">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="48e53-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48e53-128">OUTPUTS</span></span>

### <span data-ttu-id="48e53-129">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="48e53-129">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="48e53-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48e53-130">NOTES</span></span>

<span data-ttu-id="48e53-131">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="48e53-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48e53-132">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="48e53-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="48e53-133">NEWQUOTA <IQuota> :</span><span class="sxs-lookup"><span data-stu-id="48e53-133">NEWQUOTA <IQuota>:</span></span> 
  - <span data-ttu-id="48e53-134">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="48e53-134">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="48e53-135">`[AvailabilitySetCount <Int32?>]`: A rendelkezésre álló elérhetőségek száma maximálisan engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="48e53-135">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="48e53-136">`[CoresLimit <Int32?>]`: Engedélyezett magok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="48e53-136">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="48e53-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: A felügyelt lemezek és a prémium típusú Pillanatképek maximális száma</span><span class="sxs-lookup"><span data-stu-id="48e53-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="48e53-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: A felügyelt lemezek és a standard típusú Pillanatképek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="48e53-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="48e53-139">`[VMScaleSetCount <Int32?>]`: A méretarány-készletek maximális száma engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="48e53-139">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="48e53-140">`[VirtualMachineCount <Int32?>]`: Engedélyezett virtuális gépek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="48e53-140">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="48e53-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48e53-141">RELATED LINKS</span></span>

