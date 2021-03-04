---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: abc9fd93545f229c39dd696a856781ceed748a77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937081"
---
# <span data-ttu-id="bcc35-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="bcc35-101">Remove-AzGallery</span></span>

## <span data-ttu-id="bcc35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcc35-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc35-103">Gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="bcc35-103">Delete a gallery.</span></span>

## <span data-ttu-id="bcc35-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bcc35-104">SYNTAX</span></span>

### <span data-ttu-id="bcc35-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bcc35-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcc35-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="bcc35-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcc35-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="bcc35-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcc35-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bcc35-108">DESCRIPTION</span></span>
<span data-ttu-id="bcc35-109">Gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="bcc35-109">Delete a gallery.</span></span>

## <span data-ttu-id="bcc35-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bcc35-110">EXAMPLES</span></span>

### <span data-ttu-id="bcc35-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="bcc35-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="bcc35-112">Törölje az adott gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="bcc35-112">Delete the given gallery.</span></span>

## <span data-ttu-id="bcc35-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcc35-113">PARAMETERS</span></span>

### <span data-ttu-id="bcc35-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcc35-114">-AsJob</span></span>
<span data-ttu-id="bcc35-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bcc35-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcc35-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc35-116">-DefaultProfile</span></span>
<span data-ttu-id="bcc35-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bcc35-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcc35-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bcc35-118">-Force</span></span>
<span data-ttu-id="bcc35-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="bcc35-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bcc35-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcc35-120">-InputObject</span></span>
<span data-ttu-id="bcc35-121">A PS-gyűjtemény objektum</span><span class="sxs-lookup"><span data-stu-id="bcc35-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="bcc35-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bcc35-122">-Name</span></span>
<span data-ttu-id="bcc35-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="bcc35-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="bcc35-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc35-124">-ResourceGroupName</span></span>
<span data-ttu-id="bcc35-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bcc35-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="bcc35-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcc35-126">-ResourceId</span></span>
<span data-ttu-id="bcc35-127">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="bcc35-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="bcc35-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcc35-128">-Confirm</span></span>
<span data-ttu-id="bcc35-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bcc35-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcc35-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcc35-130">-WhatIf</span></span>
<span data-ttu-id="bcc35-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bcc35-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcc35-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bcc35-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcc35-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc35-133">CommonParameters</span></span>
<span data-ttu-id="bcc35-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcc35-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc35-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcc35-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc35-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcc35-136">INPUTS</span></span>

### <span data-ttu-id="bcc35-137">System.String</span><span class="sxs-lookup"><span data-stu-id="bcc35-137">System.String</span></span>

### <span data-ttu-id="bcc35-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="bcc35-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="bcc35-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcc35-139">OUTPUTS</span></span>

### <span data-ttu-id="bcc35-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="bcc35-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="bcc35-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bcc35-141">NOTES</span></span>

## <span data-ttu-id="bcc35-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcc35-142">RELATED LINKS</span></span>
