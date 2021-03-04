---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: a6b5a471b4f04ce36d20b72502894b41b8dade4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943105"
---
# <span data-ttu-id="52926-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52926-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="52926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52926-102">SYNOPSIS</span></span>
<span data-ttu-id="52926-103">CdN-végpont indítása.</span><span class="sxs-lookup"><span data-stu-id="52926-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="52926-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="52926-104">SYNTAX</span></span>

### <span data-ttu-id="52926-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52926-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52926-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52926-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52926-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="52926-107">DESCRIPTION</span></span>
<span data-ttu-id="52926-108">A **Start-AzCdnEndpoint** parancsmag elindít egy Azure Content Delivery Network (CDN) végpontot.</span><span class="sxs-lookup"><span data-stu-id="52926-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="52926-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="52926-109">EXAMPLES</span></span>

## <span data-ttu-id="52926-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52926-110">PARAMETERS</span></span>

### <span data-ttu-id="52926-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52926-111">-CdnEndpoint</span></span>
<span data-ttu-id="52926-112">A parancsmag által elindított végpontot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="52926-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="52926-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52926-113">-DefaultProfile</span></span>
<span data-ttu-id="52926-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="52926-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52926-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="52926-115">-EndpointName</span></span>
<span data-ttu-id="52926-116">A parancsmag által elindított végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52926-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="52926-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52926-117">-PassThru</span></span>
<span data-ttu-id="52926-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="52926-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52926-119">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="52926-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52926-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="52926-120">-ProfileName</span></span>
<span data-ttu-id="52926-121">Annak a profilnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="52926-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="52926-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52926-122">-ResourceGroupName</span></span>
<span data-ttu-id="52926-123">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="52926-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="52926-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52926-124">-Confirm</span></span>
<span data-ttu-id="52926-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="52926-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52926-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52926-126">-WhatIf</span></span>
<span data-ttu-id="52926-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="52926-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52926-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52926-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52926-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52926-129">CommonParameters</span></span>
<span data-ttu-id="52926-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52926-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52926-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52926-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52926-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52926-132">INPUTS</span></span>

### <span data-ttu-id="52926-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="52926-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="52926-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="52926-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="52926-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52926-135">OUTPUTS</span></span>

### <span data-ttu-id="52926-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52926-136">System.Boolean</span></span>

## <span data-ttu-id="52926-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="52926-137">NOTES</span></span>

## <span data-ttu-id="52926-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52926-138">RELATED LINKS</span></span>

[<span data-ttu-id="52926-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52926-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="52926-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52926-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="52926-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52926-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="52926-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52926-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="52926-143">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="52926-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


