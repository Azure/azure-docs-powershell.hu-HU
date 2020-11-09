---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 164fc5edb4bac3b90debde0aaf6205c719f5c95c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302075"
---
# <span data-ttu-id="24a9e-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="24a9e-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="24a9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="24a9e-103">A szolgáltatás végpont-házirendjének definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="24a9e-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="24a9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24a9e-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24a9e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="24a9e-105">DESCRIPTION</span></span>
<span data-ttu-id="24a9e-106">A **Get-AzServiceEndpointPolicyDefinition** parancsmag szolgáltatási végpont házirend-definícióját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="24a9e-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="24a9e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="24a9e-107">EXAMPLES</span></span>

### <span data-ttu-id="24a9e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="24a9e-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="24a9e-109">Ez a parancs beolvassa a ServiceEndpointPolicyDefinition1-ban a ServiceEndpointPolicy $Policy nevű szolgáltatás végpont-házirendjének definícióját $policydef változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="24a9e-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="24a9e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24a9e-110">PARAMETERS</span></span>

### <span data-ttu-id="24a9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a9e-111">-DefaultProfile</span></span>
<span data-ttu-id="24a9e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24a9e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24a9e-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24a9e-113">-Name</span></span>
<span data-ttu-id="24a9e-114">A szolgáltatás végpontjának házirend-definíciójának neve</span><span class="sxs-lookup"><span data-stu-id="24a9e-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="24a9e-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="24a9e-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="24a9e-116">A szolgáltatás végpontjának házirendje</span><span class="sxs-lookup"><span data-stu-id="24a9e-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="24a9e-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24a9e-117">-Confirm</span></span>
<span data-ttu-id="24a9e-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24a9e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24a9e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24a9e-119">-WhatIf</span></span>
<span data-ttu-id="24a9e-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24a9e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24a9e-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24a9e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24a9e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a9e-122">CommonParameters</span></span>
<span data-ttu-id="24a9e-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24a9e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a9e-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="24a9e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a9e-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a9e-125">INPUTS</span></span>

### <span data-ttu-id="24a9e-126">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="24a9e-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="24a9e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a9e-127">OUTPUTS</span></span>

### <span data-ttu-id="24a9e-128">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="24a9e-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="24a9e-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24a9e-129">NOTES</span></span>

## <span data-ttu-id="24a9e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24a9e-130">RELATED LINKS</span></span>

[<span data-ttu-id="24a9e-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="24a9e-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="24a9e-132">Új – AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="24a9e-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="24a9e-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="24a9e-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="24a9e-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="24a9e-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
