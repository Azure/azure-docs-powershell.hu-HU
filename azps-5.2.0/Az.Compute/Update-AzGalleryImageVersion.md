---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339725"
---
# <span data-ttu-id="a2975-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a2975-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="a2975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2975-102">SYNOPSIS</span></span>
<span data-ttu-id="a2975-103">Gyűjtemény képverzióját frissítheti.</span><span class="sxs-lookup"><span data-stu-id="a2975-103">Update a gallery image version.</span></span>

## <span data-ttu-id="a2975-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2975-104">SYNTAX</span></span>

### <span data-ttu-id="a2975-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2975-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2975-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a2975-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2975-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a2975-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2975-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2975-108">DESCRIPTION</span></span>
<span data-ttu-id="a2975-109">Gyűjtemény képverzióját frissítheti.</span><span class="sxs-lookup"><span data-stu-id="a2975-109">Update a gallery image version.</span></span>

## <span data-ttu-id="a2975-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2975-110">EXAMPLES</span></span>

### <span data-ttu-id="a2975-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a2975-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="a2975-112">Gyűjtemény képverzióját frissítheti.</span><span class="sxs-lookup"><span data-stu-id="a2975-112">Update a gallery image version.</span></span>

## <span data-ttu-id="a2975-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2975-113">PARAMETERS</span></span>

### <span data-ttu-id="a2975-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2975-114">-AsJob</span></span>
<span data-ttu-id="a2975-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a2975-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2975-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2975-116">-DefaultProfile</span></span>
<span data-ttu-id="a2975-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2975-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2975-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a2975-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="a2975-119">A gyűjtemény képdefiníciójának neve.</span><span class="sxs-lookup"><span data-stu-id="a2975-119">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2975-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="a2975-120">-GalleryName</span></span>
<span data-ttu-id="a2975-121">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="a2975-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2975-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2975-122">-InputObject</span></span>
<span data-ttu-id="a2975-123">A PS-gyűjtemény képverzióobjektuma.</span><span class="sxs-lookup"><span data-stu-id="a2975-123">The PS Gallery Image Version Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2975-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a2975-124">-Name</span></span>
<span data-ttu-id="a2975-125">A galériakép verziószámának neve.</span><span class="sxs-lookup"><span data-stu-id="a2975-125">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2975-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="a2975-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="a2975-127">A galéria Képverzió életciklusának vége.</span><span class="sxs-lookup"><span data-stu-id="a2975-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="a2975-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="a2975-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="a2975-129">Ha be van állítva, a Képdefiníció legújabb verziójából telepített virtuális gépek nem fogják használni ezt a képverziót.</span><span class="sxs-lookup"><span data-stu-id="a2975-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="a2975-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="a2975-130">-ReplicaCount</span></span>
<span data-ttu-id="a2975-131">A képverzió régiónként létrehozható másolatainak száma.</span><span class="sxs-lookup"><span data-stu-id="a2975-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="a2975-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2975-132">-ResourceGroupName</span></span>
<span data-ttu-id="a2975-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2975-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2975-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2975-134">-ResourceId</span></span>
<span data-ttu-id="a2975-135">A gyűjtemény képverziójának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a2975-135">The resource ID for the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2975-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="a2975-136">-Tag</span></span>
<span data-ttu-id="a2975-137">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="a2975-137">Resource tags</span></span>

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

### <span data-ttu-id="a2975-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="a2975-138">-TargetRegion</span></span>
<span data-ttu-id="a2975-139">A célterület, ahová a képverzió replikálva lesz.</span><span class="sxs-lookup"><span data-stu-id="a2975-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="a2975-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2975-140">-Confirm</span></span>
<span data-ttu-id="a2975-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a2975-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2975-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2975-142">-WhatIf</span></span>
<span data-ttu-id="a2975-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a2975-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2975-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2975-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2975-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2975-145">CommonParameters</span></span>
<span data-ttu-id="a2975-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2975-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2975-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2975-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2975-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2975-148">INPUTS</span></span>

### <span data-ttu-id="a2975-149">System.String</span><span class="sxs-lookup"><span data-stu-id="a2975-149">System.String</span></span>

### <span data-ttu-id="a2975-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a2975-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="a2975-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a2975-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a2975-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a2975-152">System.Int32</span></span>

### <span data-ttu-id="a2975-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a2975-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a2975-154">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="a2975-154">System.DateTime</span></span>

### <span data-ttu-id="a2975-155">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="a2975-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="a2975-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2975-156">OUTPUTS</span></span>

### <span data-ttu-id="a2975-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="a2975-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="a2975-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2975-158">NOTES</span></span>

## <span data-ttu-id="a2975-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2975-159">RELATED LINKS</span></span>
