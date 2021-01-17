---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 7274067b2f8daa916a0021f0ea2fd7985e1914ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480679"
---
# <span data-ttu-id="d0bf7-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="d0bf7-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="d0bf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0bf7-102">SYNOPSIS</span></span>
<span data-ttu-id="d0bf7-103">Beállítja a VMSS frissítés közbeni frissítési házirend tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="d0bf7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d0bf7-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0bf7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d0bf7-105">DESCRIPTION</span></span>
<span data-ttu-id="d0bf7-106">Beállítja a VMSS frissítés közbeni frissítési házirend tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="d0bf7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d0bf7-107">EXAMPLES</span></span>

### <span data-ttu-id="d0bf7-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d0bf7-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="d0bf7-109">Ez a parancs 40 százalékot állít be a MaxBatchInstance, 35 százalékot a MaxUnhealthyInstance, 30%-ot a MaxUnhealthyUpgradedInstance és 30 másodperc szüneti időt a VMSS helyi objektum-$vmss.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="d0bf7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0bf7-110">PARAMETERS</span></span>

### <span data-ttu-id="d0bf7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0bf7-111">-DefaultProfile</span></span>
<span data-ttu-id="d0bf7-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0bf7-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d0bf7-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="d0bf7-114">Az összes virtuális gépi példánynak az a maximális százaléka, amelyet egy kötegben a frissítéssel egyidejűleg frissít a rendszer.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="d0bf7-115">Mivel ez egy korábbi vagy jövőbeli kötegben a maximális, nem biztonságos példányok száma, a nagyobb megbízhatóság érdekében a kötegek példányainak százalékos aránya csökkenhet.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="d0bf7-116">Ha az érték nincs megadva, akkor a 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0bf7-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d0bf7-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="d0bf7-118">A méretaránykészletben lévő összes virtuális gépi példánynak az a maximális százalékos értéke, amely egyidejűleg nem megfelelő működésű lehet, akár frissítés eredményeként, akár a virtuális gép állapot-ellenőrzése során nem megfelelő állapotban lévő állapot esetén, a frissítés megszakítása előtt.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="d0bf7-119">Ezt a kényszert a köteg kezdése előtt ellenőrizni fogjuk.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="d0bf7-120">Ha az érték nincs megadva, akkor a 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0bf7-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d0bf7-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="d0bf7-122">A frissített virtuális gépi példányok azon maximális százalékos aránya, amely nem megfelelő állapotban van.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="d0bf7-123">Ez az ellenőrzés az egyes kötegek frissítése után fog megtörténni.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="d0bf7-124">Ha túllépi ezt a százalékos arányt, a görgető frissítés megszakad.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="d0bf7-125">Ha az érték nincs megadva, akkor a 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0bf7-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="d0bf7-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="d0bf7-127">Várakozási idő egy kötegben az összes virtuális gép frissítésének befejezése és a következő köteg indítása között.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="d0bf7-128">Az időidőtartamot ISO 8601 formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="d0bf7-129">Az alapértelmezett érték 0 másodperc (PT0S).</span><span class="sxs-lookup"><span data-stu-id="d0bf7-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0bf7-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d0bf7-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d0bf7-131">A VMSS-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="d0bf7-132">Az objektum létrehozásához használhatja New-AzVmssConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0bf7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0bf7-133">-Confirm</span></span>
<span data-ttu-id="d0bf7-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0bf7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0bf7-135">-WhatIf</span></span>
<span data-ttu-id="d0bf7-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0bf7-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0bf7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0bf7-138">CommonParameters</span></span>
<span data-ttu-id="d0bf7-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0bf7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0bf7-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0bf7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0bf7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0bf7-141">INPUTS</span></span>

### <span data-ttu-id="d0bf7-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d0bf7-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d0bf7-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d0bf7-143">System.Int32</span></span>

### <span data-ttu-id="d0bf7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d0bf7-144">System.String</span></span>

## <span data-ttu-id="d0bf7-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0bf7-145">OUTPUTS</span></span>

### <span data-ttu-id="d0bf7-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d0bf7-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d0bf7-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d0bf7-147">NOTES</span></span>

## <span data-ttu-id="d0bf7-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0bf7-148">RELATED LINKS</span></span>
