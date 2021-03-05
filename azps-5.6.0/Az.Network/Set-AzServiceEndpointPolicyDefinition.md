---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: bc68a57437bae2af10b5ee39221459aebf82a2df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010294"
---
# <span data-ttu-id="49ec7-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="49ec7-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="49ec7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="49ec7-103">Frissíti a szolgáltatás végponti házirend-definícióját.</span><span class="sxs-lookup"><span data-stu-id="49ec7-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="49ec7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49ec7-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ec7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49ec7-105">DESCRIPTION</span></span>
<span data-ttu-id="49ec7-106">A **Set-AzServiceEndpointPolicyDefinition parancsmag** szolgáltatási végponti házirend-definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="49ec7-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="49ec7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49ec7-107">EXAMPLES</span></span>

### <span data-ttu-id="49ec7-108">1. példa: Szolgáltatás végponti házirend-definíciójának frissítése egy szolgáltatás végponti házirendben</span><span class="sxs-lookup"><span data-stu-id="49ec7-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="49ec7-109">Ez a parancs frissíti a Házirenddef1 nevű szolgáltatásvégpont-házirend-definíciót az objektumobjektum által definiált szolgáltatásvégpont-házirendben $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="49ec7-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="49ec7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49ec7-110">PARAMETERS</span></span>

### <span data-ttu-id="49ec7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ec7-111">-DefaultProfile</span></span>
<span data-ttu-id="49ec7-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49ec7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49ec7-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="49ec7-113">-Description</span></span>
<span data-ttu-id="49ec7-114">A definíció leírása</span><span class="sxs-lookup"><span data-stu-id="49ec7-114">The description of the definition</span></span>

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

### <span data-ttu-id="49ec7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="49ec7-115">-Name</span></span>
<span data-ttu-id="49ec7-116">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="49ec7-116">The name of the rule</span></span>

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

### <span data-ttu-id="49ec7-117">-Service</span><span class="sxs-lookup"><span data-stu-id="49ec7-117">-Service</span></span>
<span data-ttu-id="49ec7-118">A szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="49ec7-118">Name of the service</span></span>

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

### <span data-ttu-id="49ec7-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="49ec7-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="49ec7-120">The NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49ec7-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="49ec7-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="49ec7-121">-ServiceResource</span></span>
<span data-ttu-id="49ec7-122">Szolgáltatáserőforrások listája</span><span class="sxs-lookup"><span data-stu-id="49ec7-122">List of service resources</span></span>

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

### <span data-ttu-id="49ec7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49ec7-123">-Confirm</span></span>
<span data-ttu-id="49ec7-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="49ec7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49ec7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ec7-125">-WhatIf</span></span>
<span data-ttu-id="49ec7-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="49ec7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49ec7-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49ec7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49ec7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ec7-128">CommonParameters</span></span>
<span data-ttu-id="49ec7-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ec7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ec7-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ec7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ec7-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49ec7-131">INPUTS</span></span>

### <span data-ttu-id="49ec7-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="49ec7-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="49ec7-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49ec7-133">OUTPUTS</span></span>

### <span data-ttu-id="49ec7-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="49ec7-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="49ec7-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49ec7-135">NOTES</span></span>

## <span data-ttu-id="49ec7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49ec7-136">RELATED LINKS</span></span>

[<span data-ttu-id="49ec7-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="49ec7-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="49ec7-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="49ec7-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="49ec7-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="49ec7-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="49ec7-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="49ec7-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
