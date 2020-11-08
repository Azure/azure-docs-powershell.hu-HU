---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024754"
---
# <span data-ttu-id="ee7b9-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="ee7b9-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="ee7b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee7b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ee7b9-103">Általános terjesztési objektum</span><span class="sxs-lookup"><span data-stu-id="ee7b9-103">Generic distribution object</span></span>

## <span data-ttu-id="ee7b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee7b9-104">SYNTAX</span></span>

### <span data-ttu-id="ee7b9-105">ManagedImageDistributor (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee7b9-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="ee7b9-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="ee7b9-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="ee7b9-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="ee7b9-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="ee7b9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee7b9-108">DESCRIPTION</span></span>
<span data-ttu-id="ee7b9-109">Általános terjesztési objektum</span><span class="sxs-lookup"><span data-stu-id="ee7b9-109">Generic distribution object</span></span>

## <span data-ttu-id="ee7b9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ee7b9-110">EXAMPLES</span></span>

### <span data-ttu-id="ee7b9-111">Példa 1: felügyelt képdisztribútor létrehozása</span><span class="sxs-lookup"><span data-stu-id="ee7b9-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="ee7b9-112">A parancs létrehoz egy felügyelt képdisztribútort.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="ee7b9-113">2. példa: virtuális VHD-forgalmazó létrehozása</span><span class="sxs-lookup"><span data-stu-id="ee7b9-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="ee7b9-114">Ez a parancs egy VHD-forgalmazót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="ee7b9-115">3. példa: megosztott kép disztribútor létrehozása</span><span class="sxs-lookup"><span data-stu-id="ee7b9-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="ee7b9-116">A parancs létrehoz egy megosztott képdisztribútort.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="ee7b9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee7b9-117">PARAMETERS</span></span>

### <span data-ttu-id="ee7b9-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="ee7b9-118">-ArtifactTag</span></span>
<span data-ttu-id="ee7b9-119">Azok a címkék, amelyeket a program a forgalmazó által létrehozott/frissített, a tárgyhoz fog alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7b9-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="ee7b9-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="ee7b9-121">Megjelölés, amely azt jelzi, hogy a létrehozott képverziót ki kell-e zárni a legújabb verzióból.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="ee7b9-122">Hagyja kihagyja az alapértelmezett (false) használatát.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-122">Omit to use the default (false).</span></span>

```yaml
Type: System.Boolean
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7b9-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="ee7b9-123">-GalleryImageId</span></span>
<span data-ttu-id="ee7b9-124">A megosztott képgyűjtemény-kép erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-124">Resource Id of the Shared Image Gallery image.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7b9-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="ee7b9-125">-ImageId</span></span>
<span data-ttu-id="ee7b9-126">A felügyelt lemezkép erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-126">Resource Id of the Managed Disk Image.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7b9-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="ee7b9-127">-Location</span></span>
<span data-ttu-id="ee7b9-128">Ha a kép már létezik, az Azure helyének egyeznie kell a képhez.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-128">Azure location for the image, should match if image already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7b9-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="ee7b9-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="ee7b9-130">Terjesztés felügyelt lemezképként</span><span class="sxs-lookup"><span data-stu-id="ee7b9-130">Distribute as a Managed Disk Image.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7b9-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="ee7b9-131">-ReplicationRegion</span></span>
<span data-ttu-id="ee7b9-132">Azoknak a régióknak a listája, amelyeknek a képe replikálódni fog.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-132">A list of regions that the image will be replicated to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7b9-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="ee7b9-133">-RunOutputName</span></span>
<span data-ttu-id="ee7b9-134">A kapcsolódó RunOutput használandó név.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-134">The name to be used for the associated RunOutput.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7b9-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="ee7b9-135">-SharedImageDistributor</span></span>
<span data-ttu-id="ee7b9-136">Megosztott képgyűjteményen keresztüli terjesztés</span><span class="sxs-lookup"><span data-stu-id="ee7b9-136">Distribute via Shared Image Gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7b9-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ee7b9-137">-StorageAccountType</span></span>
<span data-ttu-id="ee7b9-138">A megosztott kép tárolásához használt tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="ee7b9-139">Hagyja ki az alapértelmezett (Standard_LRS) használatát.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-139">Omit to use the default (Standard_LRS).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.SharedImageStorageAccountType
Parameter Sets: SharedImageDistributor
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7b9-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="ee7b9-140">-VhdDistributor</span></span>
<span data-ttu-id="ee7b9-141">Virtuális merevlemezen keresztüli terjesztés a tároló fiókban.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-141">Distribute via VHD in a storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VhdDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7b9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee7b9-142">CommonParameters</span></span>
<span data-ttu-id="ee7b9-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee7b9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee7b9-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ee7b9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee7b9-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee7b9-145">INPUTS</span></span>

## <span data-ttu-id="ee7b9-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee7b9-146">OUTPUTS</span></span>

### <span data-ttu-id="ee7b9-147">Microsoft. Azure. PowerShell. parancsmagok. ImageBuilder. modellek. Api20200214. IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="ee7b9-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="ee7b9-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee7b9-148">NOTES</span></span>

<span data-ttu-id="ee7b9-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ee7b9-149">ALIASES</span></span>

## <span data-ttu-id="ee7b9-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee7b9-150">RELATED LINKS</span></span>

