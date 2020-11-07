---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGallery.md
ms.openlocfilehash: bb743768654dcaeec9a39e7b590abe71b155cc17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680398"
---
# <span data-ttu-id="43622-101">New-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="43622-101">New-AzureRmGallery</span></span>

## <span data-ttu-id="43622-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43622-102">SYNOPSIS</span></span>
<span data-ttu-id="43622-103">Gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="43622-103">Create a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43622-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43622-104">SYNTAX</span></span>

```
New-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43622-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="43622-105">DESCRIPTION</span></span>
<span data-ttu-id="43622-106">Gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="43622-106">Create a gallery.</span></span>

## <span data-ttu-id="43622-107">Példák</span><span class="sxs-lookup"><span data-stu-id="43622-107">EXAMPLES</span></span>

### <span data-ttu-id="43622-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="43622-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="43622-109">Gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="43622-109">Create a gallery.</span></span>

## <span data-ttu-id="43622-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43622-110">PARAMETERS</span></span>

### <span data-ttu-id="43622-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43622-111">-AsJob</span></span>
<span data-ttu-id="43622-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="43622-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43622-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43622-113">-DefaultProfile</span></span>
<span data-ttu-id="43622-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43622-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43622-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="43622-115">-Description</span></span>
<span data-ttu-id="43622-116">A gyűjtemény-erőforrás leírása.</span><span class="sxs-lookup"><span data-stu-id="43622-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="43622-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="43622-117">-Location</span></span>
<span data-ttu-id="43622-118">Erőforrás-hely</span><span class="sxs-lookup"><span data-stu-id="43622-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43622-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43622-119">-Name</span></span>
<span data-ttu-id="43622-120">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="43622-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43622-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43622-121">-ResourceGroupName</span></span>
<span data-ttu-id="43622-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="43622-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43622-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="43622-123">-Tag</span></span>
<span data-ttu-id="43622-124">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="43622-124">Resource tags</span></span>

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

### <span data-ttu-id="43622-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43622-125">-Confirm</span></span>
<span data-ttu-id="43622-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43622-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43622-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43622-127">-WhatIf</span></span>
<span data-ttu-id="43622-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43622-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43622-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43622-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43622-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43622-130">CommonParameters</span></span>
<span data-ttu-id="43622-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43622-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43622-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43622-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43622-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43622-133">INPUTS</span></span>

### <span data-ttu-id="43622-134">System. String</span><span class="sxs-lookup"><span data-stu-id="43622-134">System.String</span></span>

### <span data-ttu-id="43622-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="43622-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="43622-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43622-136">OUTPUTS</span></span>

### <span data-ttu-id="43622-137">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="43622-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="43622-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43622-138">NOTES</span></span>

## <span data-ttu-id="43622-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43622-139">RELATED LINKS</span></span>
