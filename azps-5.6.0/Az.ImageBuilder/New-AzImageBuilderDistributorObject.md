---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 3421eec7fa723767db0dc896d0c3c40e7c5cbebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013046"
---
# <span data-ttu-id="f6c5c-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="f6c5c-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="f6c5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c5c-103">Generic distribution object</span><span class="sxs-lookup"><span data-stu-id="f6c5c-103">Generic distribution object</span></span>

## <span data-ttu-id="f6c5c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f6c5c-104">SYNTAX</span></span>

### <span data-ttu-id="f6c5c-105">ManagedImageDistributor (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6c5c-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="f6c5c-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="f6c5c-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="f6c5c-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="f6c5c-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="f6c5c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f6c5c-108">DESCRIPTION</span></span>
<span data-ttu-id="f6c5c-109">Generic distribution object</span><span class="sxs-lookup"><span data-stu-id="f6c5c-109">Generic distribution object</span></span>

## <span data-ttu-id="f6c5c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f6c5c-110">EXAMPLES</span></span>

### <span data-ttu-id="f6c5c-111">1. példa: Felügyelt kép terjesztő létrehozása</span><span class="sxs-lookup"><span data-stu-id="f6c5c-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="f6c5c-112">Ez a parancs egy felügyelt kép terjesztőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="f6c5c-113">2. példa: VHD terjesztő létrehozása</span><span class="sxs-lookup"><span data-stu-id="f6c5c-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="f6c5c-114">Ez a parancs egy VHD terjesztőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="f6c5c-115">3. példa: Megosztott kép terjesztő létrehozása</span><span class="sxs-lookup"><span data-stu-id="f6c5c-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="f6c5c-116">Ez a parancs megosztott kép terjesztőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="f6c5c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6c5c-117">PARAMETERS</span></span>

### <span data-ttu-id="f6c5c-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="f6c5c-118">-ArtifactTag</span></span>
<span data-ttu-id="f6c5c-119">Címkék, amelyek a terjesztő által létrehozott/frissített összetevőre lesznek alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

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

### <span data-ttu-id="f6c5c-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="f6c5c-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="f6c5c-121">Flag that indicates that created image version should be excluded from latest.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="f6c5c-122">Kihagyja az alapértelmezett (hamis) beállítást.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-122">Omit to use the default (false).</span></span>

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

### <span data-ttu-id="f6c5c-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="f6c5c-123">-GalleryImageId</span></span>
<span data-ttu-id="f6c5c-124">A Megosztott képgyűjtemény képének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-124">Resource Id of the Shared Image Gallery image.</span></span>

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

### <span data-ttu-id="f6c5c-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="f6c5c-125">-ImageId</span></span>
<span data-ttu-id="f6c5c-126">A Felügyelt lemez lemezképének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-126">Resource Id of the Managed Disk Image.</span></span>

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

### <span data-ttu-id="f6c5c-127">-Location</span><span class="sxs-lookup"><span data-stu-id="f6c5c-127">-Location</span></span>
<span data-ttu-id="f6c5c-128">A kép Azure-beli helyének egyeznie kell, ha a kép már létezik.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-128">Azure location for the image, should match if image already exists.</span></span>

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

### <span data-ttu-id="f6c5c-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="f6c5c-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="f6c5c-130">Distribute as a Managed Disk Image.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-130">Distribute as a Managed Disk Image.</span></span>

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

### <span data-ttu-id="f6c5c-131">-ReplikációsRégió</span><span class="sxs-lookup"><span data-stu-id="f6c5c-131">-ReplicationRegion</span></span>
<span data-ttu-id="f6c5c-132">Azon régiók listája, amelyekbe a képet replikálni fogja.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-132">A list of regions that the image will be replicated to.</span></span>

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

### <span data-ttu-id="f6c5c-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="f6c5c-133">-RunOutputName</span></span>
<span data-ttu-id="f6c5c-134">A társított RunOutput-hoz használt név.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-134">The name to be used for the associated RunOutput.</span></span>

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

### <span data-ttu-id="f6c5c-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="f6c5c-135">-SharedImageDistributor</span></span>
<span data-ttu-id="f6c5c-136">Terjesztheti a megosztott képgyűjteményen keresztül.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-136">Distribute via Shared Image Gallery.</span></span>

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

### <span data-ttu-id="f6c5c-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f6c5c-137">-StorageAccountType</span></span>
<span data-ttu-id="f6c5c-138">A megosztott kép tárolásához használt tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="f6c5c-139">Kihagyja az alapértelmezett (Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="f6c5c-139">Omit to use the default (Standard_LRS).</span></span>

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

### <span data-ttu-id="f6c5c-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="f6c5c-140">-VhdDistributor</span></span>
<span data-ttu-id="f6c5c-141">Terjesztés VHD-n keresztül egy tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-141">Distribute via VHD in a storage account.</span></span>

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

### <span data-ttu-id="f6c5c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c5c-142">CommonParameters</span></span>
<span data-ttu-id="f6c5c-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6c5c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c5c-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6c5c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c5c-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6c5c-145">INPUTS</span></span>

## <span data-ttu-id="f6c5c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6c5c-146">OUTPUTS</span></span>

### <span data-ttu-id="f6c5c-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="f6c5c-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="f6c5c-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f6c5c-148">NOTES</span></span>

<span data-ttu-id="f6c5c-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f6c5c-149">ALIASES</span></span>

## <span data-ttu-id="f6c5c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6c5c-150">RELATED LINKS</span></span>

