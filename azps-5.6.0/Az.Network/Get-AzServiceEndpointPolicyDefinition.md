---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 554d3285c80370559bbedfb91430d2b6801a6f51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922362"
---
# <span data-ttu-id="a7e76-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a7e76-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="a7e76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7e76-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e76-103">Szolgáltatásvégpont-házirend-definíciót kap.</span><span class="sxs-lookup"><span data-stu-id="a7e76-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="a7e76-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a7e76-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7e76-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a7e76-105">DESCRIPTION</span></span>
<span data-ttu-id="a7e76-106">A **Get-AzServiceEndpointPolicyDefinition parancsmag** szolgáltatásvégpont-házirend-definíciót kap.</span><span class="sxs-lookup"><span data-stu-id="a7e76-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="a7e76-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a7e76-107">EXAMPLES</span></span>

### <span data-ttu-id="a7e76-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a7e76-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="a7e76-109">Ez a parancs a ServiceEndpointPolicyDefinition1 nevű szolgáltatás végponti házirend-definícióját kapja meg a ServiceEndpointPolicy $Policy a $policydef változóban.</span><span class="sxs-lookup"><span data-stu-id="a7e76-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="a7e76-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7e76-110">PARAMETERS</span></span>

### <span data-ttu-id="a7e76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e76-111">-DefaultProfile</span></span>
<span data-ttu-id="a7e76-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7e76-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7e76-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a7e76-113">-Name</span></span>
<span data-ttu-id="a7e76-114">A szolgáltatás végponti házirend-definíciójának neve</span><span class="sxs-lookup"><span data-stu-id="a7e76-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="a7e76-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a7e76-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="a7e76-116">A Szolgáltatás végponti házirend</span><span class="sxs-lookup"><span data-stu-id="a7e76-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="a7e76-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7e76-117">-Confirm</span></span>
<span data-ttu-id="a7e76-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a7e76-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7e76-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7e76-119">-WhatIf</span></span>
<span data-ttu-id="a7e76-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a7e76-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7e76-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a7e76-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7e76-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e76-122">CommonParameters</span></span>
<span data-ttu-id="a7e76-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7e76-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e76-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7e76-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e76-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7e76-125">INPUTS</span></span>

### <span data-ttu-id="a7e76-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a7e76-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="a7e76-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7e76-127">OUTPUTS</span></span>

### <span data-ttu-id="a7e76-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a7e76-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="a7e76-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a7e76-129">NOTES</span></span>

## <span data-ttu-id="a7e76-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7e76-130">RELATED LINKS</span></span>

[<span data-ttu-id="a7e76-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a7e76-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="a7e76-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a7e76-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="a7e76-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a7e76-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="a7e76-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a7e76-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
