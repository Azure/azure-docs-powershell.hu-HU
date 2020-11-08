---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183397"
---
# <span data-ttu-id="fa7e8-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="fa7e8-101">Update-AzGallery</span></span>

## <span data-ttu-id="fa7e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fa7e8-102">SYNOPSIS</span></span>
<span data-ttu-id="fa7e8-103">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="fa7e8-103">Update a gallery.</span></span>

## <span data-ttu-id="fa7e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fa7e8-104">SYNTAX</span></span>

### <span data-ttu-id="fa7e8-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa7e8-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa7e8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="fa7e8-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa7e8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="fa7e8-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa7e8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fa7e8-108">DESCRIPTION</span></span>
<span data-ttu-id="fa7e8-109">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="fa7e8-109">Update a gallery.</span></span>

## <span data-ttu-id="fa7e8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fa7e8-110">EXAMPLES</span></span>

### <span data-ttu-id="fa7e8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fa7e8-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="fa7e8-112">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="fa7e8-112">Update a gallery.</span></span>

## <span data-ttu-id="fa7e8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fa7e8-113">PARAMETERS</span></span>

### <span data-ttu-id="fa7e8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa7e8-114">-AsJob</span></span>
<span data-ttu-id="fa7e8-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fa7e8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa7e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa7e8-116">-DefaultProfile</span></span>
<span data-ttu-id="fa7e8-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa7e8-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="fa7e8-118">-Description</span></span>
<span data-ttu-id="fa7e8-119">A gyűjtemény-erőforrás leírása.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="fa7e8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa7e8-120">-InputObject</span></span>
<span data-ttu-id="fa7e8-121">A PS-gyűjtemény objektuma.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="fa7e8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fa7e8-122">-Name</span></span>
<span data-ttu-id="fa7e8-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="fa7e8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa7e8-124">-ResourceGroupName</span></span>
<span data-ttu-id="fa7e8-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="fa7e8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa7e8-126">-ResourceId</span></span>
<span data-ttu-id="fa7e8-127">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fa7e8-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="fa7e8-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="fa7e8-128">-Tag</span></span>
<span data-ttu-id="fa7e8-129">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="fa7e8-129">Resource tags</span></span>

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

### <span data-ttu-id="fa7e8-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fa7e8-130">-Confirm</span></span>
<span data-ttu-id="fa7e8-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa7e8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa7e8-132">-WhatIf</span></span>
<span data-ttu-id="fa7e8-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa7e8-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa7e8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa7e8-135">CommonParameters</span></span>
<span data-ttu-id="fa7e8-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fa7e8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa7e8-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa7e8-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa7e8-138">INPUTS</span></span>

### <span data-ttu-id="fa7e8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fa7e8-139">System.String</span></span>

### <span data-ttu-id="fa7e8-140">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="fa7e8-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="fa7e8-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fa7e8-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fa7e8-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa7e8-142">OUTPUTS</span></span>

### <span data-ttu-id="fa7e8-143">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="fa7e8-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="fa7e8-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fa7e8-144">NOTES</span></span>

## <span data-ttu-id="fa7e8-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa7e8-145">RELATED LINKS</span></span>
