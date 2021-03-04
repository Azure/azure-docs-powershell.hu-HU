---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 16ea3a8754ef08e933412582f100296d07fcb430
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922057"
---
# <span data-ttu-id="df8e2-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="df8e2-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="df8e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="df8e2-103">Beállítja a VMSS frissítés közbeni frissítési házirend tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="df8e2-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="df8e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="df8e2-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df8e2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="df8e2-105">DESCRIPTION</span></span>
<span data-ttu-id="df8e2-106">Beállítja a VMSS frissítés közbeni frissítési házirend tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="df8e2-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="df8e2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="df8e2-107">EXAMPLES</span></span>

### <span data-ttu-id="df8e2-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="df8e2-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="df8e2-109">Ez a parancs 40 százalékot állít be a MaxBatchInstance, 35 százalékot a MaxUnhealthyInstance, 30%-ot a MaxUnhealthyUpgradedInstance és 30 másodperc szüneti időt a VMSS helyi objektumkötegek $vmss.</span><span class="sxs-lookup"><span data-stu-id="df8e2-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="df8e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df8e2-110">PARAMETERS</span></span>

### <span data-ttu-id="df8e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df8e2-111">-DefaultProfile</span></span>
<span data-ttu-id="df8e2-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df8e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df8e2-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="df8e2-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="df8e2-114">Az összes virtuális gépi példánynak az a maximális százalékos aránya, amelyet egy kötegben a frissítéssel egyidejűleg frissít a rendszer.</span><span class="sxs-lookup"><span data-stu-id="df8e2-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="df8e2-115">Mivel ez a maximális, nem biztonságos példányok korábbi vagy jövőbeli kötegek esetén, a nagyobb megbízhatóság érdekében csökkentheti a kötegek példányainak százalékos arányát.</span><span class="sxs-lookup"><span data-stu-id="df8e2-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="df8e2-116">Ha az érték nincs megadva, akkor a 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="df8e2-116">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="df8e2-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="df8e2-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="df8e2-118">A méretaránykészletben található összes virtuális gépi példánynak az a maximális százalékos értéke, amely egyidejűleg egészségtelen lehet, akár frissítés eredményeként, akár a virtuális gép állapot-ellenőrzése során nem megfelelő állapotban található a frissítés megszakítása előtt.</span><span class="sxs-lookup"><span data-stu-id="df8e2-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="df8e2-119">Ezt a kényszert a köteg kezdése előtt ellenőrizni fogjuk.</span><span class="sxs-lookup"><span data-stu-id="df8e2-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="df8e2-120">Ha az érték nincs megadva, akkor a 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="df8e2-120">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="df8e2-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="df8e2-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="df8e2-122">A frissített virtuális gépi példányok azon maximális százalékos értéke, amely nem megfelelő állapotban van.</span><span class="sxs-lookup"><span data-stu-id="df8e2-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="df8e2-123">Ez az ellenőrzés az egyes kötegek frissítése után fog megtörténni.</span><span class="sxs-lookup"><span data-stu-id="df8e2-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="df8e2-124">Ha túllépi ezt a százalékos arányt, a görgető frissítés megszakad.</span><span class="sxs-lookup"><span data-stu-id="df8e2-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="df8e2-125">Ha az érték nincs megadva, akkor a 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="df8e2-125">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="df8e2-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="df8e2-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="df8e2-127">A frissítés befejezése és a következő köteg megkezdése közötti várakozási idő az összes virtuális gépre egy kötegben.</span><span class="sxs-lookup"><span data-stu-id="df8e2-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="df8e2-128">Az időidőtartamot ISO 8601 formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="df8e2-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="df8e2-129">Az alapértelmezett érték 0 másodperc (PT0S).</span><span class="sxs-lookup"><span data-stu-id="df8e2-129">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="df8e2-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="df8e2-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="df8e2-131">A VMSS-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="df8e2-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="df8e2-132">Az objektum létrehozásához használhatja New-AzVmssConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="df8e2-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="df8e2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df8e2-133">-Confirm</span></span>
<span data-ttu-id="df8e2-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="df8e2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df8e2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df8e2-135">-WhatIf</span></span>
<span data-ttu-id="df8e2-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="df8e2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df8e2-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df8e2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df8e2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df8e2-138">CommonParameters</span></span>
<span data-ttu-id="df8e2-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df8e2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df8e2-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df8e2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df8e2-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df8e2-141">INPUTS</span></span>

### <span data-ttu-id="df8e2-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="df8e2-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="df8e2-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="df8e2-143">System.Int32</span></span>

### <span data-ttu-id="df8e2-144">System.String</span><span class="sxs-lookup"><span data-stu-id="df8e2-144">System.String</span></span>

## <span data-ttu-id="df8e2-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df8e2-145">OUTPUTS</span></span>

### <span data-ttu-id="df8e2-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="df8e2-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="df8e2-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="df8e2-147">NOTES</span></span>

## <span data-ttu-id="df8e2-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df8e2-148">RELATED LINKS</span></span>
