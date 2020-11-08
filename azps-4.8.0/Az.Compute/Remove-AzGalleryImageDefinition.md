---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018121"
---
# <span data-ttu-id="b7de3-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="b7de3-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="b7de3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7de3-102">SYNOPSIS</span></span>
<span data-ttu-id="b7de3-103">Gyűjtemény képdefiníciójának törlése</span><span class="sxs-lookup"><span data-stu-id="b7de3-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="b7de3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7de3-104">SYNTAX</span></span>

### <span data-ttu-id="b7de3-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7de3-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7de3-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b7de3-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7de3-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b7de3-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7de3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7de3-108">DESCRIPTION</span></span>
<span data-ttu-id="b7de3-109">Gyűjtemény képdefiníciójának törlése</span><span class="sxs-lookup"><span data-stu-id="b7de3-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="b7de3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b7de3-110">EXAMPLES</span></span>

### <span data-ttu-id="b7de3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b7de3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="b7de3-112">A gyűjtemény képének definíciójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b7de3-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="b7de3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7de3-113">PARAMETERS</span></span>

### <span data-ttu-id="b7de3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7de3-114">-AsJob</span></span>
<span data-ttu-id="b7de3-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b7de3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7de3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7de3-116">-DefaultProfile</span></span>
<span data-ttu-id="b7de3-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7de3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7de3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b7de3-118">-Force</span></span>
<span data-ttu-id="b7de3-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b7de3-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b7de3-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="b7de3-120">-GalleryName</span></span>
<span data-ttu-id="b7de3-121">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="b7de3-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="b7de3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7de3-122">-InputObject</span></span>
<span data-ttu-id="b7de3-123">A PS-gyűjtemény képdefiníciós objektuma</span><span class="sxs-lookup"><span data-stu-id="b7de3-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="b7de3-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b7de3-124">-Name</span></span>
<span data-ttu-id="b7de3-125">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="b7de3-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="b7de3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7de3-126">-ResourceGroupName</span></span>
<span data-ttu-id="b7de3-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b7de3-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7de3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7de3-128">-ResourceId</span></span>
<span data-ttu-id="b7de3-129">A tár képdefiníciójának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b7de3-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="b7de3-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7de3-130">-Confirm</span></span>
<span data-ttu-id="b7de3-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7de3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7de3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7de3-132">-WhatIf</span></span>
<span data-ttu-id="b7de3-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7de3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7de3-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7de3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7de3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7de3-135">CommonParameters</span></span>
<span data-ttu-id="b7de3-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7de3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7de3-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b7de3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7de3-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7de3-138">INPUTS</span></span>

### <span data-ttu-id="b7de3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b7de3-139">System.String</span></span>

### <span data-ttu-id="b7de3-140">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="b7de3-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="b7de3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7de3-141">OUTPUTS</span></span>

### <span data-ttu-id="b7de3-142">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b7de3-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b7de3-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7de3-143">NOTES</span></span>

## <span data-ttu-id="b7de3-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7de3-144">RELATED LINKS</span></span>
