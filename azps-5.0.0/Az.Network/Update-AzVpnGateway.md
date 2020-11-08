---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 419c7bc71def03bc2db004e378d80ea9c31f5183
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185940"
---
# <span data-ttu-id="b2429-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b2429-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="b2429-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2429-102">SYNOPSIS</span></span>
<span data-ttu-id="b2429-103">Méretezhető VPN-átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="b2429-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="b2429-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2429-104">SYNTAX</span></span>

### <span data-ttu-id="b2429-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2429-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2429-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="b2429-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2429-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="b2429-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2429-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2429-108">DESCRIPTION</span></span>
<span data-ttu-id="b2429-109">Az **Update-AzVpnGateway** parancsmag egy skálázható VPN-átjárót frissít.</span><span class="sxs-lookup"><span data-stu-id="b2429-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="b2429-110">Az Azure VPN-átjáró olyan szoftver által definiált kapcsolat a webhelyhez, ahol a VirtualHub belül a webhelyek közötti kapcsolatok használhatók.</span><span class="sxs-lookup"><span data-stu-id="b2429-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="b2429-111">Ez az átjáró a felhasználó által megadott méretarány alapján átméretezi a méretarányokat és a méretarányokat.</span><span class="sxs-lookup"><span data-stu-id="b2429-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="b2429-112">A kapcsolat beállítható egy virtuális magánhálózati webhelyről a méretezhető átjáróra.</span><span class="sxs-lookup"><span data-stu-id="b2429-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="b2429-113">Mindegyik kapcsolat két Active-Active-alagútból áll</span><span class="sxs-lookup"><span data-stu-id="b2429-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="b2429-114">Példák</span><span class="sxs-lookup"><span data-stu-id="b2429-114">EXAMPLES</span></span>

### <span data-ttu-id="b2429-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b2429-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="b2429-116">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="b2429-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b2429-117">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="b2429-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="b2429-118">Az átjáró létrehozása után a Update-AzVpnGateway az átjáró 3 léptékű egységre való frissítéséhez használja.</span><span class="sxs-lookup"><span data-stu-id="b2429-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="b2429-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="b2429-119">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\>$ipconfigurationId1 = 'Instance0'
PS C:\>$addresslist1 = @('169.254.21.5')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>$ipconfigurationId2 = 'Instance1'
PS C:\>$addresslist2 = @('169.254.21.10')
PS C:\>$gw1ipconfBgp2 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId2 -CustomAddress $addresslist2
PS C:\>$gw = Get-AzVpnGateway -ResourceGroupName testRg -Name testgw
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -BgpPeeringAddress @($gw1ipconfBgp1,$gw1ipconfBgp2)

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="b2429-120">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="b2429-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b2429-121">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="b2429-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="b2429-122">Az átjáró létrehozása után Set-AzVpnGateway frissíti a BgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="b2429-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="b2429-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2429-123">PARAMETERS</span></span>

### <span data-ttu-id="b2429-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2429-124">-AsJob</span></span>
<span data-ttu-id="b2429-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b2429-125">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2429-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="b2429-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="b2429-127">A VpnGateway bgpsettings kapcsolatos BGP-peering-címek.</span><span class="sxs-lookup"><span data-stu-id="b2429-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2429-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b2429-128">-Confirm</span></span>
<span data-ttu-id="b2429-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b2429-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2429-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2429-130">-DefaultProfile</span></span>
<span data-ttu-id="b2429-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2429-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2429-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2429-132">-InputObject</span></span>
<span data-ttu-id="b2429-133">A módosítani kívánt VPN-átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="b2429-133">The vpn gateway object to be modified</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2429-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b2429-134">-Name</span></span>
<span data-ttu-id="b2429-135">A VPN-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="b2429-135">The vpn gateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2429-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2429-136">-ResourceGroupName</span></span>
<span data-ttu-id="b2429-137">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b2429-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2429-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2429-138">-ResourceId</span></span>
<span data-ttu-id="b2429-139">A módosítani kívánt VpnGateway Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="b2429-139">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2429-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="b2429-140">-Tag</span></span>
<span data-ttu-id="b2429-141">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b2429-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2429-142">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="b2429-142">-VpnConnection</span></span>
<span data-ttu-id="b2429-143">Annak a VpnConnections a listája, amelyre a VpnGateway szüksége van.</span><span class="sxs-lookup"><span data-stu-id="b2429-143">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2429-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="b2429-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="b2429-145">A VpnGateway méretarányos egysége.</span><span class="sxs-lookup"><span data-stu-id="b2429-145">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2429-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2429-146">-WhatIf</span></span>
<span data-ttu-id="b2429-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b2429-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2429-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b2429-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2429-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2429-149">CommonParameters</span></span>
<span data-ttu-id="b2429-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2429-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2429-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b2429-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2429-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2429-152">INPUTS</span></span>

### <span data-ttu-id="b2429-153">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b2429-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="b2429-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b2429-154">System.String</span></span>

## <span data-ttu-id="b2429-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2429-155">OUTPUTS</span></span>

### <span data-ttu-id="b2429-156">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b2429-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="b2429-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2429-157">NOTES</span></span>

## <span data-ttu-id="b2429-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2429-158">RELATED LINKS</span></span>
[<span data-ttu-id="b2429-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b2429-159">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="b2429-160">Új – AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b2429-160">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="b2429-161">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b2429-161">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)