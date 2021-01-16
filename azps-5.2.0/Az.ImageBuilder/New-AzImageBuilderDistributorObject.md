---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348881"
---
# <span data-ttu-id="84776-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="84776-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="84776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84776-102">SYNOPSIS</span></span>
<span data-ttu-id="84776-103">Generic distribution object</span><span class="sxs-lookup"><span data-stu-id="84776-103">Generic distribution object</span></span>

## <span data-ttu-id="84776-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="84776-104">SYNTAX</span></span>

### <span data-ttu-id="84776-105">ManagedImageDistributor (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84776-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="84776-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="84776-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="84776-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="84776-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="84776-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="84776-108">DESCRIPTION</span></span>
<span data-ttu-id="84776-109">Generic distribution object</span><span class="sxs-lookup"><span data-stu-id="84776-109">Generic distribution object</span></span>

## <span data-ttu-id="84776-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="84776-110">EXAMPLES</span></span>

### <span data-ttu-id="84776-111">1. példa: Felügyelt kép terjesztő létrehozása</span><span class="sxs-lookup"><span data-stu-id="84776-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="84776-112">Ez a parancs egy felügyelt kép terjesztőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="84776-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="84776-113">2. példa: VHD terjesztő létrehozása</span><span class="sxs-lookup"><span data-stu-id="84776-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="84776-114">Ez a parancs egy VHD terjesztőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="84776-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="84776-115">3. példa: Megosztott kép terjesztő létrehozása</span><span class="sxs-lookup"><span data-stu-id="84776-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="84776-116">Ez a parancs megosztott kép terjesztőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="84776-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="84776-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84776-117">PARAMETERS</span></span>

### <span data-ttu-id="84776-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="84776-118">-ArtifactTag</span></span>
<span data-ttu-id="84776-119">Címkék, amelyek a terjesztő által létrehozott/frissített összetevőre lesznek alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="84776-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

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

### <span data-ttu-id="84776-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="84776-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="84776-121">Flag that indicates that created image version should be excluded from latest.</span><span class="sxs-lookup"><span data-stu-id="84776-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="84776-122">Kihagyja az alapértelmezett (hamis) beállítást.</span><span class="sxs-lookup"><span data-stu-id="84776-122">Omit to use the default (false).</span></span>

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

### <span data-ttu-id="84776-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="84776-123">-GalleryImageId</span></span>
<span data-ttu-id="84776-124">A Megosztott képgyűjtemény képének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="84776-124">Resource Id of the Shared Image Gallery image.</span></span>

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

### <span data-ttu-id="84776-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="84776-125">-ImageId</span></span>
<span data-ttu-id="84776-126">A Felügyelt lemez lemezképének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="84776-126">Resource Id of the Managed Disk Image.</span></span>

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

### <span data-ttu-id="84776-127">-Location</span><span class="sxs-lookup"><span data-stu-id="84776-127">-Location</span></span>
<span data-ttu-id="84776-128">A kép Azure-beli helyének egyeznie kell, ha a kép már létezik.</span><span class="sxs-lookup"><span data-stu-id="84776-128">Azure location for the image, should match if image already exists.</span></span>

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

### <span data-ttu-id="84776-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="84776-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="84776-130">Distribute as a Managed Disk Image.</span><span class="sxs-lookup"><span data-stu-id="84776-130">Distribute as a Managed Disk Image.</span></span>

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

### <span data-ttu-id="84776-131">-ReplikációsRégió</span><span class="sxs-lookup"><span data-stu-id="84776-131">-ReplicationRegion</span></span>
<span data-ttu-id="84776-132">Azon régiók listája, amelyekbe a képet replikálni fogja.</span><span class="sxs-lookup"><span data-stu-id="84776-132">A list of regions that the image will be replicated to.</span></span>

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

### <span data-ttu-id="84776-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="84776-133">-RunOutputName</span></span>
<span data-ttu-id="84776-134">A társított RunOutput-hoz használt név.</span><span class="sxs-lookup"><span data-stu-id="84776-134">The name to be used for the associated RunOutput.</span></span>

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

### <span data-ttu-id="84776-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="84776-135">-SharedImageDistributor</span></span>
<span data-ttu-id="84776-136">Terjesztheti a megosztott képgyűjteményen keresztül.</span><span class="sxs-lookup"><span data-stu-id="84776-136">Distribute via Shared Image Gallery.</span></span>

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

### <span data-ttu-id="84776-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="84776-137">-StorageAccountType</span></span>
<span data-ttu-id="84776-138">A megosztott kép tárolásához használt tárfiók típusa.</span><span class="sxs-lookup"><span data-stu-id="84776-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="84776-139">Kihagyja az alapértelmezett (Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="84776-139">Omit to use the default (Standard_LRS).</span></span>

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

### <span data-ttu-id="84776-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="84776-140">-VhdDistributor</span></span>
<span data-ttu-id="84776-141">Terjesztés VHD-n keresztül egy tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="84776-141">Distribute via VHD in a storage account.</span></span>

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

### <span data-ttu-id="84776-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84776-142">CommonParameters</span></span>
<span data-ttu-id="84776-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84776-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84776-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84776-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84776-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84776-145">INPUTS</span></span>

## <span data-ttu-id="84776-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84776-146">OUTPUTS</span></span>

### <span data-ttu-id="84776-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="84776-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="84776-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="84776-148">NOTES</span></span>

<span data-ttu-id="84776-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="84776-149">ALIASES</span></span>

## <span data-ttu-id="84776-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84776-150">RELATED LINKS</span></span>

