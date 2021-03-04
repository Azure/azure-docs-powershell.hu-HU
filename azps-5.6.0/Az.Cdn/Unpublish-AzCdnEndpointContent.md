---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: 403c91802c70d7d5e6cfb844909dee1ca6956847
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927433"
---
# <span data-ttu-id="b29ea-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="b29ea-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="b29ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b29ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b29ea-103">CDN-végpont végleges véglegesen történő végleges véglegesen ürlése.</span><span class="sxs-lookup"><span data-stu-id="b29ea-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="b29ea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b29ea-104">SYNTAX</span></span>

### <span data-ttu-id="b29ea-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b29ea-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b29ea-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b29ea-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b29ea-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b29ea-107">DESCRIPTION</span></span>
<span data-ttu-id="b29ea-108">Az **Unpublish-AzCdnEndpointContent parancsmag** véglegesen véglegesen elvégz egy Azure Content Delivery Network (CDN) végpont tartalmát.</span><span class="sxs-lookup"><span data-stu-id="b29ea-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b29ea-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b29ea-109">EXAMPLES</span></span>

## <span data-ttu-id="b29ea-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b29ea-110">PARAMETERS</span></span>

### <span data-ttu-id="b29ea-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b29ea-111">-CdnEndpoint</span></span>
<span data-ttu-id="b29ea-112">A parancsmag véglegesként megadott végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b29ea-112">Specifies the endpoint that this cmdlet purges.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b29ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b29ea-113">-DefaultProfile</span></span>
<span data-ttu-id="b29ea-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b29ea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b29ea-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b29ea-115">-EndpointName</span></span>
<span data-ttu-id="b29ea-116">Annak a végpontnak a nevét adja meg, amelytől a parancsmag véglegesen végleges.</span><span class="sxs-lookup"><span data-stu-id="b29ea-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29ea-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b29ea-117">-PassThru</span></span>
<span data-ttu-id="b29ea-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="b29ea-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b29ea-119">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b29ea-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b29ea-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b29ea-120">-ProfileName</span></span>
<span data-ttu-id="b29ea-121">Annak a profilnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="b29ea-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29ea-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="b29ea-122">-PurgeContent</span></span>
<span data-ttu-id="b29ea-123">Annak a forráskiszolgálónak a relatív elérési útjai tömbét adja meg, amely a parancsmagot véglegesen véglegesen meghatározza.</span><span class="sxs-lookup"><span data-stu-id="b29ea-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29ea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b29ea-124">-ResourceGroupName</span></span>
<span data-ttu-id="b29ea-125">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="b29ea-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29ea-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b29ea-126">-Confirm</span></span>
<span data-ttu-id="b29ea-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b29ea-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29ea-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b29ea-128">-WhatIf</span></span>
<span data-ttu-id="b29ea-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b29ea-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b29ea-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b29ea-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29ea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29ea-131">CommonParameters</span></span>
<span data-ttu-id="b29ea-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b29ea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29ea-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b29ea-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29ea-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b29ea-134">INPUTS</span></span>

### <span data-ttu-id="b29ea-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b29ea-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="b29ea-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b29ea-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b29ea-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b29ea-137">OUTPUTS</span></span>

### <span data-ttu-id="b29ea-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b29ea-138">System.Boolean</span></span>

## <span data-ttu-id="b29ea-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b29ea-139">NOTES</span></span>

## <span data-ttu-id="b29ea-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b29ea-140">RELATED LINKS</span></span>

[<span data-ttu-id="b29ea-141">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="b29ea-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


