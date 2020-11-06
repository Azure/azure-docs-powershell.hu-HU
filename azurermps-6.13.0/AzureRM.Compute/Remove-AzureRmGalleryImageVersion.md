---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
ms.openlocfilehash: c2a65eeb742d4182dfad0cd32be1d78951977096
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494113"
---
# <span data-ttu-id="1e9a8-101">Remove-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="1e9a8-101">Remove-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="1e9a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e9a8-102">SYNOPSIS</span></span>
<span data-ttu-id="1e9a8-103">Gyűjtemény képének törlése</span><span class="sxs-lookup"><span data-stu-id="1e9a8-103">Delete a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e9a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e9a8-104">SYNTAX</span></span>

### <span data-ttu-id="1e9a8-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e9a8-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e9a8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1e9a8-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e9a8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1e9a8-107">ObjectParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e9a8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e9a8-108">DESCRIPTION</span></span>
<span data-ttu-id="1e9a8-109">Gyűjtemény képének törlése</span><span class="sxs-lookup"><span data-stu-id="1e9a8-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="1e9a8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1e9a8-110">EXAMPLES</span></span>

### <span data-ttu-id="1e9a8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1e9a8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="1e9a8-112">Törölje az adott gyűjtemény képének verzióját.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="1e9a8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e9a8-113">PARAMETERS</span></span>

### <span data-ttu-id="1e9a8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e9a8-114">-AsJob</span></span>
<span data-ttu-id="1e9a8-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1e9a8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e9a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e9a8-116">-DefaultProfile</span></span>
<span data-ttu-id="1e9a8-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e9a8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1e9a8-118">-Force</span></span>
<span data-ttu-id="1e9a8-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1e9a8-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="1e9a8-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="1e9a8-121">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="1e9a8-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="1e9a8-122">-GalleryName</span></span>
<span data-ttu-id="1e9a8-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="1e9a8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e9a8-124">-InputObject</span></span>
<span data-ttu-id="1e9a8-125">A PS Gallery Image Version objektuma</span><span class="sxs-lookup"><span data-stu-id="1e9a8-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="1e9a8-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e9a8-126">-Name</span></span>
<span data-ttu-id="1e9a8-127">A gyűjtemény képének neve.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="1e9a8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e9a8-128">-ResourceGroupName</span></span>
<span data-ttu-id="1e9a8-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="1e9a8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e9a8-130">-ResourceId</span></span>
<span data-ttu-id="1e9a8-131">A gyűjtemény erőforrás-azonosítója a Képtár képének verziójában</span><span class="sxs-lookup"><span data-stu-id="1e9a8-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="1e9a8-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e9a8-132">-Confirm</span></span>
<span data-ttu-id="1e9a8-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e9a8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e9a8-134">-WhatIf</span></span>
<span data-ttu-id="1e9a8-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e9a8-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e9a8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e9a8-137">CommonParameters</span></span>
<span data-ttu-id="1e9a8-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e9a8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e9a8-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e9a8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e9a8-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e9a8-140">INPUTS</span></span>

### <span data-ttu-id="1e9a8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1e9a8-141">System.String</span></span>

### <span data-ttu-id="1e9a8-142">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="1e9a8-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="1e9a8-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e9a8-143">OUTPUTS</span></span>

### <span data-ttu-id="1e9a8-144">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="1e9a8-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1e9a8-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e9a8-145">NOTES</span></span>

## <span data-ttu-id="1e9a8-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e9a8-146">RELATED LINKS</span></span>
