---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012495"
---
# <span data-ttu-id="e1b49-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e1b49-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="e1b49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1b49-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b49-103">Frissítse a NAT-átjáró erőforrását nyilvános IP-címmel, nyilvános IP-előtaggal és IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="e1b49-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="e1b49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1b49-104">SYNTAX</span></span>

### <span data-ttu-id="e1b49-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1b49-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1b49-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1b49-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1b49-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1b49-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1b49-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1b49-108">DESCRIPTION</span></span>
<span data-ttu-id="e1b49-109">Frissítse a NAT-átjáró erőforrását nyilvános IP-címmel, nyilvános IP-előtaggal és IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="e1b49-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="e1b49-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e1b49-110">EXAMPLES</span></span>

### <span data-ttu-id="e1b49-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e1b49-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="e1b49-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1b49-112">PARAMETERS</span></span>

### <span data-ttu-id="e1b49-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1b49-113">-AsJob</span></span>
<span data-ttu-id="e1b49-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e1b49-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1b49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b49-115">-DefaultProfile</span></span>
<span data-ttu-id="e1b49-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1b49-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1b49-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e1b49-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e1b49-118">A NAT-átjáró üresjárati időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="e1b49-118">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b49-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1b49-119">-InputObject</span></span>
<span data-ttu-id="e1b49-120">A NAT-átjáró erőforrását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1b49-120">Specifies Nat Gateway Resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1b49-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e1b49-121">-Name</span></span>
<span data-ttu-id="e1b49-122">A NAT-átjáró erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="e1b49-122">Name of the Nat Gateway Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b49-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e1b49-123">-PublicIpAddress</span></span>
<span data-ttu-id="e1b49-124">A NAT-átjáró erőforráshoz társított nyilvános IP-címek tömbje.</span><span class="sxs-lookup"><span data-stu-id="e1b49-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b49-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e1b49-125">-PublicIpPrefix</span></span>
<span data-ttu-id="e1b49-126">A NAT-átjáró erőforráshoz társított nyilvános IP-előtagok tömbje.</span><span class="sxs-lookup"><span data-stu-id="e1b49-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b49-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1b49-127">-ResourceGroupName</span></span>
<span data-ttu-id="e1b49-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e1b49-128">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b49-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1b49-129">-ResourceId</span></span>
<span data-ttu-id="e1b49-130">A NAT-átjáró erőforrás azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1b49-130">Specifies the Id of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1b49-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e1b49-131">-Confirm</span></span>
<span data-ttu-id="e1b49-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e1b49-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1b49-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1b49-133">-WhatIf</span></span>
<span data-ttu-id="e1b49-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e1b49-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1b49-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1b49-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1b49-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b49-136">CommonParameters</span></span>
<span data-ttu-id="e1b49-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1b49-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b49-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e1b49-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b49-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1b49-139">INPUTS</span></span>

### <span data-ttu-id="e1b49-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e1b49-140">System.String</span></span>

### <span data-ttu-id="e1b49-141">Microsoft. Azure. commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="e1b49-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="e1b49-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1b49-142">OUTPUTS</span></span>

### <span data-ttu-id="e1b49-143">Microsoft. Azure. commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="e1b49-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="e1b49-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1b49-144">NOTES</span></span>

## <span data-ttu-id="e1b49-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1b49-145">RELATED LINKS</span></span>
