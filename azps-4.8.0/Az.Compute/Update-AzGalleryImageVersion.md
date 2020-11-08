---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183068"
---
# <span data-ttu-id="c751d-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="c751d-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="c751d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c751d-102">SYNOPSIS</span></span>
<span data-ttu-id="c751d-103">Gyűjtemény képének frissítése</span><span class="sxs-lookup"><span data-stu-id="c751d-103">Update a gallery image version.</span></span>

## <span data-ttu-id="c751d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c751d-104">SYNTAX</span></span>

### <span data-ttu-id="c751d-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c751d-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c751d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c751d-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c751d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="c751d-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c751d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c751d-108">DESCRIPTION</span></span>
<span data-ttu-id="c751d-109">Gyűjtemény képének frissítése</span><span class="sxs-lookup"><span data-stu-id="c751d-109">Update a gallery image version.</span></span>

## <span data-ttu-id="c751d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c751d-110">EXAMPLES</span></span>

### <span data-ttu-id="c751d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c751d-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="c751d-112">Gyűjtemény képének frissítése</span><span class="sxs-lookup"><span data-stu-id="c751d-112">Update a gallery image version.</span></span>

## <span data-ttu-id="c751d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c751d-113">PARAMETERS</span></span>

### <span data-ttu-id="c751d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c751d-114">-AsJob</span></span>
<span data-ttu-id="c751d-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c751d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c751d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c751d-116">-DefaultProfile</span></span>
<span data-ttu-id="c751d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c751d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c751d-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="c751d-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="c751d-119">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="c751d-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="c751d-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="c751d-120">-GalleryName</span></span>
<span data-ttu-id="c751d-121">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="c751d-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="c751d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c751d-122">-InputObject</span></span>
<span data-ttu-id="c751d-123">A PS-gyűjtemény képverzió objektuma.</span><span class="sxs-lookup"><span data-stu-id="c751d-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="c751d-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c751d-124">-Name</span></span>
<span data-ttu-id="c751d-125">A gyűjtemény képének neve.</span><span class="sxs-lookup"><span data-stu-id="c751d-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="c751d-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="c751d-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="c751d-127">A gyűjtemény képének befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="c751d-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="c751d-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="c751d-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="c751d-129">Ha be van állítva, akkor a kép definíciójának legújabb verziójáról telepített virtuális gépek nem fogják használni ezt a képváltozatot.</span><span class="sxs-lookup"><span data-stu-id="c751d-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="c751d-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="c751d-130">-ReplicaCount</span></span>
<span data-ttu-id="c751d-131">Az régiónként létrehozandó képverzió replikáinak száma.</span><span class="sxs-lookup"><span data-stu-id="c751d-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="c751d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c751d-132">-ResourceGroupName</span></span>
<span data-ttu-id="c751d-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c751d-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="c751d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c751d-134">-ResourceId</span></span>
<span data-ttu-id="c751d-135">A gyűjtemény képének-verziójának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c751d-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="c751d-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="c751d-136">-Tag</span></span>
<span data-ttu-id="c751d-137">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="c751d-137">Resource tags</span></span>

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

### <span data-ttu-id="c751d-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="c751d-138">-TargetRegion</span></span>
<span data-ttu-id="c751d-139">Azok a célterületek, amelyekben a képváltozatot replikálni fogja.</span><span class="sxs-lookup"><span data-stu-id="c751d-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="c751d-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c751d-140">-Confirm</span></span>
<span data-ttu-id="c751d-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c751d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c751d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c751d-142">-WhatIf</span></span>
<span data-ttu-id="c751d-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c751d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c751d-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c751d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c751d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c751d-145">CommonParameters</span></span>
<span data-ttu-id="c751d-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c751d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c751d-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c751d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c751d-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c751d-148">INPUTS</span></span>

### <span data-ttu-id="c751d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c751d-149">System.String</span></span>

### <span data-ttu-id="c751d-150">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="c751d-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="c751d-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c751d-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c751d-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c751d-152">System.Int32</span></span>

### <span data-ttu-id="c751d-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c751d-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c751d-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="c751d-154">System.DateTime</span></span>

### <span data-ttu-id="c751d-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="c751d-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="c751d-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c751d-156">OUTPUTS</span></span>

### <span data-ttu-id="c751d-157">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="c751d-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="c751d-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c751d-158">NOTES</span></span>

## <span data-ttu-id="c751d-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c751d-159">RELATED LINKS</span></span>
