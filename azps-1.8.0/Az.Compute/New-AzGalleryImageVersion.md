---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 6d5731916309baf93552f9b5d71f30943178f11c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671313"
---
# <span data-ttu-id="63fb8-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="63fb8-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="63fb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="63fb8-103">Gyűjtemény képének létrehozása</span><span class="sxs-lookup"><span data-stu-id="63fb8-103">Create a gallery image version.</span></span>

## <span data-ttu-id="63fb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63fb8-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63fb8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="63fb8-105">DESCRIPTION</span></span>
<span data-ttu-id="63fb8-106">Gyűjtemény képének létrehozása</span><span class="sxs-lookup"><span data-stu-id="63fb8-106">Create a gallery image version.</span></span>

## <span data-ttu-id="63fb8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="63fb8-107">EXAMPLES</span></span>

### <span data-ttu-id="63fb8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="63fb8-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="63fb8-109">Gyűjtemény képének létrehozása</span><span class="sxs-lookup"><span data-stu-id="63fb8-109">Create a gallery image version.</span></span>

## <span data-ttu-id="63fb8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63fb8-110">PARAMETERS</span></span>

### <span data-ttu-id="63fb8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63fb8-111">-AsJob</span></span>
<span data-ttu-id="63fb8-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="63fb8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63fb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fb8-113">-DefaultProfile</span></span>
<span data-ttu-id="63fb8-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63fb8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63fb8-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="63fb8-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="63fb8-116">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="63fb8-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="63fb8-117">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="63fb8-117">-GalleryName</span></span>
<span data-ttu-id="63fb8-118">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="63fb8-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="63fb8-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="63fb8-119">-Location</span></span>
<span data-ttu-id="63fb8-120">Erőforrás-hely</span><span class="sxs-lookup"><span data-stu-id="63fb8-120">Resource location</span></span>

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

### <span data-ttu-id="63fb8-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="63fb8-121">-Name</span></span>
<span data-ttu-id="63fb8-122">A gyűjtemény képének neve.</span><span class="sxs-lookup"><span data-stu-id="63fb8-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="63fb8-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="63fb8-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="63fb8-124">A gyűjtemény képének befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="63fb8-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="63fb8-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="63fb8-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="63fb8-126">Ha be van állítva, akkor a kép definíciójának legújabb verziójáról telepített virtuális gépek nem fogják használni ezt a képváltozatot.</span><span class="sxs-lookup"><span data-stu-id="63fb8-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="63fb8-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="63fb8-127">-ReplicaCount</span></span>
<span data-ttu-id="63fb8-128">Az régiónként létrehozandó képverzió replikáinak száma.</span><span class="sxs-lookup"><span data-stu-id="63fb8-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="63fb8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63fb8-129">-ResourceGroupName</span></span>
<span data-ttu-id="63fb8-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="63fb8-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="63fb8-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="63fb8-131">-SourceImageId</span></span>
<span data-ttu-id="63fb8-132">Annak a forrásnak az azonosítója, amelyből a kép verziója lesz létrehozva.</span><span class="sxs-lookup"><span data-stu-id="63fb8-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="63fb8-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="63fb8-133">-Tag</span></span>
<span data-ttu-id="63fb8-134">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="63fb8-134">Resource tags</span></span>

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

### <span data-ttu-id="63fb8-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="63fb8-135">-TargetRegion</span></span>
<span data-ttu-id="63fb8-136">Azok a célterületek, amelyekben a képváltozatot replikálni fogja.</span><span class="sxs-lookup"><span data-stu-id="63fb8-136">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="63fb8-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="63fb8-137">-Confirm</span></span>
<span data-ttu-id="63fb8-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="63fb8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63fb8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63fb8-139">-WhatIf</span></span>
<span data-ttu-id="63fb8-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="63fb8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63fb8-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63fb8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63fb8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fb8-142">CommonParameters</span></span>
<span data-ttu-id="63fb8-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63fb8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fb8-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63fb8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fb8-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63fb8-145">INPUTS</span></span>

### <span data-ttu-id="63fb8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="63fb8-146">System.String</span></span>

### <span data-ttu-id="63fb8-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="63fb8-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="63fb8-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="63fb8-148">System.Int32</span></span>

### <span data-ttu-id="63fb8-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="63fb8-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="63fb8-150">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="63fb8-150">System.DateTime</span></span>

### <span data-ttu-id="63fb8-151">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="63fb8-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="63fb8-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63fb8-152">OUTPUTS</span></span>

### <span data-ttu-id="63fb8-153">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="63fb8-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="63fb8-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63fb8-154">NOTES</span></span>

## <span data-ttu-id="63fb8-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63fb8-155">RELATED LINKS</span></span>
