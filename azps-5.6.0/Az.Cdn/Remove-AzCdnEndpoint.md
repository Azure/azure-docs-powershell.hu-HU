---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: e6c45f74f149cb2c087419a10f3e31cdfeb26610
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922114"
---
# <span data-ttu-id="288de-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="288de-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="288de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="288de-102">SYNOPSIS</span></span>
<span data-ttu-id="288de-103">Eltávolít egy CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="288de-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="288de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="288de-104">SYNTAX</span></span>

### <span data-ttu-id="288de-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="288de-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="288de-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="288de-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="288de-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="288de-107">DESCRIPTION</span></span>
<span data-ttu-id="288de-108">A **Remove-AzCdnEndpoint** parancsmag eltávolítja az Azure Content Delivery Network (CDN) végpontját.</span><span class="sxs-lookup"><span data-stu-id="288de-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="288de-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="288de-109">EXAMPLES</span></span>

## <span data-ttu-id="288de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="288de-110">PARAMETERS</span></span>

### <span data-ttu-id="288de-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="288de-111">-CdnEndpoint</span></span>
<span data-ttu-id="288de-112">A parancsmag által eltávolított végpontot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="288de-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="288de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="288de-113">-DefaultProfile</span></span>
<span data-ttu-id="288de-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="288de-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="288de-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="288de-115">-EndpointName</span></span>
<span data-ttu-id="288de-116">Annak a végpontnak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="288de-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="288de-117">-Force</span><span class="sxs-lookup"><span data-stu-id="288de-117">-Force</span></span>
<span data-ttu-id="288de-118">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="288de-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="288de-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="288de-119">-PassThru</span></span>
<span data-ttu-id="288de-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="288de-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="288de-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="288de-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="288de-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="288de-122">-ProfileName</span></span>
<span data-ttu-id="288de-123">Annak a profilnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="288de-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="288de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="288de-124">-ResourceGroupName</span></span>
<span data-ttu-id="288de-125">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="288de-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="288de-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="288de-126">-Confirm</span></span>
<span data-ttu-id="288de-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="288de-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="288de-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="288de-128">-WhatIf</span></span>
<span data-ttu-id="288de-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="288de-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="288de-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="288de-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="288de-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288de-131">CommonParameters</span></span>
<span data-ttu-id="288de-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="288de-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288de-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="288de-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288de-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="288de-134">INPUTS</span></span>

### <span data-ttu-id="288de-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="288de-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="288de-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="288de-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="288de-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="288de-137">OUTPUTS</span></span>

### <span data-ttu-id="288de-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="288de-138">System.Boolean</span></span>

## <span data-ttu-id="288de-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="288de-139">NOTES</span></span>

## <span data-ttu-id="288de-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="288de-140">RELATED LINKS</span></span>

[<span data-ttu-id="288de-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="288de-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="288de-142">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="288de-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="288de-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="288de-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="288de-144">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="288de-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="288de-145">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="288de-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


