---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: a74edbec0051e3a77ab3ac10595f787dd45a2dfc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013287"
---
# <span data-ttu-id="98735-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="98735-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="98735-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98735-102">SYNOPSIS</span></span>
<span data-ttu-id="98735-103">Egy szolgáltatási végpont-házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="98735-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="98735-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98735-104">SYNTAX</span></span>

### <span data-ttu-id="98735-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98735-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98735-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98735-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98735-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="98735-107">DESCRIPTION</span></span>
<span data-ttu-id="98735-108">A **Get-AzServiceEndpointPolicy** parancsmag szolgáltatási végpont-házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="98735-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="98735-109">Példák</span><span class="sxs-lookup"><span data-stu-id="98735-109">EXAMPLES</span></span>

### <span data-ttu-id="98735-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="98735-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="98735-111">Ez a parancs a ServiceEndpointPolicy1 nevű, a ResourceGroup01 nevű erőforráscsoporthoz tartozó szolgáltatás-végponti házirendet kapja meg, és a $policy változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="98735-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="98735-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="98735-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="98735-113">Ez a parancs felsorolja a ResourceGroup01 nevű erőforráscsoport összes szolgáltatás-végpont-házirendjét, és a $policyList változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="98735-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="98735-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="98735-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="98735-115">Ez a parancs a "ServiceEndpointPolicy" kezdetű szolgáltatás-végponti házirendek listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="98735-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="98735-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98735-116">PARAMETERS</span></span>

### <span data-ttu-id="98735-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98735-117">-DefaultProfile</span></span>
<span data-ttu-id="98735-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98735-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98735-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98735-119">-Name</span></span>
<span data-ttu-id="98735-120">A szolgáltatás végpont-házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="98735-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="98735-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98735-121">-ResourceGroupName</span></span>
<span data-ttu-id="98735-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="98735-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="98735-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98735-123">-ResourceId</span></span>
<span data-ttu-id="98735-124">A szolgáltatás végpont-házirendjének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="98735-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98735-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98735-125">-Confirm</span></span>
<span data-ttu-id="98735-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98735-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98735-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98735-127">-WhatIf</span></span>
<span data-ttu-id="98735-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98735-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98735-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98735-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98735-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98735-130">CommonParameters</span></span>
<span data-ttu-id="98735-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98735-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98735-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="98735-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98735-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98735-133">INPUTS</span></span>

### <span data-ttu-id="98735-134">System. String</span><span class="sxs-lookup"><span data-stu-id="98735-134">System.String</span></span>

## <span data-ttu-id="98735-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98735-135">OUTPUTS</span></span>

### <span data-ttu-id="98735-136">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="98735-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="98735-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98735-137">NOTES</span></span>

## <span data-ttu-id="98735-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98735-138">RELATED LINKS</span></span>

[<span data-ttu-id="98735-139">Új – AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="98735-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="98735-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="98735-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="98735-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="98735-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
