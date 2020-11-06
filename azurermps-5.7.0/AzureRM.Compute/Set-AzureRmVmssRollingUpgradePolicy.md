---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
ms.openlocfilehash: f77e018f464ffe7329d8b89cb74b8c44359d8a3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492351"
---
# <span data-ttu-id="d6d29-101">Set-AzureRmVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="d6d29-101">Set-AzureRmVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="d6d29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6d29-102">SYNOPSIS</span></span>
<span data-ttu-id="d6d29-103">A VMSS-es folyamatos frissítési házirend tulajdonságainak megadása</span><span class="sxs-lookup"><span data-stu-id="d6d29-103">Sets the VMSS rolling upgrade policy properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6d29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6d29-104">SYNTAX</span></span>

```
Set-AzureRmVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6d29-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6d29-105">DESCRIPTION</span></span>
<span data-ttu-id="d6d29-106">A VMSS-es folyamatos frissítési házirend tulajdonságainak megadása</span><span class="sxs-lookup"><span data-stu-id="d6d29-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="d6d29-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d6d29-107">EXAMPLES</span></span>

### <span data-ttu-id="d6d29-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d6d29-108">Example 1</span></span>
```
PS C:\> Set-AzureRmVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="d6d29-109">Ez a parancs beállítja a 40 százalékát a MaxBatchInstance, az 35 százalékát a MaxUnhealthyInstance, 30 százaléknál a MaxUnhealthyUpgradedInstance és 30 másodperc szünetet a VMSS helyi $vmss objektumokhoz tartozó kötegek között.</span><span class="sxs-lookup"><span data-stu-id="d6d29-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="d6d29-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6d29-110">PARAMETERS</span></span>

### <span data-ttu-id="d6d29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6d29-111">-DefaultProfile</span></span>
<span data-ttu-id="d6d29-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6d29-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6d29-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d6d29-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="d6d29-114">Annak a virtuális gép-példányoknak a maximális százalékos aránya, amelyet a rendszer egy kötegben a folyamatos frissítéssel egyidejűleg frissít.</span><span class="sxs-lookup"><span data-stu-id="d6d29-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="d6d29-115">Mivel az előző vagy a jövőbeli kötegekben ez a maximális, egészségtelen előfordulás, a kötegben lévő példányok százalékos arányát a nagyobb megbízhatóság érdekében is csökkentheti.</span><span class="sxs-lookup"><span data-stu-id="d6d29-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="d6d29-116">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="d6d29-116">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="d6d29-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d6d29-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="d6d29-118">A teljes virtuálisgép-példányok maximális százalékos aránya a készletben, amely egyidejű egészségtelen lehet, akár a frissítés során, akár a virtuálisgép-állapot ellenőrzésekor, a frissítés megszakítása előtt.</span><span class="sxs-lookup"><span data-stu-id="d6d29-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="d6d29-119">Ezt a korlátozást a program minden köteg kezdése előtt ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="d6d29-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="d6d29-120">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="d6d29-120">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="d6d29-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d6d29-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="d6d29-122">A frissített virtuálisgép-példányok maximális százaléka, amely egészségtelen állapotban található.</span><span class="sxs-lookup"><span data-stu-id="d6d29-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="d6d29-123">Ez az ellenőrzés minden köteg frissítésekor megtörténik.</span><span class="sxs-lookup"><span data-stu-id="d6d29-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="d6d29-124">Ha a százalékos érték túllépve, a gördülési frissítés leáll.</span><span class="sxs-lookup"><span data-stu-id="d6d29-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="d6d29-125">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="d6d29-125">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="d6d29-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="d6d29-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="d6d29-127">Az egy kötegben lévő összes virtuális gép frissítésének várakozási ideje, és a következő köteg indítása.</span><span class="sxs-lookup"><span data-stu-id="d6d29-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="d6d29-128">Az időtartamot az ISO 8601-formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="d6d29-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="d6d29-129">Az alapértelmezett érték a 0 másodperc (PT0S).</span><span class="sxs-lookup"><span data-stu-id="d6d29-129">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="d6d29-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d6d29-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d6d29-131">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6d29-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="d6d29-132">Az objektum létrehozásához az New-AzureRmVmssConfig parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="d6d29-132">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="d6d29-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6d29-133">-Confirm</span></span>
<span data-ttu-id="d6d29-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6d29-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6d29-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6d29-135">-WhatIf</span></span>
<span data-ttu-id="d6d29-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6d29-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6d29-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6d29-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6d29-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6d29-138">CommonParameters</span></span>
<span data-ttu-id="d6d29-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6d29-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6d29-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6d29-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6d29-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6d29-141">INPUTS</span></span>

### <span data-ttu-id="d6d29-142">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d6d29-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="d6d29-143">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="d6d29-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="d6d29-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6d29-144">OUTPUTS</span></span>

### <span data-ttu-id="d6d29-145">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d6d29-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d6d29-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6d29-146">NOTES</span></span>

## <span data-ttu-id="d6d29-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6d29-147">RELATED LINKS</span></span>
