---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024848"
---
# <span data-ttu-id="989fe-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="989fe-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="989fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="989fe-102">SYNOPSIS</span></span>
<span data-ttu-id="989fe-103">Adatlemez felvétele a VMSS.</span><span class="sxs-lookup"><span data-stu-id="989fe-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="989fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="989fe-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="989fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="989fe-105">DESCRIPTION</span></span>
<span data-ttu-id="989fe-106">Az **Add-AzVmssDataDisk** parancsmag adatlemezt ad hozzá a Virtual Machine Scale set (VMSS) példányhoz.</span><span class="sxs-lookup"><span data-stu-id="989fe-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="989fe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="989fe-107">EXAMPLES</span></span>

### <span data-ttu-id="989fe-108">1. példa: adatlemez hozzáadása</span><span class="sxs-lookup"><span data-stu-id="989fe-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="989fe-109">Ez a parancs üres adatlemezt ad a VMSS objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="989fe-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="989fe-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="989fe-110">PARAMETERS</span></span>

### <span data-ttu-id="989fe-111">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="989fe-111">-Caching</span></span>
<span data-ttu-id="989fe-112">A lemez gyorsítótár-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="989fe-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="989fe-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="989fe-113">-CreateOption</span></span>
<span data-ttu-id="989fe-114">A lemez létrehozási beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="989fe-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="989fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989fe-115">-DefaultProfile</span></span>
<span data-ttu-id="989fe-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="989fe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="989fe-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="989fe-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="989fe-118">Az ügyfél által felügyelt lemezvezérlő-titkosítási készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="989fe-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="989fe-119">Ezt csak a felügyelt lemezek esetében lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="989fe-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="989fe-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="989fe-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="989fe-121">A kezelt lemez Read-Write IOPS adja meg.</span><span class="sxs-lookup"><span data-stu-id="989fe-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="989fe-122">Csak akkor használható, ha a StorageAccountType UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="989fe-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="989fe-123">Ha nincs megadva, az alapértelmezett érték a diskSizeGB alapján lesz kiosztva.</span><span class="sxs-lookup"><span data-stu-id="989fe-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="989fe-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="989fe-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="989fe-125">A kezelt lemez MEGABÁJT/másodpercben megadott sávszélességét adja meg.</span><span class="sxs-lookup"><span data-stu-id="989fe-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="989fe-126">Csak akkor használható, ha a StorageAccountType UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="989fe-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="989fe-127">Ha nincs megadva, az alapértelmezett érték a diskSizeGB alapján lesz kiosztva.</span><span class="sxs-lookup"><span data-stu-id="989fe-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="989fe-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="989fe-128">-DiskSizeGB</span></span>
<span data-ttu-id="989fe-129">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="989fe-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="989fe-130">-LUN</span><span class="sxs-lookup"><span data-stu-id="989fe-130">-Lun</span></span>
<span data-ttu-id="989fe-131">A lemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="989fe-131">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="989fe-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="989fe-132">-Name</span></span>
<span data-ttu-id="989fe-133">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="989fe-133">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="989fe-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="989fe-134">-StorageAccountType</span></span>
<span data-ttu-id="989fe-135">A lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="989fe-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="989fe-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="989fe-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="989fe-137">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="989fe-137">Specify the VMSS object.</span></span>
<span data-ttu-id="989fe-138">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="989fe-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="989fe-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="989fe-139">-WriteAccelerator</span></span>
<span data-ttu-id="989fe-140">Itt adhatja meg, hogy az adatlemezen engedélyezni vagy letiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="989fe-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="989fe-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="989fe-141">-Confirm</span></span>
<span data-ttu-id="989fe-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="989fe-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="989fe-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="989fe-143">-WhatIf</span></span>
<span data-ttu-id="989fe-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="989fe-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="989fe-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="989fe-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="989fe-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989fe-146">CommonParameters</span></span>
<span data-ttu-id="989fe-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="989fe-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989fe-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="989fe-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989fe-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="989fe-149">INPUTS</span></span>

### <span data-ttu-id="989fe-150">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="989fe-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="989fe-151">System. String</span><span class="sxs-lookup"><span data-stu-id="989fe-151">System.String</span></span>

### <span data-ttu-id="989fe-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="989fe-152">System.Int32</span></span>

### <span data-ttu-id="989fe-153">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. CachingTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="989fe-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="989fe-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="989fe-154">OUTPUTS</span></span>

### <span data-ttu-id="989fe-155">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="989fe-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="989fe-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="989fe-156">NOTES</span></span>

## <span data-ttu-id="989fe-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="989fe-157">RELATED LINKS</span></span>
