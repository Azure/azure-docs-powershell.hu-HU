---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: 6a5a0925967895514de8b7e5294c81571b1cbaba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667557"
---
# <span data-ttu-id="935b2-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="935b2-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="935b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="935b2-102">SYNOPSIS</span></span>
<span data-ttu-id="935b2-103">Törli a CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="935b2-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="935b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="935b2-104">SYNTAX</span></span>

### <span data-ttu-id="935b2-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="935b2-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="935b2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="935b2-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="935b2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="935b2-107">DESCRIPTION</span></span>
<span data-ttu-id="935b2-108">A **Közzététel nélküli AzCdnEndpointContent** parancsmag kiüríti a tartalmat egy Azure Content Delivery Network (CDN) végpontról.</span><span class="sxs-lookup"><span data-stu-id="935b2-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="935b2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="935b2-109">EXAMPLES</span></span>

## <span data-ttu-id="935b2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="935b2-110">PARAMETERS</span></span>

### <span data-ttu-id="935b2-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="935b2-111">-CdnEndpoint</span></span>
<span data-ttu-id="935b2-112">A parancsmagot tartalmazó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="935b2-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="935b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935b2-113">-DefaultProfile</span></span>
<span data-ttu-id="935b2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="935b2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="935b2-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="935b2-115">-EndpointName</span></span>
<span data-ttu-id="935b2-116">Annak a végpontnak a nevét adja meg, amely a parancsmagot törli.</span><span class="sxs-lookup"><span data-stu-id="935b2-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="935b2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="935b2-117">-PassThru</span></span>
<span data-ttu-id="935b2-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="935b2-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="935b2-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="935b2-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="935b2-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="935b2-120">-ProfileName</span></span>
<span data-ttu-id="935b2-121">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="935b2-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="935b2-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="935b2-122">-PurgeContent</span></span>
<span data-ttu-id="935b2-123">A forrás-kiszolgálón található tartalom relatív elérési útjának tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="935b2-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="935b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="935b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="935b2-125">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="935b2-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="935b2-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="935b2-126">-Confirm</span></span>
<span data-ttu-id="935b2-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="935b2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="935b2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="935b2-128">-WhatIf</span></span>
<span data-ttu-id="935b2-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="935b2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="935b2-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="935b2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="935b2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935b2-131">CommonParameters</span></span>
<span data-ttu-id="935b2-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="935b2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935b2-133">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="935b2-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935b2-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="935b2-134">INPUTS</span></span>

### <span data-ttu-id="935b2-135">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="935b2-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="935b2-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="935b2-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="935b2-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="935b2-137">OUTPUTS</span></span>

### <span data-ttu-id="935b2-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="935b2-138">System.Boolean</span></span>

## <span data-ttu-id="935b2-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="935b2-139">NOTES</span></span>

## <span data-ttu-id="935b2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="935b2-140">RELATED LINKS</span></span>

[<span data-ttu-id="935b2-141">Közzététel – AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="935b2-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


