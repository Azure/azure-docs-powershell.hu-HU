---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465878"
---
# <span data-ttu-id="07080-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="07080-101">Update-AzImage</span></span>

## <span data-ttu-id="07080-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07080-102">SYNOPSIS</span></span>
<span data-ttu-id="07080-103">Frissíti a képet.</span><span class="sxs-lookup"><span data-stu-id="07080-103">Updates an image.</span></span>

## <span data-ttu-id="07080-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07080-104">SYNTAX</span></span>

### <span data-ttu-id="07080-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07080-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07080-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="07080-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07080-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="07080-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07080-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07080-108">DESCRIPTION</span></span>
<span data-ttu-id="07080-109">Az **Update-AzImage parancsmag** frissíti a képet.</span><span class="sxs-lookup"><span data-stu-id="07080-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="07080-110">Jelenleg csak a címkék frissíthetők.</span><span class="sxs-lookup"><span data-stu-id="07080-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="07080-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07080-111">EXAMPLES</span></span>

### <span data-ttu-id="07080-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="07080-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="07080-113">Ez a parancs frissíti a meglévő "Image01" kép címkeértékét az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="07080-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="07080-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07080-114">PARAMETERS</span></span>

### <span data-ttu-id="07080-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07080-115">-AsJob</span></span>
<span data-ttu-id="07080-116">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="07080-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="07080-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07080-117">-DefaultProfile</span></span>
<span data-ttu-id="07080-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07080-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07080-119">-Image</span><span class="sxs-lookup"><span data-stu-id="07080-119">-Image</span></span>
<span data-ttu-id="07080-120">Helyi képobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="07080-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07080-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="07080-121">-ImageName</span></span>
<span data-ttu-id="07080-122">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07080-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07080-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07080-123">-ResourceGroupName</span></span>
<span data-ttu-id="07080-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07080-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="07080-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07080-125">-ResourceId</span></span>
<span data-ttu-id="07080-126">A kép erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="07080-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="07080-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="07080-127">-Tag</span></span>
<span data-ttu-id="07080-128">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="07080-128">Resource tags</span></span>

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

### <span data-ttu-id="07080-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07080-129">-Confirm</span></span>
<span data-ttu-id="07080-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="07080-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07080-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07080-131">-WhatIf</span></span>
<span data-ttu-id="07080-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="07080-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07080-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07080-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07080-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07080-134">CommonParameters</span></span>
<span data-ttu-id="07080-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07080-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07080-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07080-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07080-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07080-137">INPUTS</span></span>

### <span data-ttu-id="07080-138">System.String</span><span class="sxs-lookup"><span data-stu-id="07080-138">System.String</span></span>

### <span data-ttu-id="07080-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="07080-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="07080-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07080-140">OUTPUTS</span></span>

### <span data-ttu-id="07080-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="07080-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="07080-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07080-142">NOTES</span></span>

## <span data-ttu-id="07080-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07080-143">RELATED LINKS</span></span>
