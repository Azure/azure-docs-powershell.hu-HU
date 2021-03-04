---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGatewayNatRule.md
ms.openlocfilehash: e0a2722a59a9ffe1b6a7c3fb401b4faca85a1650
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918338"
---
# <span data-ttu-id="521c5-101">Update-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="521c5-101">Update-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="521c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="521c5-102">SYNOPSIS</span></span>
<span data-ttu-id="521c5-103">Frissíti a VpnGatewayhez társított NAT-szabályt.</span><span class="sxs-lookup"><span data-stu-id="521c5-103">Updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="521c5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="521c5-104">SYNTAX</span></span>

### <span data-ttu-id="521c5-105">ByVpnGatewayNatRuleName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="521c5-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Update-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>] [-ExternalMapping <String[]>]
 [-IpConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="521c5-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="521c5-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Update-AzVpnGatewayNatRule -ResourceId <String> [-Type <String>] [-Mode <String>] [-InternalMapping <String[]>]
 [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="521c5-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="521c5-107">ByVpnGatewayNatRuleObject</span></span>
```
Update-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Type <String>] [-Mode <String>]
 [-InternalMapping <String[]>] [-ExternalMapping <String[]>] [-IpConfigurationId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="521c5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="521c5-108">DESCRIPTION</span></span>
<span data-ttu-id="521c5-109">Az **Update-AzVpnGatewayNatRule** parancsmag frissíti a VpnGatewayhez társított NAT-szabályt.</span><span class="sxs-lookup"><span data-stu-id="521c5-109">The **Update-AzVpnGatewayNatRule** cmdlet updates a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="521c5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="521c5-110">EXAMPLES</span></span>

### <span data-ttu-id="521c5-111">Példa</span><span class="sxs-lookup"><span data-stu-id="521c5-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> $natRule = Update-AzVpnGatewayNatRule -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy
PS C:\> Update-AzVpnGatewayNatRule -InputObject $natRule -Type Dynamic -Mode IngressSnat

Type                      : Dynamic
Mode                      : IngressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule
```

<span data-ttu-id="521c5-112">A fentiekkel létrehozhat egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub).</span><span class="sxs-lookup"><span data-stu-id="521c5-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub.</span></span> <span data-ttu-id="521c5-113">Ezután létre fogjuk hozni a VpnGatewayt a virtuális központ alatt.</span><span class="sxs-lookup"><span data-stu-id="521c5-113">Then, we will create VpnGateway under that Virtual Hub.</span></span> <span data-ttu-id="521c5-114">Ezután hozzon létre új NAT-szabályt a létrehozott VpnGatewayhez.</span><span class="sxs-lookup"><span data-stu-id="521c5-114">Then, create new NAT rule associated with created VpnGateway.</span></span>
<span data-ttu-id="521c5-115">Ezzel a paranccsal: Update-AzVpnGatewayNatRule, update NAT rule.</span><span class="sxs-lookup"><span data-stu-id="521c5-115">Using this command: Update-AzVpnGatewayNatRule, update NAT rule.</span></span>

## <span data-ttu-id="521c5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="521c5-116">PARAMETERS</span></span>

### <span data-ttu-id="521c5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="521c5-117">-AsJob</span></span>
<span data-ttu-id="521c5-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="521c5-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="521c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521c5-119">-DefaultProfile</span></span>
<span data-ttu-id="521c5-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="521c5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="521c5-121">-ExternalMapping</span><span class="sxs-lookup"><span data-stu-id="521c5-121">-ExternalMapping</span></span>
<span data-ttu-id="521c5-122">A NAT privát IP-cím alhálózati hozzárendeléseinek listája</span><span class="sxs-lookup"><span data-stu-id="521c5-122">The list of private IP address subnet external mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521c5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="521c5-123">-InputObject</span></span>
<span data-ttu-id="521c5-124">Frissítenünk kell a VpnGatewayNatRule objektumot.</span><span class="sxs-lookup"><span data-stu-id="521c5-124">The VpnGatewayNatRule object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule
Parameter Sets: ByVpnGatewayNatRuleObject
Aliases: VpnGatewayNatRule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="521c5-125">-InternalMapping</span><span class="sxs-lookup"><span data-stu-id="521c5-125">-InternalMapping</span></span>
<span data-ttu-id="521c5-126">A NAT privát IP-cím alhálózati belső megfeleltetéseinek listája</span><span class="sxs-lookup"><span data-stu-id="521c5-126">The list of private IP address subnet internal mappings for NAT</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521c5-127">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="521c5-127">-IpConfigurationId</span></span>
<span data-ttu-id="521c5-128">A NAT-szabály ip-konfigurációs azonosítója</span><span class="sxs-lookup"><span data-stu-id="521c5-128">The IP Configuration ID this NAT rule applies to</span></span>

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

### <span data-ttu-id="521c5-129">-Mód</span><span class="sxs-lookup"><span data-stu-id="521c5-129">-Mode</span></span>
<span data-ttu-id="521c5-130">A VPN NAT forrás NAT-útvonala</span><span class="sxs-lookup"><span data-stu-id="521c5-130">The Source NAT direction of a VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EgressSnat, IngressSnat

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521c5-131">-Name</span><span class="sxs-lookup"><span data-stu-id="521c5-131">-Name</span></span>
<span data-ttu-id="521c5-132">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="521c5-132">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521c5-133">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="521c5-133">-ParentResourceName</span></span>
<span data-ttu-id="521c5-134">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="521c5-134">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521c5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="521c5-135">-ResourceGroupName</span></span>
<span data-ttu-id="521c5-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="521c5-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521c5-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="521c5-137">-ResourceId</span></span>
<span data-ttu-id="521c5-138">A törölni kívánt VpnGatewayNatRule objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="521c5-138">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="521c5-139">-Type</span><span class="sxs-lookup"><span data-stu-id="521c5-139">-Type</span></span>
<span data-ttu-id="521c5-140">A VPN NAT NAT-szabályának típusa</span><span class="sxs-lookup"><span data-stu-id="521c5-140">The type of NAT rule for VPN NAT</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521c5-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="521c5-141">-Confirm</span></span>
<span data-ttu-id="521c5-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="521c5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="521c5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="521c5-143">-WhatIf</span></span>
<span data-ttu-id="521c5-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="521c5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="521c5-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="521c5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="521c5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521c5-146">CommonParameters</span></span>
<span data-ttu-id="521c5-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="521c5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521c5-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="521c5-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521c5-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="521c5-149">INPUTS</span></span>

### <span data-ttu-id="521c5-150">System.String</span><span class="sxs-lookup"><span data-stu-id="521c5-150">System.String</span></span>

### <span data-ttu-id="521c5-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="521c5-151">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="521c5-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="521c5-152">OUTPUTS</span></span>

### <span data-ttu-id="521c5-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="521c5-153">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="521c5-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="521c5-154">NOTES</span></span>

## <span data-ttu-id="521c5-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="521c5-155">RELATED LINKS</span></span>
