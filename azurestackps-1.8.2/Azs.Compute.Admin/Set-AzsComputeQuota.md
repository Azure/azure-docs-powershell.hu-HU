---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8da912ed9751231a44c34b27df36abc62d55c4ab
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016784"
---
# <span data-ttu-id="f637c-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="f637c-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="f637c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f637c-102">SYNOPSIS</span></span>
<span data-ttu-id="f637c-103">Meglévő számítási kvóta frissítése a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="f637c-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="f637c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f637c-104">SYNTAX</span></span>

### <span data-ttu-id="f637c-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f637c-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f637c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f637c-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f637c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f637c-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f637c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f637c-108">DESCRIPTION</span></span>
<span data-ttu-id="f637c-109">Meglévő számítási kvóta frissítése</span><span class="sxs-lookup"><span data-stu-id="f637c-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="f637c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f637c-110">EXAMPLES</span></span>

### <span data-ttu-id="f637c-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f637c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="f637c-112">A számítási kvóta frissítése</span><span class="sxs-lookup"><span data-stu-id="f637c-112">Update a compute quota.</span></span>

## <span data-ttu-id="f637c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f637c-113">PARAMETERS</span></span>

### <span data-ttu-id="f637c-114">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="f637c-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="f637c-115">Az elérhetőségi halmazok száma engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="f637c-115">Number of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f637c-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="f637c-116">-CoresCount</span></span>
<span data-ttu-id="f637c-117">A megengedett magok száma.</span><span class="sxs-lookup"><span data-stu-id="f637c-117">Number of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f637c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f637c-118">-InputObject</span></span>
<span data-ttu-id="f637c-119">Esetleg módosított számítási kvóta: az űrlap Get-AzsComputeQuota.</span><span class="sxs-lookup"><span data-stu-id="f637c-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

```yaml
Type: ComputeQuotaObject
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f637c-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="f637c-120">-Location</span></span>
<span data-ttu-id="f637c-121">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="f637c-121">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f637c-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f637c-122">-Name</span></span>
<span data-ttu-id="f637c-123">A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="f637c-123">The name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f637c-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="f637c-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="f637c-125">A normál kezelt lemezek és a pillanatképek megengedett mérete.</span><span class="sxs-lookup"><span data-stu-id="f637c-125">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f637c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f637c-126">-ResourceId</span></span>
<span data-ttu-id="f637c-127">A kar kiszámítja a kvóta azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="f637c-127">The ARM compute quota id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f637c-128">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="f637c-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="f637c-129">A normál kezelt lemezek és a pillanatképek megengedett mérete.</span><span class="sxs-lookup"><span data-stu-id="f637c-129">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f637c-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="f637c-130">-VirtualMachineCount</span></span>
<span data-ttu-id="f637c-131">Az engedélyezett virtuális gépek száma.</span><span class="sxs-lookup"><span data-stu-id="f637c-131">Number of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f637c-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="f637c-132">-VmScaleSetCount</span></span>
<span data-ttu-id="f637c-133">A megengedett méretarányok száma</span><span class="sxs-lookup"><span data-stu-id="f637c-133">Number of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f637c-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f637c-134">-Confirm</span></span>
<span data-ttu-id="f637c-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f637c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f637c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f637c-136">-WhatIf</span></span>
<span data-ttu-id="f637c-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f637c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f637c-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f637c-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f637c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f637c-139">CommonParameters</span></span>
<span data-ttu-id="f637c-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f637c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f637c-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f637c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f637c-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f637c-142">INPUTS</span></span>

## <span data-ttu-id="f637c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f637c-143">OUTPUTS</span></span>

### <span data-ttu-id="f637c-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="f637c-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="f637c-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f637c-145">NOTES</span></span>

## <span data-ttu-id="f637c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f637c-146">RELATED LINKS</span></span>

