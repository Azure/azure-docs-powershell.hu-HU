---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: b3380b367cd66989b46b1171d6696cfc60fc815e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844166"
---
# <span data-ttu-id="76e74-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="76e74-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="76e74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76e74-102">SYNOPSIS</span></span>
<span data-ttu-id="76e74-103">A VMSS-es folyamatos frissítési házirend tulajdonságainak megadása</span><span class="sxs-lookup"><span data-stu-id="76e74-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="76e74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76e74-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76e74-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="76e74-105">DESCRIPTION</span></span>
<span data-ttu-id="76e74-106">A VMSS-es folyamatos frissítési házirend tulajdonságainak megadása</span><span class="sxs-lookup"><span data-stu-id="76e74-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="76e74-107">Példák</span><span class="sxs-lookup"><span data-stu-id="76e74-107">EXAMPLES</span></span>

### <span data-ttu-id="76e74-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="76e74-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="76e74-109">Ez a parancs beállítja a 40 százalékát a MaxBatchInstance, az 35 százalékát a MaxUnhealthyInstance, 30 százaléknál a MaxUnhealthyUpgradedInstance és 30 másodperc szünetet a VMSS helyi $vmss objektumokhoz tartozó kötegek között.</span><span class="sxs-lookup"><span data-stu-id="76e74-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="76e74-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76e74-110">PARAMETERS</span></span>

### <span data-ttu-id="76e74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e74-111">-DefaultProfile</span></span>
<span data-ttu-id="76e74-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76e74-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e74-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="76e74-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="76e74-114">Annak a virtuális gép-példányoknak a maximális százalékos aránya, amelyet a rendszer egy kötegben a folyamatos frissítéssel egyidejűleg frissít.</span><span class="sxs-lookup"><span data-stu-id="76e74-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="76e74-115">Mivel az előző vagy a jövőbeli kötegekben ez a maximális, egészségtelen előfordulás, a kötegben lévő példányok százalékos arányát a nagyobb megbízhatóság érdekében is csökkentheti.</span><span class="sxs-lookup"><span data-stu-id="76e74-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="76e74-116">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="76e74-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e74-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="76e74-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="76e74-118">A teljes virtuálisgép-példányok maximális százalékos aránya a készletben, amely egyidejű egészségtelen lehet, akár a frissítés során, akár a virtuálisgép-állapot ellenőrzésekor, a frissítés megszakítása előtt.</span><span class="sxs-lookup"><span data-stu-id="76e74-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="76e74-119">Ezt a korlátozást a program minden köteg kezdése előtt ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="76e74-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="76e74-120">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="76e74-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e74-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="76e74-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="76e74-122">A frissített virtuálisgép-példányok maximális százaléka, amely egészségtelen állapotban található.</span><span class="sxs-lookup"><span data-stu-id="76e74-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="76e74-123">Ez az ellenőrzés minden köteg frissítésekor megtörténik.</span><span class="sxs-lookup"><span data-stu-id="76e74-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="76e74-124">Ha a százalékos érték túllépve, a gördülési frissítés leáll.</span><span class="sxs-lookup"><span data-stu-id="76e74-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="76e74-125">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="76e74-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e74-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="76e74-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="76e74-127">Az egy kötegben lévő összes virtuális gép frissítésének várakozási ideje, és a következő köteg indítása.</span><span class="sxs-lookup"><span data-stu-id="76e74-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="76e74-128">Az időtartamot az ISO 8601-formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="76e74-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="76e74-129">Az alapértelmezett érték a 0 másodperc (PT0S).</span><span class="sxs-lookup"><span data-stu-id="76e74-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76e74-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="76e74-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="76e74-131">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="76e74-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="76e74-132">Az objektum létrehozásához az New-AzVmssConfig parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="76e74-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76e74-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="76e74-133">-Confirm</span></span>
<span data-ttu-id="76e74-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76e74-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76e74-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76e74-135">-WhatIf</span></span>
<span data-ttu-id="76e74-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="76e74-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76e74-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76e74-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76e74-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e74-138">CommonParameters</span></span>
<span data-ttu-id="76e74-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76e74-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e74-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76e74-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e74-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76e74-141">INPUTS</span></span>

### <span data-ttu-id="76e74-142">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="76e74-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="76e74-143">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="76e74-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="76e74-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76e74-144">OUTPUTS</span></span>

### <span data-ttu-id="76e74-145">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="76e74-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="76e74-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76e74-146">NOTES</span></span>

## <span data-ttu-id="76e74-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76e74-147">RELATED LINKS</span></span>

