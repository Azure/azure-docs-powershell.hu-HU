---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 8ef13dd067cd0cf1161e3aa58b52a961fe90a949
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187069"
---
# <span data-ttu-id="fa24a-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="fa24a-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="fa24a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa24a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa24a-103">Gyűjtemény képének létrehozása</span><span class="sxs-lookup"><span data-stu-id="fa24a-103">Create a gallery image version.</span></span>

## <span data-ttu-id="fa24a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa24a-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa24a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa24a-105">DESCRIPTION</span></span>
<span data-ttu-id="fa24a-106">Gyűjtemény képének létrehozása</span><span class="sxs-lookup"><span data-stu-id="fa24a-106">Create a gallery image version.</span></span>

## <span data-ttu-id="fa24a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fa24a-107">EXAMPLES</span></span>

### <span data-ttu-id="fa24a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fa24a-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="fa24a-109">Gyűjtemény képének létrehozása</span><span class="sxs-lookup"><span data-stu-id="fa24a-109">Create a gallery image version.</span></span>

### <span data-ttu-id="fa24a-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="fa24a-110">Example 2</span></span>
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

<span data-ttu-id="fa24a-111">Hozzon létre egy képgyűjteményt a képfájlok titkosításával.</span><span class="sxs-lookup"><span data-stu-id="fa24a-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="fa24a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa24a-112">PARAMETERS</span></span>

### <span data-ttu-id="fa24a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa24a-113">-AsJob</span></span>
<span data-ttu-id="fa24a-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fa24a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa24a-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="fa24a-115">-DataDiskImage</span></span>
<span data-ttu-id="fa24a-116">Data Disk images.</span><span class="sxs-lookup"><span data-stu-id="fa24a-116">Data disk images.</span></span>   <span data-ttu-id="fa24a-117">például @ {Source = @ {ID =<source_id>}; LUN = 1; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="fa24a-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

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

### <span data-ttu-id="fa24a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa24a-118">-DefaultProfile</span></span>
<span data-ttu-id="fa24a-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa24a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa24a-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="fa24a-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="fa24a-121">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="fa24a-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="fa24a-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="fa24a-122">-GalleryName</span></span>
<span data-ttu-id="fa24a-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="fa24a-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="fa24a-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="fa24a-124">-Location</span></span>
<span data-ttu-id="fa24a-125">Erőforrás-hely</span><span class="sxs-lookup"><span data-stu-id="fa24a-125">Resource location</span></span>

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

### <span data-ttu-id="fa24a-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fa24a-126">-Name</span></span>
<span data-ttu-id="fa24a-127">A gyűjtemény képének neve.</span><span class="sxs-lookup"><span data-stu-id="fa24a-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="fa24a-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="fa24a-128">-OSDiskImage</span></span>
<span data-ttu-id="fa24a-129">OS Disk Image (például @ {Source = @ {ID =<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="fa24a-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

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

### <span data-ttu-id="fa24a-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="fa24a-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="fa24a-131">A gyűjtemény képének befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="fa24a-131">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="fa24a-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="fa24a-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="fa24a-133">Ha be van állítva, akkor a kép definíciójának legújabb verziójáról telepített virtuális gépek nem fogják használni ezt a képváltozatot.</span><span class="sxs-lookup"><span data-stu-id="fa24a-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="fa24a-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="fa24a-134">-ReplicaCount</span></span>
<span data-ttu-id="fa24a-135">Az régiónként létrehozandó képverzió replikáinak száma.</span><span class="sxs-lookup"><span data-stu-id="fa24a-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="fa24a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa24a-136">-ResourceGroupName</span></span>
<span data-ttu-id="fa24a-137">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fa24a-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="fa24a-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="fa24a-138">-SourceImageId</span></span>
<span data-ttu-id="fa24a-139">Annak a forrásnak az azonosítója, amelyből a kép verziója lesz létrehozva.</span><span class="sxs-lookup"><span data-stu-id="fa24a-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="fa24a-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="fa24a-140">-StorageAccountType</span></span>
<span data-ttu-id="fa24a-141">A kép tárolásához használandó tárterület-típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="fa24a-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="fa24a-142">Ez a tulajdonság nem frissíthető.</span><span class="sxs-lookup"><span data-stu-id="fa24a-142">This property is not updatable.</span></span> <span data-ttu-id="fa24a-143">A rendelkezésre álló értékek a Standard_LRS, a Standard_ZRS és a Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="fa24a-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

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

### <span data-ttu-id="fa24a-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="fa24a-144">-Tag</span></span>
<span data-ttu-id="fa24a-145">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="fa24a-145">Resource tags</span></span>

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

### <span data-ttu-id="fa24a-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="fa24a-146">-TargetRegion</span></span>
<span data-ttu-id="fa24a-147">Azok a célterületek, amelyekben a képváltozatot replikálni fogja.</span><span class="sxs-lookup"><span data-stu-id="fa24a-147">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="fa24a-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fa24a-148">-Confirm</span></span>
<span data-ttu-id="fa24a-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fa24a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa24a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa24a-150">-WhatIf</span></span>
<span data-ttu-id="fa24a-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fa24a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa24a-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa24a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa24a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa24a-153">CommonParameters</span></span>
<span data-ttu-id="fa24a-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa24a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa24a-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fa24a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa24a-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa24a-156">INPUTS</span></span>

### <span data-ttu-id="fa24a-157">System. String</span><span class="sxs-lookup"><span data-stu-id="fa24a-157">System.String</span></span>

### <span data-ttu-id="fa24a-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fa24a-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fa24a-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fa24a-159">System.Int32</span></span>

### <span data-ttu-id="fa24a-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa24a-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fa24a-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="fa24a-161">System.DateTime</span></span>

### <span data-ttu-id="fa24a-162">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="fa24a-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="fa24a-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa24a-163">OUTPUTS</span></span>

### <span data-ttu-id="fa24a-164">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="fa24a-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="fa24a-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa24a-165">NOTES</span></span>

## <span data-ttu-id="fa24a-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa24a-166">RELATED LINKS</span></span>
