---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467438"
---
# <span data-ttu-id="c6821-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c6821-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="c6821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6821-102">SYNOPSIS</span></span>
<span data-ttu-id="c6821-103">Szolgáltatás végponti házirend-definícióját adja hozzá egy adott házirendhez.</span><span class="sxs-lookup"><span data-stu-id="c6821-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="c6821-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c6821-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6821-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c6821-105">DESCRIPTION</span></span>
<span data-ttu-id="c6821-106">Az **Add-AzServiceEndpointPolicyDefinition parancsmag** szolgáltatásvégpont-házirend-definíciót ad a házirendhez.</span><span class="sxs-lookup"><span data-stu-id="c6821-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="c6821-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c6821-107">EXAMPLES</span></span>

### <span data-ttu-id="c6821-108">1. példa: Szolgáltatás végponti házirend-definíciójának frissítése egy szolgáltatás végponti házirendben</span><span class="sxs-lookup"><span data-stu-id="c6821-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="c6821-109">Ez a parancs frissítette a szolgáltatás végponti házirend-definícióját ServiceEndpointPolicyDefinition1 névvel, a Microsoft.Storage szolgáltatással, a szolgáltatáserőforrás-előfizetésekkel/al1-al1- és az "Új definíció" leírással, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $policydef változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c6821-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="c6821-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6821-110">PARAMETERS</span></span>

### <span data-ttu-id="c6821-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6821-111">-DefaultProfile</span></span>
<span data-ttu-id="c6821-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6821-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6821-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c6821-113">-Description</span></span>
<span data-ttu-id="c6821-114">A definíció leírása</span><span class="sxs-lookup"><span data-stu-id="c6821-114">The description of the definition</span></span>

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

### <span data-ttu-id="c6821-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c6821-115">-Name</span></span>
<span data-ttu-id="c6821-116">A szolgáltatás végponti házirend-definíciójának neve</span><span class="sxs-lookup"><span data-stu-id="c6821-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="c6821-117">-Service</span><span class="sxs-lookup"><span data-stu-id="c6821-117">-Service</span></span>
<span data-ttu-id="c6821-118">A szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="c6821-118">Name of the service</span></span>

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

### <span data-ttu-id="c6821-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c6821-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="c6821-120">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c6821-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="c6821-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="c6821-121">-ServiceResource</span></span>
<span data-ttu-id="c6821-122">Szolgáltatáserőforrások listája</span><span class="sxs-lookup"><span data-stu-id="c6821-122">List of service resources</span></span>

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

### <span data-ttu-id="c6821-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6821-123">-Confirm</span></span>
<span data-ttu-id="c6821-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c6821-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6821-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6821-125">-WhatIf</span></span>
<span data-ttu-id="c6821-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c6821-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6821-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6821-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6821-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6821-128">CommonParameters</span></span>
<span data-ttu-id="c6821-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6821-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6821-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6821-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6821-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6821-131">INPUTS</span></span>

### <span data-ttu-id="c6821-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c6821-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="c6821-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6821-133">OUTPUTS</span></span>

### <span data-ttu-id="c6821-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c6821-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="c6821-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c6821-135">NOTES</span></span>

## <span data-ttu-id="c6821-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6821-136">RELATED LINKS</span></span>

[<span data-ttu-id="c6821-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c6821-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="c6821-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c6821-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="c6821-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c6821-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="c6821-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c6821-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
