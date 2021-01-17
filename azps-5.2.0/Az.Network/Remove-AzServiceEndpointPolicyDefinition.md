---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361954"
---
# <span data-ttu-id="dd9fc-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dd9fc-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="dd9fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd9fc-102">SYNOPSIS</span></span>
<span data-ttu-id="dd9fc-103">Szolgáltatásvégpont-házirenddefiníció eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="dd9fc-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="dd9fc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dd9fc-104">SYNTAX</span></span>

### <span data-ttu-id="dd9fc-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd9fc-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd9fc-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd9fc-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd9fc-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd9fc-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd9fc-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dd9fc-108">DESCRIPTION</span></span>
<span data-ttu-id="dd9fc-109">A **Remove-AzServiceEndpointPolicy** parancsmag eltávolít egy szolgáltatás végponti házirendet.</span><span class="sxs-lookup"><span data-stu-id="dd9fc-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="dd9fc-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dd9fc-110">EXAMPLES</span></span>

### <span data-ttu-id="dd9fc-111">1. példa: Szolgáltatásvégpont-házirend eltávolítása név használatával</span><span class="sxs-lookup"><span data-stu-id="dd9fc-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="dd9fc-112">Ez a parancs eltávolít egy HázirendDef1 nevű szolgáltatásvégpont-házirendet</span><span class="sxs-lookup"><span data-stu-id="dd9fc-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="dd9fc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd9fc-113">PARAMETERS</span></span>

### <span data-ttu-id="dd9fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd9fc-114">-DefaultProfile</span></span>
<span data-ttu-id="dd9fc-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd9fc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd9fc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd9fc-116">-InputObject</span></span>
<span data-ttu-id="dd9fc-117">A szolgáltatás végponti házirend-definíciós objektuma.</span><span class="sxs-lookup"><span data-stu-id="dd9fc-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="dd9fc-118">-Name</span><span class="sxs-lookup"><span data-stu-id="dd9fc-118">-Name</span></span>
<span data-ttu-id="dd9fc-119">A szolgáltatás végpontdefiníciójának neve</span><span class="sxs-lookup"><span data-stu-id="dd9fc-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="dd9fc-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd9fc-120">-ResourceId</span></span>
<span data-ttu-id="dd9fc-121">A szolgáltatás végpontdefiníciójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dd9fc-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="dd9fc-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="dd9fc-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="dd9fc-123">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="dd9fc-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="dd9fc-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd9fc-124">-Confirm</span></span>
<span data-ttu-id="dd9fc-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dd9fc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd9fc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd9fc-126">-WhatIf</span></span>
<span data-ttu-id="dd9fc-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dd9fc-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd9fc-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd9fc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd9fc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd9fc-129">CommonParameters</span></span>
<span data-ttu-id="dd9fc-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd9fc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd9fc-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd9fc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd9fc-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd9fc-132">INPUTS</span></span>

### <span data-ttu-id="dd9fc-133">System.String</span><span class="sxs-lookup"><span data-stu-id="dd9fc-133">System.String</span></span>

### <span data-ttu-id="dd9fc-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dd9fc-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="dd9fc-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="dd9fc-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="dd9fc-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd9fc-136">OUTPUTS</span></span>

### <span data-ttu-id="dd9fc-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="dd9fc-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="dd9fc-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dd9fc-138">NOTES</span></span>

## <span data-ttu-id="dd9fc-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd9fc-139">RELATED LINKS</span></span>

[<span data-ttu-id="dd9fc-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dd9fc-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="dd9fc-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dd9fc-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="dd9fc-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dd9fc-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="dd9fc-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dd9fc-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
