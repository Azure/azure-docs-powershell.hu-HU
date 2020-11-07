---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
ms.openlocfilehash: f27c861386e7a570fe72a5266362bee7fed39e5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680396"
---
# <span data-ttu-id="926c2-101">New-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="926c2-101">New-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="926c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="926c2-102">SYNOPSIS</span></span>
<span data-ttu-id="926c2-103">Gyűjtemény képének létrehozása</span><span class="sxs-lookup"><span data-stu-id="926c2-103">Create a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="926c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="926c2-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="926c2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="926c2-105">DESCRIPTION</span></span>
<span data-ttu-id="926c2-106">Gyűjtemény képének létrehozása</span><span class="sxs-lookup"><span data-stu-id="926c2-106">Create a gallery image version.</span></span>

## <span data-ttu-id="926c2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="926c2-107">EXAMPLES</span></span>

### <span data-ttu-id="926c2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="926c2-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="926c2-109">Gyűjtemény képének létrehozása</span><span class="sxs-lookup"><span data-stu-id="926c2-109">Create a gallery image version.</span></span>

## <span data-ttu-id="926c2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="926c2-110">PARAMETERS</span></span>

### <span data-ttu-id="926c2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="926c2-111">-AsJob</span></span>
<span data-ttu-id="926c2-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="926c2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="926c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926c2-113">-DefaultProfile</span></span>
<span data-ttu-id="926c2-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="926c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="926c2-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="926c2-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="926c2-116">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="926c2-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="926c2-117">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="926c2-117">-GalleryName</span></span>
<span data-ttu-id="926c2-118">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="926c2-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="926c2-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="926c2-119">-Location</span></span>
<span data-ttu-id="926c2-120">Erőforrás-hely</span><span class="sxs-lookup"><span data-stu-id="926c2-120">Resource location</span></span>

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

### <span data-ttu-id="926c2-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="926c2-121">-Name</span></span>
<span data-ttu-id="926c2-122">A gyűjtemény képének neve.</span><span class="sxs-lookup"><span data-stu-id="926c2-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="926c2-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="926c2-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="926c2-124">A gyűjtemény képének befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="926c2-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="926c2-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="926c2-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="926c2-126">Ha be van állítva, akkor a kép definíciójának legújabb verziójáról telepített virtuális gépek nem fogják használni ezt a képváltozatot.</span><span class="sxs-lookup"><span data-stu-id="926c2-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="926c2-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="926c2-127">-ReplicaCount</span></span>
<span data-ttu-id="926c2-128">Az régiónként létrehozandó képverzió replikáinak száma.</span><span class="sxs-lookup"><span data-stu-id="926c2-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="926c2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="926c2-129">-ResourceGroupName</span></span>
<span data-ttu-id="926c2-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="926c2-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="926c2-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="926c2-131">-SourceImageId</span></span>
<span data-ttu-id="926c2-132">Annak a forrásnak az azonosítója, amelyből a kép verziója lesz létrehozva.</span><span class="sxs-lookup"><span data-stu-id="926c2-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="926c2-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="926c2-133">-Tag</span></span>
<span data-ttu-id="926c2-134">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="926c2-134">Resource tags</span></span>

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

### <span data-ttu-id="926c2-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="926c2-135">-TargetRegion</span></span>
<span data-ttu-id="926c2-136">Azok a célterületek, amelyekben a képváltozatot replikálni fogja.</span><span class="sxs-lookup"><span data-stu-id="926c2-136">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="926c2-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="926c2-137">-Confirm</span></span>
<span data-ttu-id="926c2-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="926c2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="926c2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="926c2-139">-WhatIf</span></span>
<span data-ttu-id="926c2-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="926c2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="926c2-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="926c2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="926c2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926c2-142">CommonParameters</span></span>
<span data-ttu-id="926c2-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="926c2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926c2-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="926c2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926c2-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="926c2-145">INPUTS</span></span>

### <span data-ttu-id="926c2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="926c2-146">System.String</span></span>

### <span data-ttu-id="926c2-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="926c2-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="926c2-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="926c2-148">System.Int32</span></span>

### <span data-ttu-id="926c2-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="926c2-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="926c2-150">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="926c2-150">System.DateTime</span></span>

### <span data-ttu-id="926c2-151">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="926c2-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="926c2-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="926c2-152">OUTPUTS</span></span>

### <span data-ttu-id="926c2-153">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="926c2-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="926c2-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="926c2-154">NOTES</span></span>

## <span data-ttu-id="926c2-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="926c2-155">RELATED LINKS</span></span>
