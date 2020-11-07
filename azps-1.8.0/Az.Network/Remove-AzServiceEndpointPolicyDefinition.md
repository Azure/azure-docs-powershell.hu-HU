---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: c907c60619f5a0a2fc5f0620f086ba0b99ca62ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670114"
---
# <span data-ttu-id="b79cc-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b79cc-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="b79cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b79cc-102">SYNOPSIS</span></span>
<span data-ttu-id="b79cc-103">A szolgáltatás végpont-házirendjének definíciójának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b79cc-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="b79cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b79cc-104">SYNTAX</span></span>

### <span data-ttu-id="b79cc-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b79cc-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b79cc-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b79cc-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b79cc-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b79cc-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b79cc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b79cc-108">DESCRIPTION</span></span>
<span data-ttu-id="b79cc-109">A **Remove-AzServiceEndpointPolicy** parancsmag eltávolítja a szolgáltatási végpontok házirendjét.</span><span class="sxs-lookup"><span data-stu-id="b79cc-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="b79cc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b79cc-110">EXAMPLES</span></span>

### <span data-ttu-id="b79cc-111">1. példa: a szolgáltatás végpont-házirendjének eltávolítása név használatával</span><span class="sxs-lookup"><span data-stu-id="b79cc-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="b79cc-112">Ez a parancs eltávolítja a szolgáltatás végpontjának házirendjét a név PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="b79cc-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="b79cc-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b79cc-113">PARAMETERS</span></span>

### <span data-ttu-id="b79cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b79cc-114">-DefaultProfile</span></span>
<span data-ttu-id="b79cc-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b79cc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b79cc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b79cc-116">-InputObject</span></span>
<span data-ttu-id="b79cc-117">A szolgáltatás Endpoint Policy definition objektuma.</span><span class="sxs-lookup"><span data-stu-id="b79cc-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="b79cc-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b79cc-118">-Name</span></span>
<span data-ttu-id="b79cc-119">A szolgáltatás végpont-definíciójának neve</span><span class="sxs-lookup"><span data-stu-id="b79cc-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="b79cc-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b79cc-120">-ResourceId</span></span>
<span data-ttu-id="b79cc-121">A szolgáltatás végpont-definíciójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b79cc-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="b79cc-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b79cc-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="b79cc-123">A ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b79cc-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="b79cc-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b79cc-124">-Confirm</span></span>
<span data-ttu-id="b79cc-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b79cc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b79cc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b79cc-126">-WhatIf</span></span>
<span data-ttu-id="b79cc-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b79cc-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b79cc-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b79cc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b79cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b79cc-129">CommonParameters</span></span>
<span data-ttu-id="b79cc-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b79cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b79cc-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b79cc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b79cc-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b79cc-132">INPUTS</span></span>

### <span data-ttu-id="b79cc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b79cc-133">System.String</span></span>

### <span data-ttu-id="b79cc-134">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b79cc-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="b79cc-135">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b79cc-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b79cc-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b79cc-136">OUTPUTS</span></span>

### <span data-ttu-id="b79cc-137">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b79cc-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b79cc-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b79cc-138">NOTES</span></span>

## <span data-ttu-id="b79cc-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b79cc-139">RELATED LINKS</span></span>

[<span data-ttu-id="b79cc-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b79cc-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b79cc-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b79cc-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b79cc-142">Új – AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b79cc-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b79cc-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b79cc-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
