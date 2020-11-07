---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3677b580629360a9f38d808af8df9ec0694bcc61
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670688"
---
# <span data-ttu-id="b9aef-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b9aef-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="b9aef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9aef-102">SYNOPSIS</span></span>
<span data-ttu-id="b9aef-103">A szolgáltatás végpont-házirendjének definícióját hozzáadja egy adott házirendhez.</span><span class="sxs-lookup"><span data-stu-id="b9aef-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="b9aef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9aef-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9aef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9aef-105">DESCRIPTION</span></span>
<span data-ttu-id="b9aef-106">A **Add-AzServiceEndpointPolicyDefinition** parancsmag szolgáltatási végpont házirend-definícióját adja hozzá a házirendhez.</span><span class="sxs-lookup"><span data-stu-id="b9aef-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="b9aef-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b9aef-107">EXAMPLES</span></span>

### <span data-ttu-id="b9aef-108">1. példa: a szolgáltatás végpont-házirendjének definícióját frissíti egy szolgáltatási végpont-házirendben</span><span class="sxs-lookup"><span data-stu-id="b9aef-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="b9aef-109">Ez a parancs frissítette a szolgáltatás végpontjának házirend-definícióját a name ServiceEndpointPolicyDefinition1, a Service Microsoft. Storage, a Service Resources-előfizetés/sub1 és a Description (új definíció) című témakörben, amely a ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $policydef változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b9aef-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="b9aef-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9aef-110">PARAMETERS</span></span>

### <span data-ttu-id="b9aef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9aef-111">-DefaultProfile</span></span>
<span data-ttu-id="b9aef-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9aef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9aef-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b9aef-113">-Description</span></span>
<span data-ttu-id="b9aef-114">A definíció leírása</span><span class="sxs-lookup"><span data-stu-id="b9aef-114">The description of the definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9aef-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9aef-115">-Name</span></span>
<span data-ttu-id="b9aef-116">A szolgáltatás végpontjának házirend-definíciójának neve</span><span class="sxs-lookup"><span data-stu-id="b9aef-116">The name of the service endpoint policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9aef-117">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="b9aef-117">-Service</span></span>
<span data-ttu-id="b9aef-118">A szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="b9aef-118">Name of the service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9aef-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b9aef-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="b9aef-120">A ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b9aef-120">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9aef-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="b9aef-121">-ServiceResource</span></span>
<span data-ttu-id="b9aef-122">A szolgáltatási erőforrások listája</span><span class="sxs-lookup"><span data-stu-id="b9aef-122">List of service resources</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9aef-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9aef-123">-Confirm</span></span>
<span data-ttu-id="b9aef-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9aef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9aef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9aef-125">-WhatIf</span></span>
<span data-ttu-id="b9aef-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9aef-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9aef-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9aef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9aef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9aef-128">CommonParameters</span></span>
<span data-ttu-id="b9aef-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9aef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9aef-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9aef-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9aef-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9aef-131">INPUTS</span></span>

### <span data-ttu-id="b9aef-132">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b9aef-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b9aef-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9aef-133">OUTPUTS</span></span>

### <span data-ttu-id="b9aef-134">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b9aef-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b9aef-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9aef-135">NOTES</span></span>

## <span data-ttu-id="b9aef-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9aef-136">RELATED LINKS</span></span>

[<span data-ttu-id="b9aef-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b9aef-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b9aef-138">Új – AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b9aef-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b9aef-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b9aef-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b9aef-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b9aef-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
