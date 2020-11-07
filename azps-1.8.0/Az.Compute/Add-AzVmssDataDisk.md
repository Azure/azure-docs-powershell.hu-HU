---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: df4a3676d86027c4b2e8627e8eae87dcb84644c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671377"
---
# <span data-ttu-id="946b2-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="946b2-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="946b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="946b2-102">SYNOPSIS</span></span>
<span data-ttu-id="946b2-103">Adatlemez felvétele a VMSS.</span><span class="sxs-lookup"><span data-stu-id="946b2-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="946b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="946b2-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="946b2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="946b2-105">DESCRIPTION</span></span>
<span data-ttu-id="946b2-106">Az **Add-AzVmssDataDisk** parancsmag adatlemezt ad hozzá a Virtual Machine Scale set (VMSS) példányhoz.</span><span class="sxs-lookup"><span data-stu-id="946b2-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="946b2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="946b2-107">EXAMPLES</span></span>

### <span data-ttu-id="946b2-108">1. példa: adatlemez hozzáadása</span><span class="sxs-lookup"><span data-stu-id="946b2-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="946b2-109">Ez a parancs üres adatlemezt ad a VMSS objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="946b2-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="946b2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="946b2-110">PARAMETERS</span></span>

### <span data-ttu-id="946b2-111">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="946b2-111">-Caching</span></span>
<span data-ttu-id="946b2-112">A lemez gyorsítótár-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="946b2-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="946b2-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="946b2-113">-CreateOption</span></span>
<span data-ttu-id="946b2-114">A lemez létrehozási beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="946b2-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="946b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946b2-115">-DefaultProfile</span></span>
<span data-ttu-id="946b2-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="946b2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="946b2-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="946b2-117">-DiskSizeGB</span></span>
<span data-ttu-id="946b2-118">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="946b2-118">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="946b2-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="946b2-119">-Lun</span></span>
<span data-ttu-id="946b2-120">A lemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="946b2-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="946b2-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="946b2-121">-Name</span></span>
<span data-ttu-id="946b2-122">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="946b2-122">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="946b2-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="946b2-123">-StorageAccountType</span></span>
<span data-ttu-id="946b2-124">A lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="946b2-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="946b2-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="946b2-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="946b2-126">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="946b2-126">Specify the VMSS object.</span></span>
<span data-ttu-id="946b2-127">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="946b2-127">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="946b2-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="946b2-128">-WriteAccelerator</span></span>
<span data-ttu-id="946b2-129">Itt adhatja meg, hogy az adatlemezen engedélyezni vagy letiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="946b2-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946b2-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="946b2-130">-Confirm</span></span>
<span data-ttu-id="946b2-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="946b2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="946b2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="946b2-132">-WhatIf</span></span>
<span data-ttu-id="946b2-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="946b2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="946b2-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="946b2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="946b2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946b2-135">CommonParameters</span></span>
<span data-ttu-id="946b2-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="946b2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946b2-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="946b2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946b2-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="946b2-138">INPUTS</span></span>

### <span data-ttu-id="946b2-139">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="946b2-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="946b2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="946b2-140">System.String</span></span>

### <span data-ttu-id="946b2-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="946b2-141">System.Int32</span></span>

### <span data-ttu-id="946b2-142">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. CachingTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="946b2-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="946b2-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="946b2-143">OUTPUTS</span></span>

### <span data-ttu-id="946b2-144">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="946b2-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="946b2-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="946b2-145">NOTES</span></span>

## <span data-ttu-id="946b2-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="946b2-146">RELATED LINKS</span></span>
