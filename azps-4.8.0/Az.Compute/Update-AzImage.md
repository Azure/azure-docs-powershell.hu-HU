---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181990"
---
# <span data-ttu-id="54402-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="54402-101">Update-AzImage</span></span>

## <span data-ttu-id="54402-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54402-102">SYNOPSIS</span></span>
<span data-ttu-id="54402-103">Frissít egy képet.</span><span class="sxs-lookup"><span data-stu-id="54402-103">Updates an image.</span></span>

## <span data-ttu-id="54402-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54402-104">SYNTAX</span></span>

### <span data-ttu-id="54402-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="54402-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54402-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="54402-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54402-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="54402-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54402-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="54402-108">DESCRIPTION</span></span>
<span data-ttu-id="54402-109">Az **Update-AzImage** parancsmag frissíti a képet.</span><span class="sxs-lookup"><span data-stu-id="54402-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="54402-110">Jelenleg csak a címkéket lehet frissíteni.</span><span class="sxs-lookup"><span data-stu-id="54402-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="54402-111">Példák</span><span class="sxs-lookup"><span data-stu-id="54402-111">EXAMPLES</span></span>

### <span data-ttu-id="54402-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="54402-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="54402-113">Ez a parancs frissíti a "ResourceGroup01" erőforráscsoport "Image01" a meglévő kép címke értékét.</span><span class="sxs-lookup"><span data-stu-id="54402-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="54402-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54402-114">PARAMETERS</span></span>

### <span data-ttu-id="54402-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54402-115">-AsJob</span></span>
<span data-ttu-id="54402-116">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="54402-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="54402-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54402-117">-DefaultProfile</span></span>
<span data-ttu-id="54402-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54402-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54402-119">-Kép</span><span class="sxs-lookup"><span data-stu-id="54402-119">-Image</span></span>
<span data-ttu-id="54402-120">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="54402-120">Specifies a local image object.</span></span>

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

### <span data-ttu-id="54402-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="54402-121">-ImageName</span></span>
<span data-ttu-id="54402-122">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54402-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="54402-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54402-123">-ResourceGroupName</span></span>
<span data-ttu-id="54402-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54402-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="54402-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54402-125">-ResourceId</span></span>
<span data-ttu-id="54402-126">A kép erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="54402-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="54402-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="54402-127">-Tag</span></span>
<span data-ttu-id="54402-128">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="54402-128">Resource tags</span></span>

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

### <span data-ttu-id="54402-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54402-129">-Confirm</span></span>
<span data-ttu-id="54402-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54402-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54402-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54402-131">-WhatIf</span></span>
<span data-ttu-id="54402-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54402-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54402-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54402-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54402-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54402-134">CommonParameters</span></span>
<span data-ttu-id="54402-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54402-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54402-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="54402-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54402-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54402-137">INPUTS</span></span>

### <span data-ttu-id="54402-138">System. String</span><span class="sxs-lookup"><span data-stu-id="54402-138">System.String</span></span>

### <span data-ttu-id="54402-139">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="54402-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="54402-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54402-140">OUTPUTS</span></span>

### <span data-ttu-id="54402-141">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="54402-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="54402-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54402-142">NOTES</span></span>

## <span data-ttu-id="54402-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54402-143">RELATED LINKS</span></span>
