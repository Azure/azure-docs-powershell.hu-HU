---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: d1a25b3e8466c691272f4c556fe728cbce47a718
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356009"
---
# <span data-ttu-id="c07cd-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="c07cd-101">New-AzGallery</span></span>

## <span data-ttu-id="c07cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c07cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c07cd-103">Gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="c07cd-103">Create a gallery.</span></span>

## <span data-ttu-id="c07cd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c07cd-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c07cd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c07cd-105">DESCRIPTION</span></span>
<span data-ttu-id="c07cd-106">Gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="c07cd-106">Create a gallery.</span></span>

## <span data-ttu-id="c07cd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c07cd-107">EXAMPLES</span></span>

### <span data-ttu-id="c07cd-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c07cd-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="c07cd-109">Gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="c07cd-109">Create a gallery.</span></span>

## <span data-ttu-id="c07cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c07cd-110">PARAMETERS</span></span>

### <span data-ttu-id="c07cd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c07cd-111">-AsJob</span></span>
<span data-ttu-id="c07cd-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c07cd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c07cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c07cd-113">-DefaultProfile</span></span>
<span data-ttu-id="c07cd-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c07cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c07cd-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c07cd-115">-Description</span></span>
<span data-ttu-id="c07cd-116">A gyűjtemény típusú erőforrás leírása.</span><span class="sxs-lookup"><span data-stu-id="c07cd-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="c07cd-117">-Location</span><span class="sxs-lookup"><span data-stu-id="c07cd-117">-Location</span></span>
<span data-ttu-id="c07cd-118">Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="c07cd-118">Resource location</span></span>

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

### <span data-ttu-id="c07cd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c07cd-119">-Name</span></span>
<span data-ttu-id="c07cd-120">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="c07cd-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="c07cd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c07cd-121">-ResourceGroupName</span></span>
<span data-ttu-id="c07cd-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c07cd-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="c07cd-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="c07cd-123">-Tag</span></span>
<span data-ttu-id="c07cd-124">Erőforráscímkék</span><span class="sxs-lookup"><span data-stu-id="c07cd-124">Resource tags</span></span>

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

### <span data-ttu-id="c07cd-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c07cd-125">-Confirm</span></span>
<span data-ttu-id="c07cd-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c07cd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c07cd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c07cd-127">-WhatIf</span></span>
<span data-ttu-id="c07cd-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c07cd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c07cd-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c07cd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c07cd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07cd-130">CommonParameters</span></span>
<span data-ttu-id="c07cd-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c07cd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07cd-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c07cd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07cd-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c07cd-133">INPUTS</span></span>

### <span data-ttu-id="c07cd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c07cd-134">System.String</span></span>

### <span data-ttu-id="c07cd-135">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c07cd-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c07cd-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c07cd-136">OUTPUTS</span></span>

### <span data-ttu-id="c07cd-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="c07cd-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="c07cd-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c07cd-138">NOTES</span></span>

## <span data-ttu-id="c07cd-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c07cd-139">RELATED LINKS</span></span>
