---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 7e68e8e48ffa9d86222951b7ca2e076351872be6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934802"
---
# <span data-ttu-id="4d64c-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4d64c-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="4d64c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d64c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d64c-103">Méretezhető VPN-átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4d64c-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="4d64c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d64c-104">SYNTAX</span></span>

### <span data-ttu-id="4d64c-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d64c-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d64c-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="4d64c-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d64c-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="4d64c-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d64c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d64c-108">DESCRIPTION</span></span>
<span data-ttu-id="4d64c-109">New-AzVpnGateway létrehoz egy méretezhető VPN-átjárót.</span><span class="sxs-lookup"><span data-stu-id="4d64c-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span>
<span data-ttu-id="4d64c-110">Ez a VirtualHubon belüli webhelykapcsolatok szoftverrel definiált kapcsolata.</span><span class="sxs-lookup"><span data-stu-id="4d64c-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span>

<span data-ttu-id="4d64c-111">Ez az átjáró az ebben vagy a parancsmagban megadott méretarány alapján méretezi át Set-AzVpnGateway méretarányt.</span><span class="sxs-lookup"><span data-stu-id="4d64c-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span>

<span data-ttu-id="4d64c-112">A kapcsolat egy VPNSite néven ismert ágból vagy webhelyről van beállítva a méretezhető átjáróval.</span><span class="sxs-lookup"><span data-stu-id="4d64c-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span>
<span data-ttu-id="4d64c-113">Minden kapcsolat 2 különböző Active-Active része.</span><span class="sxs-lookup"><span data-stu-id="4d64c-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="4d64c-114">A VpnGateway ugyanazon a helyen lesz, mint a hivatkozott VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="4d64c-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="4d64c-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d64c-115">EXAMPLES</span></span>

### <span data-ttu-id="4d64c-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="4d64c-116">Example 1</span></span>
```
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2 -EnableRoutingPreferenceInternetFlag

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

<span data-ttu-id="4d64c-117">A fentiekkel létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure).</span><span class="sxs-lookup"><span data-stu-id="4d64c-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4d64c-118">Ezután létrejön egy VPN-átjáró a virtuális központban 2 méretarányú egységben.</span><span class="sxs-lookup"><span data-stu-id="4d64c-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="4d64c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d64c-119">PARAMETERS</span></span>

### <span data-ttu-id="4d64c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d64c-120">-AsJob</span></span>
<span data-ttu-id="4d64c-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4d64c-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d64c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d64c-122">-DefaultProfile</span></span>
<span data-ttu-id="4d64c-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d64c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d64c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4d64c-124">-Name</span></span>
<span data-ttu-id="4d64c-125">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4d64c-125">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d64c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d64c-126">-ResourceGroupName</span></span>
<span data-ttu-id="4d64c-127">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4d64c-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d64c-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="4d64c-128">-Tag</span></span>
<span data-ttu-id="4d64c-129">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="4d64c-129">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4d64c-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="4d64c-130">-VirtualHub</span></span>
<span data-ttu-id="4d64c-131">A VirtualHubhoz, a VpnGatewayhez társítva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4d64c-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d64c-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="4d64c-132">-VirtualHubId</span></span>
<span data-ttu-id="4d64c-133">Annak a VirtualHubnak az azonosítóját, amelyhez a VpnGatewaynek társítva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4d64c-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d64c-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="4d64c-134">-VirtualHubName</span></span>
<span data-ttu-id="4d64c-135">Annak a VirtualHubnak az azonosítóját, amelyhez a VpnGatewaynek társítva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4d64c-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d64c-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4d64c-136">-VpnConnection</span></span>
<span data-ttu-id="4d64c-137">A VpnGatewayhez szükséges VpnConnections listája.</span><span class="sxs-lookup"><span data-stu-id="4d64c-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

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

### <span data-ttu-id="4d64c-138">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="4d64c-138">-VpnGatewayNatRule</span></span>
<span data-ttu-id="4d64c-139">A VpnGatewayhez társított VpnGatewayNatRules listája.</span><span class="sxs-lookup"><span data-stu-id="4d64c-139">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d64c-140">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4d64c-140">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="4d64c-141">A VpnGateway méretaránya.</span><span class="sxs-lookup"><span data-stu-id="4d64c-141">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d64c-142">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="4d64c-142">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="4d64c-143">Flag to enable Routing Preference Internet on this VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4d64c-143">Flag to enable Routing Preference Internet on this VpnGateway.</span></span>

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

### <span data-ttu-id="4d64c-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d64c-144">-Confirm</span></span>
<span data-ttu-id="4d64c-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4d64c-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d64c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d64c-146">-WhatIf</span></span>
<span data-ttu-id="4d64c-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4d64c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d64c-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d64c-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d64c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d64c-149">CommonParameters</span></span>
<span data-ttu-id="4d64c-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d64c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d64c-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d64c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d64c-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d64c-152">INPUTS</span></span>

### <span data-ttu-id="4d64c-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4d64c-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
### <span data-ttu-id="4d64c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="4d64c-154">System.String</span></span>
## <span data-ttu-id="4d64c-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d64c-155">OUTPUTS</span></span>

### <span data-ttu-id="4d64c-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4d64c-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>
## <span data-ttu-id="4d64c-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d64c-157">NOTES</span></span>

## <span data-ttu-id="4d64c-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d64c-158">RELATED LINKS</span></span>

[<span data-ttu-id="4d64c-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4d64c-159">Get-AzVpnGateway</span></span>]()

[<span data-ttu-id="4d64c-160">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4d64c-160">Remove-AzVpnGateway</span></span>]()

[<span data-ttu-id="4d64c-161">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4d64c-161">Update-AzVpnGateway</span></span>]()

