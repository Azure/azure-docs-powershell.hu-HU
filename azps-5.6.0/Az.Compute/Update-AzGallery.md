---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 4badbfc9973b20869c6db421bd1299e00337d7fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938257"
---
# <span data-ttu-id="1db6a-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="1db6a-101">Update-AzGallery</span></span>

## <span data-ttu-id="1db6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1db6a-102">SYNOPSIS</span></span>
<span data-ttu-id="1db6a-103">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="1db6a-103">Update a gallery.</span></span>

## <span data-ttu-id="1db6a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1db6a-104">SYNTAX</span></span>

### <span data-ttu-id="1db6a-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1db6a-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1db6a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1db6a-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1db6a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1db6a-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1db6a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1db6a-108">DESCRIPTION</span></span>
<span data-ttu-id="1db6a-109">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="1db6a-109">Update a gallery.</span></span>

## <span data-ttu-id="1db6a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1db6a-110">EXAMPLES</span></span>

### <span data-ttu-id="1db6a-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="1db6a-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="1db6a-112">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="1db6a-112">Update a gallery.</span></span>

## <span data-ttu-id="1db6a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1db6a-113">PARAMETERS</span></span>

### <span data-ttu-id="1db6a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1db6a-114">-AsJob</span></span>
<span data-ttu-id="1db6a-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1db6a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1db6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db6a-116">-DefaultProfile</span></span>
<span data-ttu-id="1db6a-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1db6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1db6a-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1db6a-118">-Description</span></span>
<span data-ttu-id="1db6a-119">A gyűjtemény típusú erőforrás leírása.</span><span class="sxs-lookup"><span data-stu-id="1db6a-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="1db6a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1db6a-120">-InputObject</span></span>
<span data-ttu-id="1db6a-121">A PS-gyűjtemény objektum.</span><span class="sxs-lookup"><span data-stu-id="1db6a-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="1db6a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1db6a-122">-Name</span></span>
<span data-ttu-id="1db6a-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="1db6a-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="1db6a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1db6a-124">-ResourceGroupName</span></span>
<span data-ttu-id="1db6a-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1db6a-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="1db6a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1db6a-126">-ResourceId</span></span>
<span data-ttu-id="1db6a-127">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1db6a-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="1db6a-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="1db6a-128">-Tag</span></span>
<span data-ttu-id="1db6a-129">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="1db6a-129">Resource tags</span></span>

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

### <span data-ttu-id="1db6a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1db6a-130">-Confirm</span></span>
<span data-ttu-id="1db6a-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1db6a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1db6a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1db6a-132">-WhatIf</span></span>
<span data-ttu-id="1db6a-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1db6a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1db6a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1db6a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1db6a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db6a-135">CommonParameters</span></span>
<span data-ttu-id="1db6a-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1db6a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db6a-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1db6a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db6a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1db6a-138">INPUTS</span></span>

### <span data-ttu-id="1db6a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1db6a-139">System.String</span></span>

### <span data-ttu-id="1db6a-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="1db6a-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="1db6a-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1db6a-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1db6a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1db6a-142">OUTPUTS</span></span>

### <span data-ttu-id="1db6a-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="1db6a-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="1db6a-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1db6a-144">NOTES</span></span>

## <span data-ttu-id="1db6a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1db6a-145">RELATED LINKS</span></span>
