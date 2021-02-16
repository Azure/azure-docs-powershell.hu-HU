---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162243"
---
# <span data-ttu-id="4fc4c-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="4fc4c-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="4fc4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fc4c-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc4c-103">Gyűjtemény képdefiníciójának törlése</span><span class="sxs-lookup"><span data-stu-id="4fc4c-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="4fc4c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4fc4c-104">SYNTAX</span></span>

### <span data-ttu-id="4fc4c-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fc4c-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fc4c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4fc4c-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fc4c-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4fc4c-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fc4c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4fc4c-108">DESCRIPTION</span></span>
<span data-ttu-id="4fc4c-109">Gyűjtemény képdefiníciójának törlése</span><span class="sxs-lookup"><span data-stu-id="4fc4c-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="4fc4c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4fc4c-110">EXAMPLES</span></span>

### <span data-ttu-id="4fc4c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4fc4c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="4fc4c-112">Távolítsa el a gyűjtemény képdefinícióját.</span><span class="sxs-lookup"><span data-stu-id="4fc4c-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="4fc4c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fc4c-113">PARAMETERS</span></span>

### <span data-ttu-id="4fc4c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fc4c-114">-AsJob</span></span>
<span data-ttu-id="4fc4c-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4fc4c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fc4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc4c-116">-DefaultProfile</span></span>
<span data-ttu-id="4fc4c-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fc4c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fc4c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4fc4c-118">-Force</span></span>
<span data-ttu-id="4fc4c-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4fc4c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4fc4c-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="4fc4c-120">-GalleryName</span></span>
<span data-ttu-id="4fc4c-121">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="4fc4c-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="4fc4c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fc4c-122">-InputObject</span></span>
<span data-ttu-id="4fc4c-123">A PS-gyűjtemény képdefiníciós objektuma</span><span class="sxs-lookup"><span data-stu-id="4fc4c-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc4c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4fc4c-124">-Name</span></span>
<span data-ttu-id="4fc4c-125">A gyűjtemény képdefiníciójának neve.</span><span class="sxs-lookup"><span data-stu-id="4fc4c-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc4c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fc4c-126">-ResourceGroupName</span></span>
<span data-ttu-id="4fc4c-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4fc4c-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="4fc4c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fc4c-128">-ResourceId</span></span>
<span data-ttu-id="4fc4c-129">A gyűjtemény képdefiníciójának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4fc4c-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="4fc4c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fc4c-130">-Confirm</span></span>
<span data-ttu-id="4fc4c-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4fc4c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fc4c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc4c-132">-WhatIf</span></span>
<span data-ttu-id="4fc4c-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4fc4c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fc4c-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fc4c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fc4c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc4c-135">CommonParameters</span></span>
<span data-ttu-id="4fc4c-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc4c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc4c-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fc4c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc4c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fc4c-138">INPUTS</span></span>

### <span data-ttu-id="4fc4c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4fc4c-139">System.String</span></span>

### <span data-ttu-id="4fc4c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="4fc4c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="4fc4c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fc4c-141">OUTPUTS</span></span>

### <span data-ttu-id="4fc4c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4fc4c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4fc4c-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4fc4c-143">NOTES</span></span>

## <span data-ttu-id="4fc4c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fc4c-144">RELATED LINKS</span></span>
