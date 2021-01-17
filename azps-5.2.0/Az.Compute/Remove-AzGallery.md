---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337649"
---
# <span data-ttu-id="deacd-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="deacd-101">Remove-AzGallery</span></span>

## <span data-ttu-id="deacd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deacd-102">SYNOPSIS</span></span>
<span data-ttu-id="deacd-103">Gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="deacd-103">Delete a gallery.</span></span>

## <span data-ttu-id="deacd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="deacd-104">SYNTAX</span></span>

### <span data-ttu-id="deacd-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="deacd-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deacd-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="deacd-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deacd-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="deacd-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deacd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="deacd-108">DESCRIPTION</span></span>
<span data-ttu-id="deacd-109">Gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="deacd-109">Delete a gallery.</span></span>

## <span data-ttu-id="deacd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="deacd-110">EXAMPLES</span></span>

### <span data-ttu-id="deacd-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="deacd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="deacd-112">Törölje az adott gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="deacd-112">Delete the given gallery.</span></span>

## <span data-ttu-id="deacd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="deacd-113">PARAMETERS</span></span>

### <span data-ttu-id="deacd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="deacd-114">-AsJob</span></span>
<span data-ttu-id="deacd-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="deacd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="deacd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deacd-116">-DefaultProfile</span></span>
<span data-ttu-id="deacd-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="deacd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deacd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="deacd-118">-Force</span></span>
<span data-ttu-id="deacd-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="deacd-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="deacd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="deacd-120">-InputObject</span></span>
<span data-ttu-id="deacd-121">A PS-gyűjtemény objektum</span><span class="sxs-lookup"><span data-stu-id="deacd-121">The PS Gallery Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="deacd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="deacd-122">-Name</span></span>
<span data-ttu-id="deacd-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="deacd-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deacd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deacd-124">-ResourceGroupName</span></span>
<span data-ttu-id="deacd-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="deacd-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="deacd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="deacd-126">-ResourceId</span></span>
<span data-ttu-id="deacd-127">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="deacd-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="deacd-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="deacd-128">-Confirm</span></span>
<span data-ttu-id="deacd-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="deacd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deacd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deacd-130">-WhatIf</span></span>
<span data-ttu-id="deacd-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="deacd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deacd-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="deacd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deacd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deacd-133">CommonParameters</span></span>
<span data-ttu-id="deacd-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deacd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deacd-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="deacd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deacd-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="deacd-136">INPUTS</span></span>

### <span data-ttu-id="deacd-137">System.String</span><span class="sxs-lookup"><span data-stu-id="deacd-137">System.String</span></span>

### <span data-ttu-id="deacd-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="deacd-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="deacd-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="deacd-139">OUTPUTS</span></span>

### <span data-ttu-id="deacd-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="deacd-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="deacd-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="deacd-141">NOTES</span></span>

## <span data-ttu-id="deacd-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="deacd-142">RELATED LINKS</span></span>
