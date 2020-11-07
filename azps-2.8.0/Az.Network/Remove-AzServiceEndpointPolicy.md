---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: fbe09b0ce6ad997ee914bf515aeb78f3fcee7971
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837828"
---
# <span data-ttu-id="f17a8-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f17a8-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="f17a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f17a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f17a8-103">A szolgáltatás végpont-házirendjének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="f17a8-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="f17a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f17a8-104">SYNTAX</span></span>

### <span data-ttu-id="f17a8-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f17a8-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f17a8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f17a8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f17a8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f17a8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f17a8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f17a8-108">DESCRIPTION</span></span>
<span data-ttu-id="f17a8-109">A **Remove-AzServiceEndpointPolicy** parancsmag eltávolítja a szolgáltatási végpontok házirendjét.</span><span class="sxs-lookup"><span data-stu-id="f17a8-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="f17a8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f17a8-110">EXAMPLES</span></span>

### <span data-ttu-id="f17a8-111">1. példa: a szolgáltatás végpont-házirendjének eltávolítása név használatával</span><span class="sxs-lookup"><span data-stu-id="f17a8-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="f17a8-112">Ez a parancs eltávolítja a Service Endpoint Policy nevű Házirend1, amely a "resourcegroup1" nevű resourcegroup tartozik</span><span class="sxs-lookup"><span data-stu-id="f17a8-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="f17a8-113">2. példa: a szolgáltatási végpontok házirendjének eltávolítása a beviteli objektum használatával</span><span class="sxs-lookup"><span data-stu-id="f17a8-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="f17a8-114">Ez a parancs eltávolítja az "resourcegroup1" nevű resourcegroup-Házirend1 tartozó szolgáltatás-végpontok házirend-objektumát.</span><span class="sxs-lookup"><span data-stu-id="f17a8-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="f17a8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f17a8-115">PARAMETERS</span></span>

### <span data-ttu-id="f17a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f17a8-116">-DefaultProfile</span></span>
<span data-ttu-id="f17a8-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f17a8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f17a8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f17a8-118">-Force</span></span>
<span data-ttu-id="f17a8-119">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f17a8-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f17a8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f17a8-120">-InputObject</span></span>
<span data-ttu-id="f17a8-121">A szolgáltatás végpontjának házirend-objektuma.</span><span class="sxs-lookup"><span data-stu-id="f17a8-121">The service endpoint policy object.</span></span>

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

### <span data-ttu-id="f17a8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f17a8-122">-Name</span></span>
<span data-ttu-id="f17a8-123">A szolgáltatás végpont-házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="f17a8-123">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="f17a8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f17a8-124">-PassThru</span></span>
<span data-ttu-id="f17a8-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f17a8-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="f17a8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f17a8-126">-ResourceGroupName</span></span>
<span data-ttu-id="f17a8-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f17a8-127">The resource group name.</span></span>

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

### <span data-ttu-id="f17a8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f17a8-128">-ResourceId</span></span>
<span data-ttu-id="f17a8-129">A szolgáltatás végpont-házirendjének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f17a8-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="f17a8-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f17a8-130">-Confirm</span></span>
<span data-ttu-id="f17a8-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f17a8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f17a8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f17a8-132">-WhatIf</span></span>
<span data-ttu-id="f17a8-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f17a8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f17a8-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f17a8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f17a8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17a8-135">CommonParameters</span></span>
<span data-ttu-id="f17a8-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f17a8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17a8-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f17a8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17a8-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f17a8-138">INPUTS</span></span>

### <span data-ttu-id="f17a8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f17a8-139">System.String</span></span>

### <span data-ttu-id="f17a8-140">Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f17a8-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f17a8-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f17a8-141">OUTPUTS</span></span>

### <span data-ttu-id="f17a8-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f17a8-142">System.Boolean</span></span>

## <span data-ttu-id="f17a8-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f17a8-143">NOTES</span></span>

## <span data-ttu-id="f17a8-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f17a8-144">RELATED LINKS</span></span>

[<span data-ttu-id="f17a8-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f17a8-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="f17a8-146">Új – AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f17a8-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="f17a8-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f17a8-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
