---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012827"
---
# <span data-ttu-id="69c27-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="69c27-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="69c27-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69c27-102">SYNOPSIS</span></span>
<span data-ttu-id="69c27-103">Beindít egy CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="69c27-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="69c27-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69c27-104">SYNTAX</span></span>

### <span data-ttu-id="69c27-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69c27-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69c27-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69c27-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69c27-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="69c27-107">DESCRIPTION</span></span>
<span data-ttu-id="69c27-108">A **Start-AzCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját indítja el.</span><span class="sxs-lookup"><span data-stu-id="69c27-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="69c27-109">Példák</span><span class="sxs-lookup"><span data-stu-id="69c27-109">EXAMPLES</span></span>

## <span data-ttu-id="69c27-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69c27-110">PARAMETERS</span></span>

### <span data-ttu-id="69c27-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="69c27-111">-CdnEndpoint</span></span>
<span data-ttu-id="69c27-112">A parancsmag kezdetét megadó végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="69c27-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="69c27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c27-113">-DefaultProfile</span></span>
<span data-ttu-id="69c27-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="69c27-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69c27-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="69c27-115">-EndpointName</span></span>
<span data-ttu-id="69c27-116">Annak a végpontnak a nevét adja meg, amelyre a parancsmag indul.</span><span class="sxs-lookup"><span data-stu-id="69c27-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="69c27-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69c27-117">-PassThru</span></span>
<span data-ttu-id="69c27-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="69c27-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69c27-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="69c27-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="69c27-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="69c27-120">-ProfileName</span></span>
<span data-ttu-id="69c27-121">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="69c27-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="69c27-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c27-122">-ResourceGroupName</span></span>
<span data-ttu-id="69c27-123">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="69c27-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="69c27-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69c27-124">-Confirm</span></span>
<span data-ttu-id="69c27-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69c27-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69c27-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69c27-126">-WhatIf</span></span>
<span data-ttu-id="69c27-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69c27-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69c27-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69c27-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69c27-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c27-129">CommonParameters</span></span>
<span data-ttu-id="69c27-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69c27-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c27-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="69c27-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c27-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69c27-132">INPUTS</span></span>

### <span data-ttu-id="69c27-133">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="69c27-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="69c27-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="69c27-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="69c27-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69c27-135">OUTPUTS</span></span>

### <span data-ttu-id="69c27-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69c27-136">System.Boolean</span></span>

## <span data-ttu-id="69c27-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69c27-137">NOTES</span></span>

## <span data-ttu-id="69c27-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69c27-138">RELATED LINKS</span></span>

[<span data-ttu-id="69c27-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="69c27-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="69c27-140">Új – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="69c27-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="69c27-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="69c27-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="69c27-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="69c27-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="69c27-143">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="69c27-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


