---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: e1afa87d1ab21222987a4eeecf68a3786934ef57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367035"
---
# <span data-ttu-id="20e96-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="20e96-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="20e96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20e96-102">SYNOPSIS</span></span>
<span data-ttu-id="20e96-103">Leállítja a CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="20e96-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="20e96-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="20e96-104">SYNTAX</span></span>

### <span data-ttu-id="20e96-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="20e96-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20e96-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20e96-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20e96-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="20e96-107">DESCRIPTION</span></span>
<span data-ttu-id="20e96-108">A **Stop-AzCdnEndpoint** parancsmag leállítja az Azure Content Delivery Network (CDN) végpontot.</span><span class="sxs-lookup"><span data-stu-id="20e96-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="20e96-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="20e96-109">EXAMPLES</span></span>

## <span data-ttu-id="20e96-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20e96-110">PARAMETERS</span></span>

### <span data-ttu-id="20e96-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="20e96-111">-CdnEndpoint</span></span>
<span data-ttu-id="20e96-112">A parancsmag végpontobjektumát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="20e96-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="20e96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e96-113">-DefaultProfile</span></span>
<span data-ttu-id="20e96-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="20e96-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20e96-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="20e96-115">-EndpointName</span></span>
<span data-ttu-id="20e96-116">A parancsmag végpontjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="20e96-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="20e96-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20e96-117">-PassThru</span></span>
<span data-ttu-id="20e96-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="20e96-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="20e96-119">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="20e96-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="20e96-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="20e96-120">-ProfileName</span></span>
<span data-ttu-id="20e96-121">Annak a profilnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="20e96-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="20e96-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20e96-122">-ResourceGroupName</span></span>
<span data-ttu-id="20e96-123">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="20e96-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="20e96-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20e96-124">-Confirm</span></span>
<span data-ttu-id="20e96-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="20e96-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20e96-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20e96-126">-WhatIf</span></span>
<span data-ttu-id="20e96-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="20e96-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20e96-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20e96-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20e96-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e96-129">CommonParameters</span></span>
<span data-ttu-id="20e96-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20e96-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e96-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20e96-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e96-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20e96-132">INPUTS</span></span>

### <span data-ttu-id="20e96-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="20e96-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="20e96-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="20e96-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="20e96-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20e96-135">OUTPUTS</span></span>

### <span data-ttu-id="20e96-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="20e96-136">System.Boolean</span></span>

## <span data-ttu-id="20e96-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="20e96-137">NOTES</span></span>

## <span data-ttu-id="20e96-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20e96-138">RELATED LINKS</span></span>

[<span data-ttu-id="20e96-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="20e96-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="20e96-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="20e96-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="20e96-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="20e96-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="20e96-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="20e96-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="20e96-143">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="20e96-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


