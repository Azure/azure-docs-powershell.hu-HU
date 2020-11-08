---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185958"
---
# <span data-ttu-id="f4b6a-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f4b6a-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="f4b6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b6a-103">A NAT-átjáró erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f4b6a-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="f4b6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4b6a-104">SYNTAX</span></span>

### <span data-ttu-id="f4b6a-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4b6a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4b6a-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4b6a-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4b6a-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4b6a-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4b6a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4b6a-108">DESCRIPTION</span></span>
<span data-ttu-id="f4b6a-109">A NAT-átjáró erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f4b6a-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="f4b6a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f4b6a-110">EXAMPLES</span></span>

### <span data-ttu-id="f4b6a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f4b6a-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="f4b6a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4b6a-112">PARAMETERS</span></span>

### <span data-ttu-id="f4b6a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4b6a-113">-AsJob</span></span>
<span data-ttu-id="f4b6a-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f4b6a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4b6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b6a-115">-DefaultProfile</span></span>
<span data-ttu-id="f4b6a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4b6a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4b6a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f4b6a-117">-Force</span></span>
<span data-ttu-id="f4b6a-118">Ha törölni szeretné az erőforrást, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4b6a-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="f4b6a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4b6a-119">-InputObject</span></span>
<span data-ttu-id="f4b6a-120">A NAT-átjáró erőforrását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4b6a-120">Specifies the Nat Gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b6a-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4b6a-121">-Name</span></span>
<span data-ttu-id="f4b6a-122">A NAT-átjáró erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="f4b6a-122">Name of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b6a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4b6a-123">-PassThru</span></span>
<span data-ttu-id="f4b6a-124">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f4b6a-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f4b6a-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f4b6a-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f4b6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4b6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="f4b6a-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4b6a-127">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b6a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4b6a-128">-ResourceId</span></span>
<span data-ttu-id="f4b6a-129">A NAT-átjáróhoz társított erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f4b6a-129">Resource Id associated with the Nat Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b6a-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4b6a-130">-Confirm</span></span>
<span data-ttu-id="f4b6a-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4b6a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4b6a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4b6a-132">-WhatIf</span></span>
<span data-ttu-id="f4b6a-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4b6a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4b6a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4b6a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4b6a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b6a-135">CommonParameters</span></span>
<span data-ttu-id="f4b6a-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4b6a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b6a-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f4b6a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b6a-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4b6a-138">INPUTS</span></span>

### <span data-ttu-id="f4b6a-139">Microsoft. Azure. commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="f4b6a-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="f4b6a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f4b6a-140">System.String</span></span>

## <span data-ttu-id="f4b6a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4b6a-141">OUTPUTS</span></span>

### <span data-ttu-id="f4b6a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4b6a-142">System.Boolean</span></span>

## <span data-ttu-id="f4b6a-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4b6a-143">NOTES</span></span>

## <span data-ttu-id="f4b6a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4b6a-144">RELATED LINKS</span></span>
