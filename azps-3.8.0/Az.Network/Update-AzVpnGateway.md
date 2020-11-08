---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: 8db43fc826086235a51f32e67a8f787a3ac5792d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011771"
---
# <span data-ttu-id="663b0-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="663b0-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="663b0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="663b0-102">SYNOPSIS</span></span>
<span data-ttu-id="663b0-103">Méretezhető VPN-átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="663b0-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="663b0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="663b0-104">SYNTAX</span></span>

### <span data-ttu-id="663b0-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="663b0-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="663b0-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="663b0-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="663b0-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="663b0-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="663b0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="663b0-108">DESCRIPTION</span></span>
<span data-ttu-id="663b0-109">Az **Update-AzVpnGateway** parancsmag egy skálázható VPN-átjárót frissít.</span><span class="sxs-lookup"><span data-stu-id="663b0-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="663b0-110">Az Azure VPN-átjáró olyan szoftver által definiált kapcsolat a webhelyhez, ahol a VirtualHub belül a webhelyek közötti kapcsolatok használhatók.</span><span class="sxs-lookup"><span data-stu-id="663b0-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="663b0-111">Ez az átjáró a felhasználó által megadott méretarány alapján átméretezi a méretarányokat és a méretarányokat.</span><span class="sxs-lookup"><span data-stu-id="663b0-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="663b0-112">A kapcsolat beállítható egy virtuális magánhálózati webhelyről a méretezhető átjáróra.</span><span class="sxs-lookup"><span data-stu-id="663b0-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="663b0-113">Mindegyik kapcsolat két Active-Active-alagútból áll</span><span class="sxs-lookup"><span data-stu-id="663b0-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="663b0-114">Példák</span><span class="sxs-lookup"><span data-stu-id="663b0-114">EXAMPLES</span></span>

### <span data-ttu-id="663b0-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="663b0-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Set-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

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

<span data-ttu-id="663b0-116">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="663b0-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="663b0-117">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="663b0-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="663b0-118">Az átjáró létrehozása után a Set-AzVpnGateway az átjáró 3 léptékű egységre való frissítéséhez használja.</span><span class="sxs-lookup"><span data-stu-id="663b0-118">After the gateway has been created, it uses Set-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

## <span data-ttu-id="663b0-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="663b0-119">PARAMETERS</span></span>

### <span data-ttu-id="663b0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="663b0-120">-AsJob</span></span>
<span data-ttu-id="663b0-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="663b0-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="663b0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="663b0-122">-DefaultProfile</span></span>
<span data-ttu-id="663b0-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="663b0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="663b0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="663b0-124">-InputObject</span></span>
<span data-ttu-id="663b0-125">A módosítani kívánt VPN-átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="663b0-125">The vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="663b0-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="663b0-126">-Name</span></span>
<span data-ttu-id="663b0-127">A virtuális WAN-név.</span><span class="sxs-lookup"><span data-stu-id="663b0-127">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663b0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="663b0-128">-ResourceGroupName</span></span>
<span data-ttu-id="663b0-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="663b0-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663b0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="663b0-130">-ResourceId</span></span>
<span data-ttu-id="663b0-131">A módosítani kívánt VpnGateway Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="663b0-131">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663b0-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="663b0-132">-Tag</span></span>
<span data-ttu-id="663b0-133">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="663b0-133">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663b0-134">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="663b0-134">-VpnConnection</span></span>
<span data-ttu-id="663b0-135">Annak a VpnConnections a listája, amelyre a VpnGateway szüksége van.</span><span class="sxs-lookup"><span data-stu-id="663b0-135">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663b0-136">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="663b0-136">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="663b0-137">A VpnGateway méretarányos egysége.</span><span class="sxs-lookup"><span data-stu-id="663b0-137">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663b0-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="663b0-138">-Confirm</span></span>
<span data-ttu-id="663b0-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="663b0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="663b0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="663b0-140">-WhatIf</span></span>
<span data-ttu-id="663b0-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="663b0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="663b0-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="663b0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="663b0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="663b0-143">CommonParameters</span></span>
<span data-ttu-id="663b0-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="663b0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="663b0-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="663b0-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="663b0-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="663b0-146">INPUTS</span></span>

### <span data-ttu-id="663b0-147">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="663b0-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="663b0-148">System. String</span><span class="sxs-lookup"><span data-stu-id="663b0-148">System.String</span></span>

## <span data-ttu-id="663b0-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="663b0-149">OUTPUTS</span></span>

### <span data-ttu-id="663b0-150">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="663b0-150">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="663b0-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="663b0-151">NOTES</span></span>

## <span data-ttu-id="663b0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="663b0-152">RELATED LINKS</span></span>

[<span data-ttu-id="663b0-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="663b0-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="663b0-154">Új – AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="663b0-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="663b0-155">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="663b0-155">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)
