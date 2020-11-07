---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847649"
---
# <span data-ttu-id="940e0-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="940e0-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="940e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="940e0-102">SYNOPSIS</span></span>
<span data-ttu-id="940e0-103">Gyűjtemény képdefiníciójának törlése</span><span class="sxs-lookup"><span data-stu-id="940e0-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="940e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="940e0-104">SYNTAX</span></span>

### <span data-ttu-id="940e0-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="940e0-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="940e0-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="940e0-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="940e0-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="940e0-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="940e0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="940e0-108">DESCRIPTION</span></span>
<span data-ttu-id="940e0-109">Gyűjtemény képdefiníciójának törlése</span><span class="sxs-lookup"><span data-stu-id="940e0-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="940e0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="940e0-110">EXAMPLES</span></span>

### <span data-ttu-id="940e0-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="940e0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="940e0-112">A gyűjtemény képének definíciójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="940e0-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="940e0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="940e0-113">PARAMETERS</span></span>

### <span data-ttu-id="940e0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="940e0-114">-AsJob</span></span>
<span data-ttu-id="940e0-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="940e0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="940e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="940e0-116">-DefaultProfile</span></span>
<span data-ttu-id="940e0-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="940e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="940e0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="940e0-118">-Force</span></span>
<span data-ttu-id="940e0-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="940e0-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="940e0-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="940e0-120">-GalleryName</span></span>
<span data-ttu-id="940e0-121">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="940e0-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="940e0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="940e0-122">-InputObject</span></span>
<span data-ttu-id="940e0-123">A PS-gyűjtemény képdefiníciós objektuma</span><span class="sxs-lookup"><span data-stu-id="940e0-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="940e0-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="940e0-124">-Name</span></span>
<span data-ttu-id="940e0-125">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="940e0-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="940e0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="940e0-126">-ResourceGroupName</span></span>
<span data-ttu-id="940e0-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="940e0-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="940e0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="940e0-128">-ResourceId</span></span>
<span data-ttu-id="940e0-129">A tár képdefiníciójának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="940e0-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="940e0-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="940e0-130">-Confirm</span></span>
<span data-ttu-id="940e0-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="940e0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="940e0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="940e0-132">-WhatIf</span></span>
<span data-ttu-id="940e0-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="940e0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="940e0-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="940e0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="940e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940e0-135">CommonParameters</span></span>
<span data-ttu-id="940e0-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="940e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940e0-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="940e0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940e0-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="940e0-138">INPUTS</span></span>

### <span data-ttu-id="940e0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="940e0-139">System.String</span></span>

### <span data-ttu-id="940e0-140">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="940e0-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="940e0-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="940e0-141">OUTPUTS</span></span>

### <span data-ttu-id="940e0-142">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="940e0-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="940e0-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="940e0-143">NOTES</span></span>

## <span data-ttu-id="940e0-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="940e0-144">RELATED LINKS</span></span>
