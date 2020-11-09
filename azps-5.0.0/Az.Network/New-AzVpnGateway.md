---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: fa7374264e46e65dcddacb9f35e5822f18294147
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303710"
---
# <span data-ttu-id="2bac6-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2bac6-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="2bac6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2bac6-102">SYNOPSIS</span></span>
<span data-ttu-id="2bac6-103">Méretezhető VPN-átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2bac6-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="2bac6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2bac6-104">SYNTAX</span></span>

### <span data-ttu-id="2bac6-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2bac6-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bac6-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="2bac6-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bac6-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="2bac6-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bac6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2bac6-108">DESCRIPTION</span></span>

<span data-ttu-id="2bac6-109">A New-AzVpnGateway méretezhető VPN-átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2bac6-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span> <span data-ttu-id="2bac6-110">Ez a szoftver által definiált, a VirtualHub-on belüli kapcsolatok a webhelyek között.</span><span class="sxs-lookup"><span data-stu-id="2bac6-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span> 

<span data-ttu-id="2bac6-111">Az átjáró az ebben vagy az Set-AzVpnGateway parancsmagban megadott méretarány alapján átméretezi a méretarányokat és a méretarányokat.</span><span class="sxs-lookup"><span data-stu-id="2bac6-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span> 

<span data-ttu-id="2bac6-112">Egy kapcsolat be van állítva egy olyan elágazásból/webhelyről, amelyet a VPNSite a skálázható átjárónak nevezünk.</span><span class="sxs-lookup"><span data-stu-id="2bac6-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span> <span data-ttu-id="2bac6-113">Mindegyik kapcsolat két Active-Active-alagútból áll.</span><span class="sxs-lookup"><span data-stu-id="2bac6-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="2bac6-114">A VpnGateway ugyanabba a helyre kerül, mint a hivatkozott VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="2bac6-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="2bac6-115">Példák</span><span class="sxs-lookup"><span data-stu-id="2bac6-115">EXAMPLES</span></span>

### <span data-ttu-id="2bac6-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2bac6-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="2bac6-117">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="2bac6-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="2bac6-118">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="2bac6-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="2bac6-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2bac6-119">PARAMETERS</span></span>

### <span data-ttu-id="2bac6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bac6-120">-AsJob</span></span>
<span data-ttu-id="2bac6-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2bac6-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bac6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bac6-122">-DefaultProfile</span></span>
<span data-ttu-id="2bac6-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2bac6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bac6-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2bac6-124">-Name</span></span>
<span data-ttu-id="2bac6-125">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2bac6-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bac6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bac6-126">-ResourceGroupName</span></span>
<span data-ttu-id="2bac6-127">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2bac6-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bac6-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="2bac6-128">-Tag</span></span>
<span data-ttu-id="2bac6-129">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2bac6-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2bac6-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="2bac6-130">-VirtualHub</span></span>
<span data-ttu-id="2bac6-131">A VirtualHub ehhez a VpnGateway társítva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2bac6-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bac6-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="2bac6-132">-VirtualHubId</span></span>
<span data-ttu-id="2bac6-133">Annak a VirtualHub az azonosítóját, amelyre ezt a VpnGateway társítani kell.</span><span class="sxs-lookup"><span data-stu-id="2bac6-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bac6-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="2bac6-134">-VirtualHubName</span></span>
<span data-ttu-id="2bac6-135">Annak a VirtualHub az azonosítóját, amelyre ezt a VpnGateway társítani kell.</span><span class="sxs-lookup"><span data-stu-id="2bac6-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bac6-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2bac6-136">-VpnConnection</span></span>
<span data-ttu-id="2bac6-137">Annak a VpnConnections a listája, amelyre a VpnGateway szüksége van.</span><span class="sxs-lookup"><span data-stu-id="2bac6-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="2bac6-138">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="2bac6-138">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="2bac6-139">A VpnGateway méretarányos egysége.</span><span class="sxs-lookup"><span data-stu-id="2bac6-139">The scale unit for this VpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bac6-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2bac6-140">-Confirm</span></span>
<span data-ttu-id="2bac6-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2bac6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bac6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bac6-142">-WhatIf</span></span>
<span data-ttu-id="2bac6-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2bac6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bac6-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2bac6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bac6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bac6-145">CommonParameters</span></span>
<span data-ttu-id="2bac6-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2bac6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bac6-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bac6-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bac6-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bac6-148">INPUTS</span></span>

### <span data-ttu-id="2bac6-149">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2bac6-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="2bac6-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2bac6-150">System.String</span></span>

## <span data-ttu-id="2bac6-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bac6-151">OUTPUTS</span></span>

### <span data-ttu-id="2bac6-152">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2bac6-152">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="2bac6-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2bac6-153">NOTES</span></span>

## <span data-ttu-id="2bac6-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2bac6-154">RELATED LINKS</span></span>

[<span data-ttu-id="2bac6-155">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2bac6-155">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="2bac6-156">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2bac6-156">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="2bac6-157">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2bac6-157">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
