---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: a6046dc58e010905094f1f0db47f49f7840cc913
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836734"
---
# <span data-ttu-id="f9f02-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="f9f02-101">Remove-AzGallery</span></span>

## <span data-ttu-id="f9f02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9f02-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f02-103">Gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="f9f02-103">Delete a gallery.</span></span>

## <span data-ttu-id="f9f02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9f02-104">SYNTAX</span></span>

### <span data-ttu-id="f9f02-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f9f02-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9f02-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f9f02-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9f02-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f9f02-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9f02-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9f02-108">DESCRIPTION</span></span>
<span data-ttu-id="f9f02-109">Gyűjtemény törlése</span><span class="sxs-lookup"><span data-stu-id="f9f02-109">Delete a gallery.</span></span>

## <span data-ttu-id="f9f02-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f9f02-110">EXAMPLES</span></span>

### <span data-ttu-id="f9f02-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f9f02-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="f9f02-112">Törölje a megadott gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="f9f02-112">Delete the given gallery.</span></span>

## <span data-ttu-id="f9f02-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9f02-113">PARAMETERS</span></span>

### <span data-ttu-id="f9f02-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9f02-114">-AsJob</span></span>
<span data-ttu-id="f9f02-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f9f02-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9f02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f02-116">-DefaultProfile</span></span>
<span data-ttu-id="f9f02-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9f02-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9f02-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f9f02-118">-Force</span></span>
<span data-ttu-id="f9f02-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f9f02-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f9f02-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9f02-120">-InputObject</span></span>
<span data-ttu-id="f9f02-121">A PS-gyűjtemény objektuma</span><span class="sxs-lookup"><span data-stu-id="f9f02-121">The PS Gallery Object</span></span>

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

### <span data-ttu-id="f9f02-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f9f02-122">-Name</span></span>
<span data-ttu-id="f9f02-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="f9f02-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="f9f02-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f02-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9f02-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f9f02-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9f02-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9f02-126">-ResourceId</span></span>
<span data-ttu-id="f9f02-127">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f9f02-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="f9f02-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f9f02-128">-Confirm</span></span>
<span data-ttu-id="f9f02-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f9f02-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9f02-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9f02-130">-WhatIf</span></span>
<span data-ttu-id="f9f02-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f9f02-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9f02-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9f02-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9f02-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f02-133">CommonParameters</span></span>
<span data-ttu-id="f9f02-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9f02-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f02-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9f02-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f02-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9f02-136">INPUTS</span></span>

### <span data-ttu-id="f9f02-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f9f02-137">System.String</span></span>

### <span data-ttu-id="f9f02-138">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="f9f02-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="f9f02-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9f02-139">OUTPUTS</span></span>

### <span data-ttu-id="f9f02-140">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f9f02-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f9f02-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9f02-141">NOTES</span></span>

## <span data-ttu-id="f9f02-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9f02-142">RELATED LINKS</span></span>
