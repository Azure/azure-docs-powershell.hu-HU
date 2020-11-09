---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 32628ff27485f70f9451a5ea331d8d3d60824cc4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296435"
---
# <span data-ttu-id="c5869-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="c5869-101">Update-AzGallery</span></span>

## <span data-ttu-id="c5869-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5869-102">SYNOPSIS</span></span>
<span data-ttu-id="c5869-103">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="c5869-103">Update a gallery.</span></span>

## <span data-ttu-id="c5869-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5869-104">SYNTAX</span></span>

### <span data-ttu-id="c5869-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5869-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5869-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c5869-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5869-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="c5869-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5869-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5869-108">DESCRIPTION</span></span>
<span data-ttu-id="c5869-109">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="c5869-109">Update a gallery.</span></span>

## <span data-ttu-id="c5869-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c5869-110">EXAMPLES</span></span>

### <span data-ttu-id="c5869-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c5869-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="c5869-112">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="c5869-112">Update a gallery.</span></span>

## <span data-ttu-id="c5869-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5869-113">PARAMETERS</span></span>

### <span data-ttu-id="c5869-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5869-114">-AsJob</span></span>
<span data-ttu-id="c5869-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c5869-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5869-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5869-116">-DefaultProfile</span></span>
<span data-ttu-id="c5869-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5869-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5869-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c5869-118">-Description</span></span>
<span data-ttu-id="c5869-119">A gyűjtemény-erőforrás leírása.</span><span class="sxs-lookup"><span data-stu-id="c5869-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="c5869-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5869-120">-InputObject</span></span>
<span data-ttu-id="c5869-121">A PS-gyűjtemény objektuma.</span><span class="sxs-lookup"><span data-stu-id="c5869-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="c5869-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5869-122">-Name</span></span>
<span data-ttu-id="c5869-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="c5869-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="c5869-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5869-124">-ResourceGroupName</span></span>
<span data-ttu-id="c5869-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c5869-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="c5869-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5869-126">-ResourceId</span></span>
<span data-ttu-id="c5869-127">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c5869-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="c5869-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="c5869-128">-Tag</span></span>
<span data-ttu-id="c5869-129">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="c5869-129">Resource tags</span></span>

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

### <span data-ttu-id="c5869-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c5869-130">-Confirm</span></span>
<span data-ttu-id="c5869-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5869-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5869-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5869-132">-WhatIf</span></span>
<span data-ttu-id="c5869-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c5869-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5869-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5869-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5869-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5869-135">CommonParameters</span></span>
<span data-ttu-id="c5869-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5869-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5869-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c5869-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5869-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5869-138">INPUTS</span></span>

### <span data-ttu-id="c5869-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c5869-139">System.String</span></span>

### <span data-ttu-id="c5869-140">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="c5869-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="c5869-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c5869-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c5869-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5869-142">OUTPUTS</span></span>

### <span data-ttu-id="c5869-143">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="c5869-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="c5869-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5869-144">NOTES</span></span>

## <span data-ttu-id="c5869-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5869-145">RELATED LINKS</span></span>
