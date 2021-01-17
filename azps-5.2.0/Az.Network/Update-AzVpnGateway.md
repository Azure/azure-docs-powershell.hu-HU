---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 419c7bc71def03bc2db004e378d80ea9c31f5183
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350693"
---
# <span data-ttu-id="76361-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="76361-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="76361-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76361-102">SYNOPSIS</span></span>
<span data-ttu-id="76361-103">Frissíti a méretezhető VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="76361-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="76361-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="76361-104">SYNTAX</span></span>

### <span data-ttu-id="76361-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="76361-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76361-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="76361-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76361-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="76361-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76361-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="76361-108">DESCRIPTION</span></span>
<span data-ttu-id="76361-109">Az **Update-AzVpnGateway** parancsmag frissít egy méretezhető VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="76361-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="76361-110">Az Azure VPN-átjáró egy olyan szoftveres kapcsolat, amely a VirtualHubon belüli webhelykapcsolatokat csatlakoztatja a webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="76361-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="76361-111">Ez az átjáró átméretezi és méretezi a felhasználó által megadott méretarányt.</span><span class="sxs-lookup"><span data-stu-id="76361-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="76361-112">Egy VPN-webhelyről be lehet állítani egy kapcsolatot a méretezhető átjáróval.</span><span class="sxs-lookup"><span data-stu-id="76361-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="76361-113">Minden kapcsolat 2 különböző Active-Active része</span><span class="sxs-lookup"><span data-stu-id="76361-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="76361-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="76361-114">EXAMPLES</span></span>

### <span data-ttu-id="76361-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="76361-115">Example 1</span></span>

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

<span data-ttu-id="76361-116">A fentiekkel létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure).</span><span class="sxs-lookup"><span data-stu-id="76361-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="76361-117">Ezután létrejön egy VPN-átjáró a virtuális központban 2 méretarányú egységben.</span><span class="sxs-lookup"><span data-stu-id="76361-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="76361-118">Az átjáró létrehozása után a Update-AzVpnGateway 3 méretarányú egységekre frissíti az átjárót.</span><span class="sxs-lookup"><span data-stu-id="76361-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="76361-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="76361-119">Example 2</span></span>

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

<span data-ttu-id="76361-120">A fentiekkel létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure).</span><span class="sxs-lookup"><span data-stu-id="76361-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="76361-121">Ezután létrejön egy VPN-átjáró a virtuális központban 2 méretarányú egységben.</span><span class="sxs-lookup"><span data-stu-id="76361-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="76361-122">Az átjáró létrehozása után a Set-AzVpnGateway BgpPeeringAddress frissítése.</span><span class="sxs-lookup"><span data-stu-id="76361-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="76361-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76361-123">PARAMETERS</span></span>

### <span data-ttu-id="76361-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76361-124">-AsJob</span></span>
<span data-ttu-id="76361-125">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="76361-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76361-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="76361-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="76361-127">A VpnGateway bgpsettings BGP-társviszony-címei.</span><span class="sxs-lookup"><span data-stu-id="76361-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

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

### <span data-ttu-id="76361-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76361-128">-Confirm</span></span>
<span data-ttu-id="76361-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="76361-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76361-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76361-130">-DefaultProfile</span></span>
<span data-ttu-id="76361-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76361-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76361-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76361-132">-InputObject</span></span>
<span data-ttu-id="76361-133">A módosítható VPN-átjáróobjektum</span><span class="sxs-lookup"><span data-stu-id="76361-133">The vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="76361-134">-Name</span><span class="sxs-lookup"><span data-stu-id="76361-134">-Name</span></span>
<span data-ttu-id="76361-135">A vpn-átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="76361-135">The vpn gateway name.</span></span>

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

### <span data-ttu-id="76361-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76361-136">-ResourceGroupName</span></span>
<span data-ttu-id="76361-137">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="76361-137">The resource group name.</span></span>

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

### <span data-ttu-id="76361-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76361-138">-ResourceId</span></span>
<span data-ttu-id="76361-139">A módosítható VpnGateway Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="76361-139">The Azure resource ID of the VpnGateway to be modified.</span></span>

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

### <span data-ttu-id="76361-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="76361-140">-Tag</span></span>
<span data-ttu-id="76361-141">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="76361-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="76361-142">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="76361-142">-VpnConnection</span></span>
<span data-ttu-id="76361-143">A VpnGatewayhez szükséges VpnConnections listája.</span><span class="sxs-lookup"><span data-stu-id="76361-143">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="76361-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="76361-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="76361-145">A VpnGateway méretaránya.</span><span class="sxs-lookup"><span data-stu-id="76361-145">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="76361-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76361-146">-WhatIf</span></span>
<span data-ttu-id="76361-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="76361-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76361-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76361-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76361-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76361-149">CommonParameters</span></span>
<span data-ttu-id="76361-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76361-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76361-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76361-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76361-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76361-152">INPUTS</span></span>

### <span data-ttu-id="76361-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="76361-153">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="76361-154">System.String</span><span class="sxs-lookup"><span data-stu-id="76361-154">System.String</span></span>

## <span data-ttu-id="76361-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76361-155">OUTPUTS</span></span>

### <span data-ttu-id="76361-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="76361-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="76361-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="76361-157">NOTES</span></span>

## <span data-ttu-id="76361-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76361-158">RELATED LINKS</span></span>
[<span data-ttu-id="76361-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="76361-159">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="76361-160">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="76361-160">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="76361-161">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="76361-161">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)