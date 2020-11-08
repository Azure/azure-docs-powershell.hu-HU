---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024845"
---
# <span data-ttu-id="c0834-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="c0834-101">New-AzGallery</span></span>

## <span data-ttu-id="c0834-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0834-102">SYNOPSIS</span></span>
<span data-ttu-id="c0834-103">Gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="c0834-103">Create a gallery.</span></span>

## <span data-ttu-id="c0834-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0834-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0834-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0834-105">DESCRIPTION</span></span>
<span data-ttu-id="c0834-106">Gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="c0834-106">Create a gallery.</span></span>

## <span data-ttu-id="c0834-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c0834-107">EXAMPLES</span></span>

### <span data-ttu-id="c0834-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c0834-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="c0834-109">Gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="c0834-109">Create a gallery.</span></span>

## <span data-ttu-id="c0834-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0834-110">PARAMETERS</span></span>

### <span data-ttu-id="c0834-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0834-111">-AsJob</span></span>
<span data-ttu-id="c0834-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c0834-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0834-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0834-113">-DefaultProfile</span></span>
<span data-ttu-id="c0834-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0834-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0834-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c0834-115">-Description</span></span>
<span data-ttu-id="c0834-116">A gyűjtemény-erőforrás leírása.</span><span class="sxs-lookup"><span data-stu-id="c0834-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="c0834-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="c0834-117">-Location</span></span>
<span data-ttu-id="c0834-118">Erőforrás-hely</span><span class="sxs-lookup"><span data-stu-id="c0834-118">Resource location</span></span>

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

### <span data-ttu-id="c0834-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0834-119">-Name</span></span>
<span data-ttu-id="c0834-120">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="c0834-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="c0834-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0834-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0834-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c0834-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="c0834-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="c0834-123">-Tag</span></span>
<span data-ttu-id="c0834-124">Erőforrás-Címkék</span><span class="sxs-lookup"><span data-stu-id="c0834-124">Resource tags</span></span>

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

### <span data-ttu-id="c0834-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c0834-125">-Confirm</span></span>
<span data-ttu-id="c0834-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0834-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0834-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0834-127">-WhatIf</span></span>
<span data-ttu-id="c0834-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c0834-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0834-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0834-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0834-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0834-130">CommonParameters</span></span>
<span data-ttu-id="c0834-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0834-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0834-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c0834-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0834-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0834-133">INPUTS</span></span>

### <span data-ttu-id="c0834-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c0834-134">System.String</span></span>

### <span data-ttu-id="c0834-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c0834-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c0834-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0834-136">OUTPUTS</span></span>

### <span data-ttu-id="c0834-137">Microsoft. Azure. commands. számítási. Automation. models. galériában</span><span class="sxs-lookup"><span data-stu-id="c0834-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="c0834-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0834-138">NOTES</span></span>

## <span data-ttu-id="c0834-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0834-139">RELATED LINKS</span></span>
