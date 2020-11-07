---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846141"
---
# <span data-ttu-id="deffd-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="deffd-101">Update-AzGallery</span></span>

## <span data-ttu-id="deffd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="deffd-102">SYNOPSIS</span></span>
<span data-ttu-id="deffd-103">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="deffd-103">Update a gallery.</span></span>

## <span data-ttu-id="deffd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="deffd-104">SYNTAX</span></span>

### <span data-ttu-id="deffd-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="deffd-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deffd-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="deffd-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deffd-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="deffd-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deffd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="deffd-108">DESCRIPTION</span></span>
<span data-ttu-id="deffd-109">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="deffd-109">Update a gallery.</span></span>

## <span data-ttu-id="deffd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="deffd-110">EXAMPLES</span></span>

### <span data-ttu-id="deffd-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="deffd-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="deffd-112">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="deffd-112">Update a gallery.</span></span>

## <span data-ttu-id="deffd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="deffd-113">PARAMETERS</span></span>

### <span data-ttu-id="deffd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="deffd-114">-AsJob</span></span>
<span data-ttu-id="deffd-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="deffd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="deffd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deffd-116">-DefaultProfile</span></span>
<span data-ttu-id="deffd-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="deffd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deffd-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="deffd-118">-Description</span></span>
<span data-ttu-id="deffd-119">A gyűjtemény-erőforrás leírása.</span><span class="sxs-lookup"><span data-stu-id="deffd-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="deffd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="deffd-120">-InputObject</span></span>
<span data-ttu-id="deffd-121">A PS-gyűjtemény objektuma.</span><span class="sxs-lookup"><span data-stu-id="deffd-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="deffd-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="deffd-122">-Name</span></span>
<span data-ttu-id="deffd-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="deffd-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="deffd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deffd-124">-ResourceGroupName</span></span>
<span data-ttu-id="deffd-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="deffd-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="deffd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="deffd-126">-ResourceId</span></span>
<span data-ttu-id="deffd-127">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="deffd-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="deffd-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="deffd-128">-Tag</span></span>
<span data-ttu-id="deffd-129">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="deffd-129">Resource tags</span></span>

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

### <span data-ttu-id="deffd-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="deffd-130">-Confirm</span></span>
<span data-ttu-id="deffd-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="deffd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deffd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deffd-132">-WhatIf</span></span>
<span data-ttu-id="deffd-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="deffd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deffd-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="deffd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deffd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deffd-135">CommonParameters</span></span>
<span data-ttu-id="deffd-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="deffd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deffd-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="deffd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deffd-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="deffd-138">INPUTS</span></span>

### <span data-ttu-id="deffd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="deffd-139">System.String</span></span>

### <span data-ttu-id="deffd-140">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="deffd-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="deffd-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="deffd-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="deffd-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="deffd-142">OUTPUTS</span></span>

### <span data-ttu-id="deffd-143">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="deffd-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="deffd-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="deffd-144">NOTES</span></span>

## <span data-ttu-id="deffd-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="deffd-145">RELATED LINKS</span></span>
