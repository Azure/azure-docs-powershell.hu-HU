---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847653"
---
# <span data-ttu-id="eb666-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="eb666-101">Remove-AzGallery</span></span>

## <span data-ttu-id="eb666-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb666-102">SYNOPSIS</span></span>
<span data-ttu-id="eb666-103">Gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="eb666-103">Delete a gallery.</span></span>

## <span data-ttu-id="eb666-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb666-104">SYNTAX</span></span>

### <span data-ttu-id="eb666-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb666-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb666-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="eb666-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb666-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="eb666-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb666-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb666-108">DESCRIPTION</span></span>
<span data-ttu-id="eb666-109">Gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="eb666-109">Delete a gallery.</span></span>

## <span data-ttu-id="eb666-110">Példák</span><span class="sxs-lookup"><span data-stu-id="eb666-110">EXAMPLES</span></span>

### <span data-ttu-id="eb666-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eb666-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="eb666-112">Törölje a megadott gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="eb666-112">Delete the given gallery.</span></span>

## <span data-ttu-id="eb666-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb666-113">PARAMETERS</span></span>

### <span data-ttu-id="eb666-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb666-114">-AsJob</span></span>
<span data-ttu-id="eb666-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="eb666-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb666-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb666-116">-DefaultProfile</span></span>
<span data-ttu-id="eb666-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb666-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb666-118">-Force</span><span class="sxs-lookup"><span data-stu-id="eb666-118">-Force</span></span>
<span data-ttu-id="eb666-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="eb666-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eb666-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb666-120">-InputObject</span></span>
<span data-ttu-id="eb666-121">A PS-gyűjtemény objektuma</span><span class="sxs-lookup"><span data-stu-id="eb666-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="eb666-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb666-122">-Name</span></span>
<span data-ttu-id="eb666-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="eb666-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="eb666-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb666-124">-ResourceGroupName</span></span>
<span data-ttu-id="eb666-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eb666-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="eb666-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb666-126">-ResourceId</span></span>
<span data-ttu-id="eb666-127">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="eb666-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="eb666-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb666-128">-Confirm</span></span>
<span data-ttu-id="eb666-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb666-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb666-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb666-130">-WhatIf</span></span>
<span data-ttu-id="eb666-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb666-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb666-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb666-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb666-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb666-133">CommonParameters</span></span>
<span data-ttu-id="eb666-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb666-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb666-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eb666-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb666-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb666-136">INPUTS</span></span>

### <span data-ttu-id="eb666-137">System. String</span><span class="sxs-lookup"><span data-stu-id="eb666-137">System.String</span></span>

### <span data-ttu-id="eb666-138">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="eb666-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="eb666-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb666-139">OUTPUTS</span></span>

### <span data-ttu-id="eb666-140">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="eb666-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="eb666-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb666-141">NOTES</span></span>

## <span data-ttu-id="eb666-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb666-142">RELATED LINKS</span></span>
