---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
ms.openlocfilehash: 5d8ed5a26e141d0ae8d6eb7494a76d8c53590d29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679588"
---
# <span data-ttu-id="35225-101">Update-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="35225-101">Update-AzureRmGallery</span></span>

## <span data-ttu-id="35225-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35225-102">SYNOPSIS</span></span>
<span data-ttu-id="35225-103">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="35225-103">Update a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35225-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35225-104">SYNTAX</span></span>

### <span data-ttu-id="35225-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="35225-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35225-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="35225-106">ResourceIdParameter</span></span>
```
Update-AzureRmGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35225-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="35225-107">ObjectParameter</span></span>
```
Update-AzureRmGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35225-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="35225-108">DESCRIPTION</span></span>
<span data-ttu-id="35225-109">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="35225-109">Update a gallery.</span></span>

## <span data-ttu-id="35225-110">Példák</span><span class="sxs-lookup"><span data-stu-id="35225-110">EXAMPLES</span></span>

### <span data-ttu-id="35225-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="35225-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="35225-112">Gyűjtemény frissítése</span><span class="sxs-lookup"><span data-stu-id="35225-112">Update a gallery.</span></span>

## <span data-ttu-id="35225-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35225-113">PARAMETERS</span></span>

### <span data-ttu-id="35225-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35225-114">-AsJob</span></span>
<span data-ttu-id="35225-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="35225-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35225-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35225-116">-DefaultProfile</span></span>
<span data-ttu-id="35225-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35225-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35225-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="35225-118">-Description</span></span>
<span data-ttu-id="35225-119">A gyűjtemény-erőforrás leírása.</span><span class="sxs-lookup"><span data-stu-id="35225-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="35225-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35225-120">-InputObject</span></span>
<span data-ttu-id="35225-121">A PS-gyűjtemény objektuma.</span><span class="sxs-lookup"><span data-stu-id="35225-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="35225-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="35225-122">-Name</span></span>
<span data-ttu-id="35225-123">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="35225-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="35225-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35225-124">-ResourceGroupName</span></span>
<span data-ttu-id="35225-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="35225-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="35225-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35225-126">-ResourceId</span></span>
<span data-ttu-id="35225-127">A gyűjtemény erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="35225-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="35225-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="35225-128">-Tag</span></span>
<span data-ttu-id="35225-129">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="35225-129">Resource tags</span></span>

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

### <span data-ttu-id="35225-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="35225-130">-Confirm</span></span>
<span data-ttu-id="35225-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="35225-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35225-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35225-132">-WhatIf</span></span>
<span data-ttu-id="35225-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="35225-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35225-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35225-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35225-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35225-135">CommonParameters</span></span>
<span data-ttu-id="35225-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35225-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35225-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35225-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35225-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35225-138">INPUTS</span></span>

### <span data-ttu-id="35225-139">System. String</span><span class="sxs-lookup"><span data-stu-id="35225-139">System.String</span></span>

### <span data-ttu-id="35225-140">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="35225-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="35225-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="35225-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="35225-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35225-142">OUTPUTS</span></span>

### <span data-ttu-id="35225-143">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="35225-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="35225-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35225-144">NOTES</span></span>

## <span data-ttu-id="35225-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35225-145">RELATED LINKS</span></span>
