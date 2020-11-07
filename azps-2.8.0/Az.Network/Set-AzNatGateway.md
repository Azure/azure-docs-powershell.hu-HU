---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: 40a1d9c77d870971f8aa432735f556e89ad55e0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837773"
---
# <span data-ttu-id="edd0d-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="edd0d-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="edd0d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="edd0d-102">SYNOPSIS</span></span>
<span data-ttu-id="edd0d-103">Frissítse a NAT-átjáró erőforrását nyilvános IP-címmel, nyilvános IP-előtaggal és IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="edd0d-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="edd0d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="edd0d-104">SYNTAX</span></span>

### <span data-ttu-id="edd0d-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="edd0d-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edd0d-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="edd0d-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edd0d-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="edd0d-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edd0d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="edd0d-108">DESCRIPTION</span></span>
<span data-ttu-id="edd0d-109">Frissítse a NAT-átjáró erőforrását nyilvános IP-címmel, nyilvános IP-előtaggal és IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="edd0d-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="edd0d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="edd0d-110">EXAMPLES</span></span>

### <span data-ttu-id="edd0d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="edd0d-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="edd0d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="edd0d-112">PARAMETERS</span></span>

### <span data-ttu-id="edd0d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edd0d-113">-AsJob</span></span>
<span data-ttu-id="edd0d-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="edd0d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edd0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd0d-115">-DefaultProfile</span></span>
<span data-ttu-id="edd0d-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="edd0d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edd0d-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="edd0d-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="edd0d-118">A NAT-átjáró üresjárati időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="edd0d-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="edd0d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edd0d-119">-InputObject</span></span>
<span data-ttu-id="edd0d-120">A NAT-átjáró erőforrását adja meg.</span><span class="sxs-lookup"><span data-stu-id="edd0d-120">Specifies Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="edd0d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="edd0d-121">-Name</span></span>
<span data-ttu-id="edd0d-122">A NAT-átjáró erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="edd0d-122">Name of the Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="edd0d-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="edd0d-123">-PublicIpAddress</span></span>
<span data-ttu-id="edd0d-124">A NAT-átjáró erőforráshoz társított nyilvános IP-címek tömbje.</span><span class="sxs-lookup"><span data-stu-id="edd0d-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="edd0d-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="edd0d-125">-PublicIpPrefix</span></span>
<span data-ttu-id="edd0d-126">A NAT-átjáró erőforráshoz társított nyilvános IP-előtagok tömbje.</span><span class="sxs-lookup"><span data-stu-id="edd0d-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="edd0d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edd0d-127">-ResourceGroupName</span></span>
<span data-ttu-id="edd0d-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="edd0d-128">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="edd0d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edd0d-129">-ResourceId</span></span>
<span data-ttu-id="edd0d-130">A NAT-átjáró erőforrás azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="edd0d-130">Specifies the Id of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="edd0d-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="edd0d-131">-Confirm</span></span>
<span data-ttu-id="edd0d-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="edd0d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edd0d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edd0d-133">-WhatIf</span></span>
<span data-ttu-id="edd0d-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="edd0d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edd0d-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="edd0d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edd0d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd0d-136">CommonParameters</span></span>
<span data-ttu-id="edd0d-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="edd0d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd0d-138">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="edd0d-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd0d-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="edd0d-139">INPUTS</span></span>

### <span data-ttu-id="edd0d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="edd0d-140">System.String</span></span>

### <span data-ttu-id="edd0d-141">Microsoft. Azure. commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="edd0d-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="edd0d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="edd0d-142">OUTPUTS</span></span>

### <span data-ttu-id="edd0d-143">Microsoft. Azure. commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="edd0d-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="edd0d-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="edd0d-144">NOTES</span></span>

## <span data-ttu-id="edd0d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="edd0d-145">RELATED LINKS</span></span>
