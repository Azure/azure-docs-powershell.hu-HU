---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 4c4809ed022595af7c0ad977d082c6a52616e920
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362346"
---
# <span data-ttu-id="2cfee-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2cfee-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="2cfee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cfee-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfee-103">Gyűjtemény képverzióját törölheti.</span><span class="sxs-lookup"><span data-stu-id="2cfee-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="2cfee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2cfee-104">SYNTAX</span></span>

### <span data-ttu-id="2cfee-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2cfee-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cfee-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2cfee-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cfee-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2cfee-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cfee-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2cfee-108">DESCRIPTION</span></span>
<span data-ttu-id="2cfee-109">Gyűjtemény képverzióját törölheti.</span><span class="sxs-lookup"><span data-stu-id="2cfee-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="2cfee-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2cfee-110">EXAMPLES</span></span>

### <span data-ttu-id="2cfee-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2cfee-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="2cfee-112">Törölje a gyűjtemény adott képverzióját.</span><span class="sxs-lookup"><span data-stu-id="2cfee-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="2cfee-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cfee-113">PARAMETERS</span></span>

### <span data-ttu-id="2cfee-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cfee-114">-AsJob</span></span>
<span data-ttu-id="2cfee-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2cfee-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cfee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfee-116">-DefaultProfile</span></span>
<span data-ttu-id="2cfee-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cfee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cfee-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2cfee-118">-Force</span></span>
<span data-ttu-id="2cfee-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="2cfee-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2cfee-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="2cfee-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="2cfee-121">A gyűjtemény képdefiníciójának neve.</span><span class="sxs-lookup"><span data-stu-id="2cfee-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="2cfee-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="2cfee-122">-GalleryName</span></span>
<span data-ttu-id="2cfee-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="2cfee-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="2cfee-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cfee-124">-InputObject</span></span>
<span data-ttu-id="2cfee-125">A PS-gyűjtemény Kép verzióobjektuma</span><span class="sxs-lookup"><span data-stu-id="2cfee-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="2cfee-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2cfee-126">-Name</span></span>
<span data-ttu-id="2cfee-127">A galériakép verziószámának neve.</span><span class="sxs-lookup"><span data-stu-id="2cfee-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="2cfee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cfee-128">-ResourceGroupName</span></span>
<span data-ttu-id="2cfee-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2cfee-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="2cfee-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cfee-130">-ResourceId</span></span>
<span data-ttu-id="2cfee-131">The resource ID for gallery image version</span><span class="sxs-lookup"><span data-stu-id="2cfee-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="2cfee-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cfee-132">-Confirm</span></span>
<span data-ttu-id="2cfee-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2cfee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cfee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cfee-134">-WhatIf</span></span>
<span data-ttu-id="2cfee-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2cfee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cfee-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2cfee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cfee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfee-137">CommonParameters</span></span>
<span data-ttu-id="2cfee-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cfee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfee-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cfee-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfee-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cfee-140">INPUTS</span></span>

### <span data-ttu-id="2cfee-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2cfee-141">System.String</span></span>

### <span data-ttu-id="2cfee-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2cfee-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="2cfee-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cfee-143">OUTPUTS</span></span>

### <span data-ttu-id="2cfee-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2cfee-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2cfee-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2cfee-145">NOTES</span></span>

## <span data-ttu-id="2cfee-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cfee-146">RELATED LINKS</span></span>
