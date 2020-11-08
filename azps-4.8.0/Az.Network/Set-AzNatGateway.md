---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025143"
---
# <span data-ttu-id="5aab1-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5aab1-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="5aab1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5aab1-102">SYNOPSIS</span></span>
<span data-ttu-id="5aab1-103">Frissítse a NAT-átjáró erőforrását nyilvános IP-címmel, nyilvános IP-előtaggal és IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="5aab1-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="5aab1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5aab1-104">SYNTAX</span></span>

### <span data-ttu-id="5aab1-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5aab1-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5aab1-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5aab1-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5aab1-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5aab1-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aab1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5aab1-108">DESCRIPTION</span></span>
<span data-ttu-id="5aab1-109">Frissítse a NAT-átjáró erőforrását nyilvános IP-címmel, nyilvános IP-előtaggal és IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="5aab1-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="5aab1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5aab1-110">EXAMPLES</span></span>

### <span data-ttu-id="5aab1-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5aab1-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="5aab1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5aab1-112">PARAMETERS</span></span>

### <span data-ttu-id="5aab1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5aab1-113">-AsJob</span></span>
<span data-ttu-id="5aab1-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5aab1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5aab1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aab1-115">-DefaultProfile</span></span>
<span data-ttu-id="5aab1-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5aab1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5aab1-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5aab1-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="5aab1-118">A NAT-átjáró üresjárati időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="5aab1-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="5aab1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5aab1-119">-InputObject</span></span>
<span data-ttu-id="5aab1-120">A NAT-átjáró erőforrását adja meg.</span><span class="sxs-lookup"><span data-stu-id="5aab1-120">Specifies Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="5aab1-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5aab1-121">-Name</span></span>
<span data-ttu-id="5aab1-122">A NAT-átjáró erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="5aab1-122">Name of the Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="5aab1-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5aab1-123">-PublicIpAddress</span></span>
<span data-ttu-id="5aab1-124">A NAT-átjáró erőforráshoz társított nyilvános IP-címek tömbje.</span><span class="sxs-lookup"><span data-stu-id="5aab1-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="5aab1-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5aab1-125">-PublicIpPrefix</span></span>
<span data-ttu-id="5aab1-126">A NAT-átjáró erőforráshoz társított nyilvános IP-előtagok tömbje.</span><span class="sxs-lookup"><span data-stu-id="5aab1-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="5aab1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aab1-127">-ResourceGroupName</span></span>
<span data-ttu-id="5aab1-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5aab1-128">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="5aab1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5aab1-129">-ResourceId</span></span>
<span data-ttu-id="5aab1-130">A NAT-átjáró erőforrás azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5aab1-130">Specifies the Id of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="5aab1-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5aab1-131">-Confirm</span></span>
<span data-ttu-id="5aab1-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5aab1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aab1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aab1-133">-WhatIf</span></span>
<span data-ttu-id="5aab1-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5aab1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aab1-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5aab1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aab1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aab1-136">CommonParameters</span></span>
<span data-ttu-id="5aab1-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5aab1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aab1-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5aab1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aab1-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5aab1-139">INPUTS</span></span>

### <span data-ttu-id="5aab1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5aab1-140">System.String</span></span>

### <span data-ttu-id="5aab1-141">Microsoft. Azure. commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="5aab1-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="5aab1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5aab1-142">OUTPUTS</span></span>

### <span data-ttu-id="5aab1-143">Microsoft. Azure. commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="5aab1-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="5aab1-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5aab1-144">NOTES</span></span>

## <span data-ttu-id="5aab1-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5aab1-145">RELATED LINKS</span></span>
