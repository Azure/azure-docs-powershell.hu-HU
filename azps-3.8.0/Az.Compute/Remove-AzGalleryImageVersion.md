---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: addf292e2a73b27f6e1e40258c0d8c60e54cfaed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847646"
---
# <span data-ttu-id="99de6-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="99de6-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="99de6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99de6-102">SYNOPSIS</span></span>
<span data-ttu-id="99de6-103">Gyűjtemény képének törlése</span><span class="sxs-lookup"><span data-stu-id="99de6-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="99de6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99de6-104">SYNTAX</span></span>

### <span data-ttu-id="99de6-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99de6-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99de6-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="99de6-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99de6-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="99de6-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99de6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="99de6-108">DESCRIPTION</span></span>
<span data-ttu-id="99de6-109">Gyűjtemény képének törlése</span><span class="sxs-lookup"><span data-stu-id="99de6-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="99de6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="99de6-110">EXAMPLES</span></span>

### <span data-ttu-id="99de6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="99de6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="99de6-112">Törölje az adott gyűjtemény képének verzióját.</span><span class="sxs-lookup"><span data-stu-id="99de6-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="99de6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99de6-113">PARAMETERS</span></span>

### <span data-ttu-id="99de6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99de6-114">-AsJob</span></span>
<span data-ttu-id="99de6-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="99de6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99de6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99de6-116">-DefaultProfile</span></span>
<span data-ttu-id="99de6-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99de6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99de6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="99de6-118">-Force</span></span>
<span data-ttu-id="99de6-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="99de6-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99de6-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="99de6-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="99de6-121">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="99de6-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="99de6-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="99de6-122">-GalleryName</span></span>
<span data-ttu-id="99de6-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="99de6-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="99de6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99de6-124">-InputObject</span></span>
<span data-ttu-id="99de6-125">A PS Gallery Image Version objektuma</span><span class="sxs-lookup"><span data-stu-id="99de6-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="99de6-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99de6-126">-Name</span></span>
<span data-ttu-id="99de6-127">A gyűjtemény képének neve.</span><span class="sxs-lookup"><span data-stu-id="99de6-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="99de6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99de6-128">-ResourceGroupName</span></span>
<span data-ttu-id="99de6-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="99de6-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="99de6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99de6-130">-ResourceId</span></span>
<span data-ttu-id="99de6-131">A gyűjtemény erőforrás-azonosítója a Képtár képének verziójában</span><span class="sxs-lookup"><span data-stu-id="99de6-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="99de6-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99de6-132">-Confirm</span></span>
<span data-ttu-id="99de6-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99de6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99de6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99de6-134">-WhatIf</span></span>
<span data-ttu-id="99de6-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99de6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99de6-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99de6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99de6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99de6-137">CommonParameters</span></span>
<span data-ttu-id="99de6-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99de6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99de6-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="99de6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99de6-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99de6-140">INPUTS</span></span>

### <span data-ttu-id="99de6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="99de6-141">System.String</span></span>

### <span data-ttu-id="99de6-142">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="99de6-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="99de6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99de6-143">OUTPUTS</span></span>

### <span data-ttu-id="99de6-144">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="99de6-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="99de6-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99de6-145">NOTES</span></span>

## <span data-ttu-id="99de6-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99de6-146">RELATED LINKS</span></span>
