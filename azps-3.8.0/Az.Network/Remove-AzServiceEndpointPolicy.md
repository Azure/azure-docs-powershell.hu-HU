---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013991"
---
# <span data-ttu-id="3239e-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3239e-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="3239e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3239e-102">SYNOPSIS</span></span>
<span data-ttu-id="3239e-103">A szolgáltatás végpont-házirendjének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3239e-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="3239e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3239e-104">SYNTAX</span></span>

### <span data-ttu-id="3239e-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3239e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3239e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3239e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3239e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3239e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3239e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3239e-108">DESCRIPTION</span></span>
<span data-ttu-id="3239e-109">A **Remove-AzServiceEndpointPolicy** parancsmag eltávolítja a szolgáltatási végpontok házirendjét.</span><span class="sxs-lookup"><span data-stu-id="3239e-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="3239e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3239e-110">EXAMPLES</span></span>

### <span data-ttu-id="3239e-111">1. példa: a szolgáltatás végpont-házirendjének eltávolítása név használatával</span><span class="sxs-lookup"><span data-stu-id="3239e-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="3239e-112">Ez a parancs eltávolítja a Service Endpoint Policy nevű Házirend1, amely a "resourcegroup1" nevű resourcegroup tartozik</span><span class="sxs-lookup"><span data-stu-id="3239e-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="3239e-113">2. példa: a szolgáltatási végpontok házirendjének eltávolítása a beviteli objektum használatával</span><span class="sxs-lookup"><span data-stu-id="3239e-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="3239e-114">Ez a parancs eltávolítja az "resourcegroup1" nevű resourcegroup-Házirend1 tartozó szolgáltatás-végpontok házirend-objektumát.</span><span class="sxs-lookup"><span data-stu-id="3239e-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="3239e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3239e-115">PARAMETERS</span></span>

### <span data-ttu-id="3239e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3239e-116">-DefaultProfile</span></span>
<span data-ttu-id="3239e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3239e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3239e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3239e-118">-Force</span></span>
<span data-ttu-id="3239e-119">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3239e-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3239e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3239e-120">-InputObject</span></span>
<span data-ttu-id="3239e-121">A szolgáltatás végpontjának házirend-objektuma.</span><span class="sxs-lookup"><span data-stu-id="3239e-121">The service endpoint policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3239e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3239e-122">-Name</span></span>
<span data-ttu-id="3239e-123">A szolgáltatás végpont-házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="3239e-123">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3239e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3239e-124">-PassThru</span></span>
<span data-ttu-id="3239e-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="3239e-125">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3239e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3239e-126">-ResourceGroupName</span></span>
<span data-ttu-id="3239e-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3239e-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3239e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3239e-128">-ResourceId</span></span>
<span data-ttu-id="3239e-129">A szolgáltatás végpont-házirendjének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3239e-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="3239e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3239e-130">-Confirm</span></span>
<span data-ttu-id="3239e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3239e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3239e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3239e-132">-WhatIf</span></span>
<span data-ttu-id="3239e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3239e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3239e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3239e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3239e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3239e-135">CommonParameters</span></span>
<span data-ttu-id="3239e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3239e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3239e-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3239e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3239e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3239e-138">INPUTS</span></span>

### <span data-ttu-id="3239e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3239e-139">System.String</span></span>

### <span data-ttu-id="3239e-140">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3239e-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="3239e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3239e-141">OUTPUTS</span></span>

### <span data-ttu-id="3239e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3239e-142">System.Boolean</span></span>

## <span data-ttu-id="3239e-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3239e-143">NOTES</span></span>

## <span data-ttu-id="3239e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3239e-144">RELATED LINKS</span></span>

[<span data-ttu-id="3239e-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3239e-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="3239e-146">Új – AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3239e-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="3239e-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3239e-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
