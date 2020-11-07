---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageVersion.md
ms.openlocfilehash: e8c50ffb2ac60c65f64806781d9155600c9bbe0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672988"
---
# <span data-ttu-id="b09aa-101">Update-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b09aa-101">Update-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="b09aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b09aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b09aa-103">Gyűjtemény képének frissítése</span><span class="sxs-lookup"><span data-stu-id="b09aa-103">Update a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b09aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b09aa-104">SYNTAX</span></span>

### <span data-ttu-id="b09aa-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b09aa-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-Tag <Hashtable>] [-ReplicaCount <Int32>]
 [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b09aa-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b09aa-106">ResourceIdParameter</span></span>
```
Update-AzureRmGalleryImageVersion [-ResourceId] <String> [-AsJob] [-Tag <Hashtable>] [-ReplicaCount <Int32>]
 [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b09aa-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b09aa-107">ObjectParameter</span></span>
```
Update-AzureRmGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob] [-Tag <Hashtable>]
 [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b09aa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b09aa-108">DESCRIPTION</span></span>
<span data-ttu-id="b09aa-109">Gyűjtemény képének frissítése</span><span class="sxs-lookup"><span data-stu-id="b09aa-109">Update a gallery image version.</span></span>

## <span data-ttu-id="b09aa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b09aa-110">EXAMPLES</span></span>

### <span data-ttu-id="b09aa-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b09aa-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="b09aa-112">Gyűjtemény képének frissítése</span><span class="sxs-lookup"><span data-stu-id="b09aa-112">Update a gallery image version.</span></span>

## <span data-ttu-id="b09aa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b09aa-113">PARAMETERS</span></span>

### <span data-ttu-id="b09aa-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b09aa-114">-AsJob</span></span>
<span data-ttu-id="b09aa-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b09aa-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b09aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b09aa-116">-DefaultProfile</span></span>
<span data-ttu-id="b09aa-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b09aa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b09aa-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b09aa-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="b09aa-119">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="b09aa-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="b09aa-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="b09aa-120">-GalleryName</span></span>
<span data-ttu-id="b09aa-121">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="b09aa-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="b09aa-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b09aa-122">-InputObject</span></span>
<span data-ttu-id="b09aa-123">A PS-gyűjtemény képverzió objektuma.</span><span class="sxs-lookup"><span data-stu-id="b09aa-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="b09aa-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b09aa-124">-Name</span></span>
<span data-ttu-id="b09aa-125">A gyűjtemény képének neve.</span><span class="sxs-lookup"><span data-stu-id="b09aa-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="b09aa-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="b09aa-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="b09aa-127">A gyűjtemény képének befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="b09aa-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="b09aa-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="b09aa-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="b09aa-129">Ha be van állítva, akkor a kép definíciójának legújabb verziójáról telepített virtuális gépek nem fogják használni ezt a képváltozatot.</span><span class="sxs-lookup"><span data-stu-id="b09aa-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="b09aa-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="b09aa-130">-ReplicaCount</span></span>
<span data-ttu-id="b09aa-131">Az régiónként létrehozandó képverzió replikáinak száma.</span><span class="sxs-lookup"><span data-stu-id="b09aa-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="b09aa-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b09aa-132">-ResourceGroupName</span></span>
<span data-ttu-id="b09aa-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b09aa-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="b09aa-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b09aa-134">-ResourceId</span></span>
<span data-ttu-id="b09aa-135">A gyűjtemény képének-verziójának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b09aa-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="b09aa-136">-Címke</span><span class="sxs-lookup"><span data-stu-id="b09aa-136">-Tag</span></span>
<span data-ttu-id="b09aa-137">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="b09aa-137">Resource tags</span></span>

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

### <span data-ttu-id="b09aa-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="b09aa-138">-TargetRegion</span></span>
<span data-ttu-id="b09aa-139">Azok a célterületek, amelyekben a képváltozatot replikálni fogja.</span><span class="sxs-lookup"><span data-stu-id="b09aa-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="b09aa-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b09aa-140">-Confirm</span></span>
<span data-ttu-id="b09aa-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b09aa-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b09aa-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b09aa-142">-WhatIf</span></span>
<span data-ttu-id="b09aa-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b09aa-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b09aa-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b09aa-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b09aa-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b09aa-145">CommonParameters</span></span>
<span data-ttu-id="b09aa-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b09aa-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b09aa-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b09aa-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b09aa-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b09aa-148">INPUTS</span></span>

### <span data-ttu-id="b09aa-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b09aa-149">System.String</span></span>

### <span data-ttu-id="b09aa-150">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b09aa-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="b09aa-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b09aa-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b09aa-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b09aa-152">System.Int32</span></span>

### <span data-ttu-id="b09aa-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b09aa-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b09aa-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="b09aa-154">System.DateTime</span></span>

### <span data-ttu-id="b09aa-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="b09aa-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="b09aa-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b09aa-156">OUTPUTS</span></span>

### <span data-ttu-id="b09aa-157">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="b09aa-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="b09aa-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b09aa-158">NOTES</span></span>

## <span data-ttu-id="b09aa-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b09aa-159">RELATED LINKS</span></span>
