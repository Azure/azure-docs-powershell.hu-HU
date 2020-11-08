---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186392"
---
# <span data-ttu-id="69973-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="69973-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="69973-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69973-102">SYNOPSIS</span></span>
<span data-ttu-id="69973-103">A szolgáltatás végpont-házirendjének definíciójának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="69973-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="69973-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69973-104">SYNTAX</span></span>

### <span data-ttu-id="69973-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69973-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69973-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69973-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69973-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69973-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69973-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="69973-108">DESCRIPTION</span></span>
<span data-ttu-id="69973-109">A **Remove-AzServiceEndpointPolicy** parancsmag eltávolítja a szolgáltatási végpontok házirendjét.</span><span class="sxs-lookup"><span data-stu-id="69973-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="69973-110">Példák</span><span class="sxs-lookup"><span data-stu-id="69973-110">EXAMPLES</span></span>

### <span data-ttu-id="69973-111">1. példa: a szolgáltatás végpont-házirendjének eltávolítása név használatával</span><span class="sxs-lookup"><span data-stu-id="69973-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="69973-112">Ez a parancs eltávolítja a szolgáltatás végpontjának házirendjét a név PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="69973-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="69973-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69973-113">PARAMETERS</span></span>

### <span data-ttu-id="69973-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69973-114">-DefaultProfile</span></span>
<span data-ttu-id="69973-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69973-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69973-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69973-116">-InputObject</span></span>
<span data-ttu-id="69973-117">A szolgáltatás Endpoint Policy definition objektuma.</span><span class="sxs-lookup"><span data-stu-id="69973-117">The service endpoint policy definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69973-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69973-118">-Name</span></span>
<span data-ttu-id="69973-119">A szolgáltatás végpont-definíciójának neve</span><span class="sxs-lookup"><span data-stu-id="69973-119">The name of the service endpoint definition</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69973-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69973-120">-ResourceId</span></span>
<span data-ttu-id="69973-121">A szolgáltatás végpont-definíciójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="69973-121">The ID of the service endpoint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69973-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="69973-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="69973-123">A ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="69973-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="69973-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69973-124">-Confirm</span></span>
<span data-ttu-id="69973-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69973-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69973-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69973-126">-WhatIf</span></span>
<span data-ttu-id="69973-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69973-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69973-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69973-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69973-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69973-129">CommonParameters</span></span>
<span data-ttu-id="69973-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69973-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69973-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69973-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69973-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69973-132">INPUTS</span></span>

### <span data-ttu-id="69973-133">System. String</span><span class="sxs-lookup"><span data-stu-id="69973-133">System.String</span></span>

### <span data-ttu-id="69973-134">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="69973-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="69973-135">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="69973-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="69973-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69973-136">OUTPUTS</span></span>

### <span data-ttu-id="69973-137">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="69973-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="69973-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69973-138">NOTES</span></span>

## <span data-ttu-id="69973-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69973-139">RELATED LINKS</span></span>

[<span data-ttu-id="69973-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="69973-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="69973-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="69973-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="69973-142">Új – AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="69973-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="69973-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="69973-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
