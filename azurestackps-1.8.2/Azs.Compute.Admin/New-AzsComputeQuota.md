---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffd2667f8c07c5b0594abe38f6cee5d40ce91a49
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016791"
---
# <span data-ttu-id="81e6c-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="81e6c-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="81e6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="81e6c-103">Új számítási kvóta létrehozása a számítási források korlátozásához.</span><span class="sxs-lookup"><span data-stu-id="81e6c-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="81e6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81e6c-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81e6c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="81e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="81e6c-106">Hozzon létre egy új számítási kvótát.</span><span class="sxs-lookup"><span data-stu-id="81e6c-106">Create a new compute quota.</span></span>

## <span data-ttu-id="81e6c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="81e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="81e6c-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="81e6c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="81e6c-109">Hozzon létre egy új számítási kvótát.</span><span class="sxs-lookup"><span data-stu-id="81e6c-109">Create a new compute quota.</span></span>

## <span data-ttu-id="81e6c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81e6c-110">PARAMETERS</span></span>

### <span data-ttu-id="81e6c-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="81e6c-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="81e6c-112">Az elérhetőségi halmazok száma engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="81e6c-112">Number  of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e6c-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="81e6c-113">-CoresCount</span></span>
<span data-ttu-id="81e6c-114">A megengedett magok száma.</span><span class="sxs-lookup"><span data-stu-id="81e6c-114">Number  of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: 3
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e6c-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="81e6c-115">-Location</span></span>
<span data-ttu-id="81e6c-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="81e6c-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e6c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81e6c-117">-Name</span></span>
<span data-ttu-id="81e6c-118">A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="81e6c-118">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e6c-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="81e6c-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="81e6c-120">A normál kezelt lemezek és a pillanatképek megengedett mérete.</span><span class="sxs-lookup"><span data-stu-id="81e6c-120">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e6c-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="81e6c-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="81e6c-122">A normál kezelt lemezek és a pillanatképek megengedett mérete.</span><span class="sxs-lookup"><span data-stu-id="81e6c-122">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e6c-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="81e6c-123">-VirtualMachineCount</span></span>
<span data-ttu-id="81e6c-124">Az engedélyezett virtuális gépek száma.</span><span class="sxs-lookup"><span data-stu-id="81e6c-124">Number  of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e6c-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="81e6c-125">-VmScaleSetCount</span></span>
<span data-ttu-id="81e6c-126">A megengedett méretarányok száma</span><span class="sxs-lookup"><span data-stu-id="81e6c-126">Number  of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e6c-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81e6c-127">-Confirm</span></span>
<span data-ttu-id="81e6c-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81e6c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81e6c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81e6c-129">-WhatIf</span></span>
<span data-ttu-id="81e6c-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81e6c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81e6c-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81e6c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81e6c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e6c-132">CommonParameters</span></span>
<span data-ttu-id="81e6c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81e6c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e6c-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81e6c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e6c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81e6c-135">INPUTS</span></span>

## <span data-ttu-id="81e6c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81e6c-136">OUTPUTS</span></span>

### <span data-ttu-id="81e6c-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="81e6c-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="81e6c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81e6c-138">NOTES</span></span>

## <span data-ttu-id="81e6c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81e6c-139">RELATED LINKS</span></span>

