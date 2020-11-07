---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847469"
---
# <span data-ttu-id="675dc-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="675dc-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="675dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="675dc-102">SYNOPSIS</span></span>
<span data-ttu-id="675dc-103">Frissíti a szolgáltatás végpont-házirendjének definícióját.</span><span class="sxs-lookup"><span data-stu-id="675dc-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="675dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="675dc-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="675dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="675dc-105">DESCRIPTION</span></span>
<span data-ttu-id="675dc-106">A **set-AzServiceEndpointPolicyDefinition** parancsmag szolgáltatás-végponti házirend-definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="675dc-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="675dc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="675dc-107">EXAMPLES</span></span>

### <span data-ttu-id="675dc-108">1. példa: a szolgáltatás végpont-házirendjének definícióját frissíti egy szolgáltatási végpont-házirendben</span><span class="sxs-lookup"><span data-stu-id="675dc-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="675dc-109">Ez a parancs frissíti az objektum $ServiceEndpointPolicy által definiált szolgáltatási végpont házirendben a Policydef1 nevű szolgáltatási végpont házirend-definícióját.</span><span class="sxs-lookup"><span data-stu-id="675dc-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="675dc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="675dc-110">PARAMETERS</span></span>

### <span data-ttu-id="675dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="675dc-111">-DefaultProfile</span></span>
<span data-ttu-id="675dc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="675dc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="675dc-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="675dc-113">-Description</span></span>
<span data-ttu-id="675dc-114">A definíció leírása</span><span class="sxs-lookup"><span data-stu-id="675dc-114">The description of the definition</span></span>

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

### <span data-ttu-id="675dc-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="675dc-115">-Name</span></span>
<span data-ttu-id="675dc-116">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="675dc-116">The name of the rule</span></span>

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

### <span data-ttu-id="675dc-117">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="675dc-117">-Service</span></span>
<span data-ttu-id="675dc-118">A szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="675dc-118">Name of the service</span></span>

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

### <span data-ttu-id="675dc-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="675dc-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="675dc-120">A NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="675dc-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="675dc-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="675dc-121">-ServiceResource</span></span>
<span data-ttu-id="675dc-122">A szolgáltatási erőforrások listája</span><span class="sxs-lookup"><span data-stu-id="675dc-122">List of service resources</span></span>

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

### <span data-ttu-id="675dc-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="675dc-123">-Confirm</span></span>
<span data-ttu-id="675dc-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="675dc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="675dc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="675dc-125">-WhatIf</span></span>
<span data-ttu-id="675dc-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="675dc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="675dc-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="675dc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="675dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="675dc-128">CommonParameters</span></span>
<span data-ttu-id="675dc-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="675dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="675dc-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="675dc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="675dc-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="675dc-131">INPUTS</span></span>

### <span data-ttu-id="675dc-132">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="675dc-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="675dc-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="675dc-133">OUTPUTS</span></span>

### <span data-ttu-id="675dc-134">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="675dc-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="675dc-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="675dc-135">NOTES</span></span>

## <span data-ttu-id="675dc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="675dc-136">RELATED LINKS</span></span>

[<span data-ttu-id="675dc-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="675dc-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="675dc-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="675dc-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="675dc-139">Új – AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="675dc-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="675dc-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="675dc-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)