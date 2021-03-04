---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 95622cba86c39b52b850b017ac370ea71dc2f84d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931402"
---
# <span data-ttu-id="255c0-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="255c0-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="255c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="255c0-102">SYNOPSIS</span></span>
<span data-ttu-id="255c0-103">Galériakép-verzió létrehozása</span><span class="sxs-lookup"><span data-stu-id="255c0-103">Create a gallery image version.</span></span>

## <span data-ttu-id="255c0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="255c0-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="255c0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="255c0-105">DESCRIPTION</span></span>
<span data-ttu-id="255c0-106">Galériakép-verzió létrehozása</span><span class="sxs-lookup"><span data-stu-id="255c0-106">Create a gallery image version.</span></span>

## <span data-ttu-id="255c0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="255c0-107">EXAMPLES</span></span>

### <span data-ttu-id="255c0-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="255c0-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="255c0-109">Galériakép-verzió létrehozása</span><span class="sxs-lookup"><span data-stu-id="255c0-109">Create a gallery image version.</span></span>

### <span data-ttu-id="255c0-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="255c0-110">Example 2</span></span>
```powershell
PS C:\> $osDiskImageEncryption = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES'}
PS C:\> $dataDiskImageEncryption1 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES1';Lun=1}
PS C:\> $dataDiskImageEncryption2 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES2';Lun=2}
PS C:\> $dataDiskImageEncryptions = @($dataDiskImageEncryption1,$dataDiskImageEncryption2)
PS C:\> $encryption1 = @{OSDiskImage=$osDiskImageEncryption;DataDiskImages=$dataDiskImageEncryptions}
PS C:\> $region1 = @{Name='West US';ReplicaCount=1;StorageAccountType=Standard_LRS;Encryption=$encryption1}
PS C:\> $targetRegions = @{$region1}
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $SourceImageId -ReplicaCount 2 -StorageAccountType Standard_LRS -PublishingProfileExcludeFromLatest -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegion
```

<span data-ttu-id="255c0-111">Lemez képtitkosítással létrehozhat egy galériaképverziót.</span><span class="sxs-lookup"><span data-stu-id="255c0-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="255c0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="255c0-112">PARAMETERS</span></span>

### <span data-ttu-id="255c0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="255c0-113">-AsJob</span></span>
<span data-ttu-id="255c0-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="255c0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="255c0-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="255c0-115">-DataDiskImage</span></span>
<span data-ttu-id="255c0-116">Adatlemezek képei.</span><span class="sxs-lookup"><span data-stu-id="255c0-116">Data disk images.</span></span>   <span data-ttu-id="255c0-117">például @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span><span class="sxs-lookup"><span data-stu-id="255c0-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryDataDiskImage[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="255c0-118">-DefaultProfile</span></span>
<span data-ttu-id="255c0-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="255c0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="255c0-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="255c0-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="255c0-121">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="255c0-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c0-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="255c0-122">-GalleryName</span></span>
<span data-ttu-id="255c0-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="255c0-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c0-124">-Location</span><span class="sxs-lookup"><span data-stu-id="255c0-124">-Location</span></span>
<span data-ttu-id="255c0-125">Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="255c0-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="255c0-126">-Name</span></span>
<span data-ttu-id="255c0-127">A galériakép verziószámának neve.</span><span class="sxs-lookup"><span data-stu-id="255c0-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c0-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="255c0-128">-OSDiskImage</span></span>
<span data-ttu-id="255c0-129">Os lemez képe például @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span><span class="sxs-lookup"><span data-stu-id="255c0-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryOSDiskImage
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c0-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="255c0-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="255c0-131">A galéria Képverzió életciklusának vége.</span><span class="sxs-lookup"><span data-stu-id="255c0-131">The end of life date of the gallery Image Version.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c0-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="255c0-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="255c0-133">Ha be van állítva, a Képdefiníció legújabb verziójából telepített virtuális gépek nem fogják használni ezt a képverziót.</span><span class="sxs-lookup"><span data-stu-id="255c0-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c0-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="255c0-134">-ReplicaCount</span></span>
<span data-ttu-id="255c0-135">A képverzió régiónként létrehozható másolatainak száma.</span><span class="sxs-lookup"><span data-stu-id="255c0-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="255c0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="255c0-136">-ResourceGroupName</span></span>
<span data-ttu-id="255c0-137">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="255c0-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c0-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="255c0-138">-SourceImageId</span></span>
<span data-ttu-id="255c0-139">Annak a forrásképnek az azonosítója, amelyből a képverziót létre fogja hozatni.</span><span class="sxs-lookup"><span data-stu-id="255c0-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="255c0-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="255c0-140">-StorageAccountType</span></span>
<span data-ttu-id="255c0-141">A kép tárolásához használt tárfiók típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="255c0-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="255c0-142">Ez a tulajdonság nem frissíthető.</span><span class="sxs-lookup"><span data-stu-id="255c0-142">This property is not updatable.</span></span> <span data-ttu-id="255c0-143">A rendelkezésre álló értékek Standard_LRS, Standard_ZRS és Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="255c0-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

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

### <span data-ttu-id="255c0-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="255c0-144">-Tag</span></span>
<span data-ttu-id="255c0-145">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="255c0-145">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c0-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="255c0-146">-TargetRegion</span></span>
<span data-ttu-id="255c0-147">A célterület, ahová a képverzió replikálva lesz.</span><span class="sxs-lookup"><span data-stu-id="255c0-147">The target regions where the Image Version is going to be replicated to.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255c0-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="255c0-148">-Confirm</span></span>
<span data-ttu-id="255c0-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="255c0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="255c0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="255c0-150">-WhatIf</span></span>
<span data-ttu-id="255c0-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="255c0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="255c0-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="255c0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="255c0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255c0-153">CommonParameters</span></span>
<span data-ttu-id="255c0-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="255c0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255c0-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="255c0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255c0-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="255c0-156">INPUTS</span></span>

### <span data-ttu-id="255c0-157">System.String</span><span class="sxs-lookup"><span data-stu-id="255c0-157">System.String</span></span>

### <span data-ttu-id="255c0-158">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="255c0-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="255c0-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="255c0-159">System.Int32</span></span>

### <span data-ttu-id="255c0-160">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="255c0-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="255c0-161">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="255c0-161">System.DateTime</span></span>

### <span data-ttu-id="255c0-162">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="255c0-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="255c0-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="255c0-163">OUTPUTS</span></span>

### <span data-ttu-id="255c0-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="255c0-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="255c0-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="255c0-165">NOTES</span></span>

## <span data-ttu-id="255c0-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="255c0-166">RELATED LINKS</span></span>
