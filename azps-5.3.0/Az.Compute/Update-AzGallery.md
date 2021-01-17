---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480667"
---
# <span data-ttu-id="47ccd-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="47ccd-101">Update-AzGallery</span></span>

## <span data-ttu-id="47ccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="47ccd-103">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="47ccd-103">Update a gallery.</span></span>

## <span data-ttu-id="47ccd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="47ccd-104">SYNTAX</span></span>

### <span data-ttu-id="47ccd-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47ccd-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ccd-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="47ccd-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ccd-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="47ccd-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47ccd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="47ccd-108">DESCRIPTION</span></span>
<span data-ttu-id="47ccd-109">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="47ccd-109">Update a gallery.</span></span>

## <span data-ttu-id="47ccd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="47ccd-110">EXAMPLES</span></span>

### <span data-ttu-id="47ccd-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="47ccd-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="47ccd-112">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="47ccd-112">Update a gallery.</span></span>

## <span data-ttu-id="47ccd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47ccd-113">PARAMETERS</span></span>

### <span data-ttu-id="47ccd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47ccd-114">-AsJob</span></span>
<span data-ttu-id="47ccd-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="47ccd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47ccd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ccd-116">-DefaultProfile</span></span>
<span data-ttu-id="47ccd-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47ccd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47ccd-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="47ccd-118">-Description</span></span>
<span data-ttu-id="47ccd-119">A gyűjtemény típusú erőforrás leírása.</span><span class="sxs-lookup"><span data-stu-id="47ccd-119">The description of the gallery resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47ccd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47ccd-120">-InputObject</span></span>
<span data-ttu-id="47ccd-121">A PS-gyűjtemény objektum.</span><span class="sxs-lookup"><span data-stu-id="47ccd-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="47ccd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="47ccd-122">-Name</span></span>
<span data-ttu-id="47ccd-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="47ccd-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="47ccd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47ccd-124">-ResourceGroupName</span></span>
<span data-ttu-id="47ccd-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="47ccd-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="47ccd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47ccd-126">-ResourceId</span></span>
<span data-ttu-id="47ccd-127">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="47ccd-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="47ccd-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="47ccd-128">-Tag</span></span>
<span data-ttu-id="47ccd-129">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="47ccd-129">Resource tags</span></span>

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

### <span data-ttu-id="47ccd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47ccd-130">-Confirm</span></span>
<span data-ttu-id="47ccd-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="47ccd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ccd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ccd-132">-WhatIf</span></span>
<span data-ttu-id="47ccd-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="47ccd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47ccd-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47ccd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ccd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ccd-135">CommonParameters</span></span>
<span data-ttu-id="47ccd-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ccd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ccd-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47ccd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ccd-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47ccd-138">INPUTS</span></span>

### <span data-ttu-id="47ccd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="47ccd-139">System.String</span></span>

### <span data-ttu-id="47ccd-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="47ccd-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="47ccd-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="47ccd-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="47ccd-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47ccd-142">OUTPUTS</span></span>

### <span data-ttu-id="47ccd-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="47ccd-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="47ccd-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="47ccd-144">NOTES</span></span>

## <span data-ttu-id="47ccd-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47ccd-145">RELATED LINKS</span></span>
