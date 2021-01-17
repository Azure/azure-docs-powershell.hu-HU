---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 4c4809ed022595af7c0ad977d082c6a52616e920
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480789"
---
# <span data-ttu-id="7c7a1-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7c7a1-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="7c7a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c7a1-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7a1-103">Gyűjtemény képverzióját törölheti.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="7c7a1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c7a1-104">SYNTAX</span></span>

### <span data-ttu-id="7c7a1-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c7a1-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c7a1-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="7c7a1-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c7a1-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="7c7a1-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c7a1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c7a1-108">DESCRIPTION</span></span>
<span data-ttu-id="7c7a1-109">Gyűjtemény képverzióját törölheti.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="7c7a1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c7a1-110">EXAMPLES</span></span>

### <span data-ttu-id="7c7a1-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7c7a1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="7c7a1-112">Törölje a gyűjtemény adott képverzióját.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="7c7a1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c7a1-113">PARAMETERS</span></span>

### <span data-ttu-id="7c7a1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c7a1-114">-AsJob</span></span>
<span data-ttu-id="7c7a1-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7c7a1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c7a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c7a1-116">-DefaultProfile</span></span>
<span data-ttu-id="7c7a1-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c7a1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7c7a1-118">-Force</span></span>
<span data-ttu-id="7c7a1-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c7a1-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7c7a1-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="7c7a1-121">A gyűjtemény képdefiníciójának neve.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="7c7a1-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="7c7a1-122">-GalleryName</span></span>
<span data-ttu-id="7c7a1-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="7c7a1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c7a1-124">-InputObject</span></span>
<span data-ttu-id="7c7a1-125">A PS-gyűjtemény Kép verzióobjektuma</span><span class="sxs-lookup"><span data-stu-id="7c7a1-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="7c7a1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7c7a1-126">-Name</span></span>
<span data-ttu-id="7c7a1-127">A galériakép verziószámának neve.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="7c7a1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c7a1-128">-ResourceGroupName</span></span>
<span data-ttu-id="7c7a1-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="7c7a1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c7a1-130">-ResourceId</span></span>
<span data-ttu-id="7c7a1-131">The resource ID for gallery image version</span><span class="sxs-lookup"><span data-stu-id="7c7a1-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="7c7a1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c7a1-132">-Confirm</span></span>
<span data-ttu-id="7c7a1-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c7a1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c7a1-134">-WhatIf</span></span>
<span data-ttu-id="7c7a1-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c7a1-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c7a1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7a1-137">CommonParameters</span></span>
<span data-ttu-id="7c7a1-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c7a1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7a1-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c7a1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7a1-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c7a1-140">INPUTS</span></span>

### <span data-ttu-id="7c7a1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7c7a1-141">System.String</span></span>

### <span data-ttu-id="7c7a1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7c7a1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="7c7a1-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c7a1-143">OUTPUTS</span></span>

### <span data-ttu-id="7c7a1-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7c7a1-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7c7a1-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c7a1-145">NOTES</span></span>

## <span data-ttu-id="7c7a1-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c7a1-146">RELATED LINKS</span></span>
