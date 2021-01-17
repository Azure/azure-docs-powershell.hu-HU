---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480900"
---
# <span data-ttu-id="571e3-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="571e3-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="571e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="571e3-102">SYNOPSIS</span></span>
<span data-ttu-id="571e3-103">Hozzáad egy adatlemezt a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="571e3-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="571e3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="571e3-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="571e3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="571e3-105">DESCRIPTION</span></span>
<span data-ttu-id="571e3-106">Az **Add-AzVmssDataDisk** parancsmag hozzáad egy adatlemezt a VIRTUÁLISgép-mérethalmaz (VMSS) példányhoz.</span><span class="sxs-lookup"><span data-stu-id="571e3-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="571e3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="571e3-107">EXAMPLES</span></span>

### <span data-ttu-id="571e3-108">1. példa: Adatlemez hozzáadása</span><span class="sxs-lookup"><span data-stu-id="571e3-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="571e3-109">Ez a parancs egy üres adatlemezt ad a VMSS-objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="571e3-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="571e3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="571e3-110">PARAMETERS</span></span>

### <span data-ttu-id="571e3-111">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="571e3-111">-Caching</span></span>
<span data-ttu-id="571e3-112">A lemez gyorsítótárának típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="571e3-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="571e3-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="571e3-113">-CreateOption</span></span>
<span data-ttu-id="571e3-114">A lemez létrehozási beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="571e3-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="571e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="571e3-115">-DefaultProfile</span></span>
<span data-ttu-id="571e3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="571e3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="571e3-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="571e3-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="571e3-118">Az ügyfél által felügyelt lemeztitkosítási készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="571e3-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="571e3-119">Ez csak felügyelt lemezhez lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="571e3-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="571e3-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="571e3-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="571e3-121">A felügyelt lemez Read-Write IOPS-át adja meg.</span><span class="sxs-lookup"><span data-stu-id="571e3-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="571e3-122">Csak akkor érdemes használni, ha a StorageAccountType UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="571e3-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="571e3-123">Ha nincs megadva, a rendszer a diskSizeGB alapján rendeli hozzá az alapértelmezett értéket.</span><span class="sxs-lookup"><span data-stu-id="571e3-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

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

### <span data-ttu-id="571e3-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="571e3-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="571e3-125">A felügyelt lemez sávszélességét adja meg MB/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="571e3-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="571e3-126">Csak akkor érdemes használni, ha a StorageAccountType UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="571e3-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="571e3-127">Ha nincs megadva, a rendszer a diskSizeGB alapján rendeli hozzá az alapértelmezett értéket.</span><span class="sxs-lookup"><span data-stu-id="571e3-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

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

### <span data-ttu-id="571e3-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="571e3-128">-DiskSizeGB</span></span>
<span data-ttu-id="571e3-129">A lemez mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="571e3-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="571e3-130">-Lun</span><span class="sxs-lookup"><span data-stu-id="571e3-130">-Lun</span></span>
<span data-ttu-id="571e3-131">A lemez logikai egységszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="571e3-131">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="571e3-132">-Name</span><span class="sxs-lookup"><span data-stu-id="571e3-132">-Name</span></span>
<span data-ttu-id="571e3-133">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="571e3-133">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="571e3-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="571e3-134">-StorageAccountType</span></span>
<span data-ttu-id="571e3-135">A lemez tárfióktípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="571e3-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="571e3-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="571e3-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="571e3-137">Adja meg a VMSS-objektumot.</span><span class="sxs-lookup"><span data-stu-id="571e3-137">Specify the VMSS object.</span></span>
<span data-ttu-id="571e3-138">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="571e3-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="571e3-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="571e3-139">-WriteAccelerator</span></span>
<span data-ttu-id="571e3-140">Azt adja meg, hogy a WriteAccelerator engedélyezve vagy letiltva legyen-e az adatlemezen.</span><span class="sxs-lookup"><span data-stu-id="571e3-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="571e3-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="571e3-141">-Confirm</span></span>
<span data-ttu-id="571e3-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="571e3-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="571e3-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="571e3-143">-WhatIf</span></span>
<span data-ttu-id="571e3-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="571e3-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="571e3-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="571e3-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="571e3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="571e3-146">CommonParameters</span></span>
<span data-ttu-id="571e3-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="571e3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="571e3-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="571e3-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="571e3-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="571e3-149">INPUTS</span></span>

### <span data-ttu-id="571e3-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="571e3-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="571e3-151">System.String</span><span class="sxs-lookup"><span data-stu-id="571e3-151">System.String</span></span>

### <span data-ttu-id="571e3-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="571e3-152">System.Int32</span></span>

### <span data-ttu-id="571e3-153">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="571e3-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="571e3-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="571e3-154">OUTPUTS</span></span>

### <span data-ttu-id="571e3-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="571e3-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="571e3-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="571e3-156">NOTES</span></span>

## <span data-ttu-id="571e3-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="571e3-157">RELATED LINKS</span></span>
