---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 4c4809ed022595af7c0ad977d082c6a52616e920
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185608"
---
# <span data-ttu-id="d4833-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d4833-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="d4833-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4833-102">SYNOPSIS</span></span>
<span data-ttu-id="d4833-103">Gyűjtemény képének törlése</span><span class="sxs-lookup"><span data-stu-id="d4833-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="d4833-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4833-104">SYNTAX</span></span>

### <span data-ttu-id="d4833-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4833-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4833-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d4833-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4833-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d4833-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4833-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4833-108">DESCRIPTION</span></span>
<span data-ttu-id="d4833-109">Gyűjtemény képének törlése</span><span class="sxs-lookup"><span data-stu-id="d4833-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="d4833-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d4833-110">EXAMPLES</span></span>

### <span data-ttu-id="d4833-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d4833-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="d4833-112">Törölje az adott gyűjtemény képének verzióját.</span><span class="sxs-lookup"><span data-stu-id="d4833-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="d4833-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4833-113">PARAMETERS</span></span>

### <span data-ttu-id="d4833-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4833-114">-AsJob</span></span>
<span data-ttu-id="d4833-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d4833-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4833-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4833-116">-DefaultProfile</span></span>
<span data-ttu-id="d4833-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4833-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4833-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d4833-118">-Force</span></span>
<span data-ttu-id="d4833-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d4833-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d4833-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d4833-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="d4833-121">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="d4833-121">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4833-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="d4833-122">-GalleryName</span></span>
<span data-ttu-id="d4833-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="d4833-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="d4833-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4833-124">-InputObject</span></span>
<span data-ttu-id="d4833-125">A PS Gallery Image Version objektuma</span><span class="sxs-lookup"><span data-stu-id="d4833-125">The PS Gallery Image Version Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4833-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4833-126">-Name</span></span>
<span data-ttu-id="d4833-127">A gyűjtemény képének neve.</span><span class="sxs-lookup"><span data-stu-id="d4833-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4833-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4833-128">-ResourceGroupName</span></span>
<span data-ttu-id="d4833-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d4833-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="d4833-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4833-130">-ResourceId</span></span>
<span data-ttu-id="d4833-131">A gyűjtemény erőforrás-azonosítója a Képtár képének verziójában</span><span class="sxs-lookup"><span data-stu-id="d4833-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="d4833-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4833-132">-Confirm</span></span>
<span data-ttu-id="d4833-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4833-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4833-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4833-134">-WhatIf</span></span>
<span data-ttu-id="d4833-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4833-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4833-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4833-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4833-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4833-137">CommonParameters</span></span>
<span data-ttu-id="d4833-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4833-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4833-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d4833-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4833-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4833-140">INPUTS</span></span>

### <span data-ttu-id="d4833-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d4833-141">System.String</span></span>

### <span data-ttu-id="d4833-142">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d4833-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="d4833-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4833-143">OUTPUTS</span></span>

### <span data-ttu-id="d4833-144">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d4833-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d4833-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4833-145">NOTES</span></span>

## <span data-ttu-id="d4833-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4833-146">RELATED LINKS</span></span>