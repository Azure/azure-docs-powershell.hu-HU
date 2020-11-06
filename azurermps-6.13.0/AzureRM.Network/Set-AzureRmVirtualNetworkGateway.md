---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 1884dd461c0433c4f6a68bf906f56653ca960e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499467"
---
# <span data-ttu-id="043f6-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="043f6-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="043f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="043f6-102">SYNOPSIS</span></span>
<span data-ttu-id="043f6-103">Virtuális hálózati átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="043f6-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="043f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="043f6-104">SYNTAX</span></span>

### <span data-ttu-id="043f6-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="043f6-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="043f6-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="043f6-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="043f6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="043f6-107">DESCRIPTION</span></span>
<span data-ttu-id="043f6-108">A **set-AzureRmVirtualNetworkGateway** parancsmag frissíti a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="043f6-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="043f6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="043f6-109">EXAMPLES</span></span>

### <span data-ttu-id="043f6-110">Példa 1: a cél állapotának beállítása virtuális hálózati átjáróval</span><span class="sxs-lookup"><span data-stu-id="043f6-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="043f6-111">Az első parancs be$Gateway olvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancs a második parancsra állítja be a $Gateway változó ban tárolt virtuális hálózati átjáró céljának állapotát.</span><span class="sxs-lookup"><span data-stu-id="043f6-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="043f6-112">A parancs az ASN-1337 is beállítja.</span><span class="sxs-lookup"><span data-stu-id="043f6-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="043f6-113">2. példa: a cél állapot beállítása virtuális hálózati átjáróként</span><span class="sxs-lookup"><span data-stu-id="043f6-113">Example 2: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="043f6-114">Az első parancs beolvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és $Gateway a második parancsban tárolja a VPN IPSec-házirend-objektumot meghatározott IPSec-paraméterekként.</span><span class="sxs-lookup"><span data-stu-id="043f6-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="043f6-115">A harmadik parancs a $Gateway változóban tárolt virtuális hálózati átjáró céljának állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="043f6-115">The third command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="043f6-116">A parancs a virtuális hálózati átjárón a $vpnclientipsecpolicy objektumban megadott egyéni virtuális magánhálózati IPSec-házirendet is beállítja.</span><span class="sxs-lookup"><span data-stu-id="043f6-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="043f6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="043f6-117">PARAMETERS</span></span>

### <span data-ttu-id="043f6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="043f6-118">-AsJob</span></span>
<span data-ttu-id="043f6-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="043f6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="043f6-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="043f6-120">-Asn</span></span>
<span data-ttu-id="043f6-121">Annak a virtuális hálózati átjárónak az autonóm rendszerszámát adja meg, amely az IPsec-alagutakban a Border Gateway Protocol (BGP) munkamenetek beállításához használatos.</span><span class="sxs-lookup"><span data-stu-id="043f6-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="043f6-122">-DefaultProfile</span></span>
<span data-ttu-id="043f6-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="043f6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="043f6-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="043f6-125">Letiltja az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="043f6-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="043f6-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="043f6-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="043f6-127">Engedélyezi az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="043f6-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="043f6-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="043f6-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="043f6-129">Itt adhatja meg, hogy milyen alapértelmezett webhely legyen használható a kényszerítő bújtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="043f6-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="043f6-130">Ha meg van adva egy alapértelmezett webhely, az átjáró virtuális magánhálózat (VPN) minden internetes forgalmát átirányítja az adott webhelyre.</span><span class="sxs-lookup"><span data-stu-id="043f6-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="043f6-131">-GatewaySku</span></span>
<span data-ttu-id="043f6-132">A virtuális hálózati átjáró készlet-megőrzési egységét adja meg.</span><span class="sxs-lookup"><span data-stu-id="043f6-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="043f6-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="043f6-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="043f6-134">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="043f6-134">Basic</span></span>
- <span data-ttu-id="043f6-135">Standard</span><span class="sxs-lookup"><span data-stu-id="043f6-135">Standard</span></span>
- <span data-ttu-id="043f6-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="043f6-136">HighPerformance</span></span>
- <span data-ttu-id="043f6-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="043f6-137">VpnGw1</span></span>
- <span data-ttu-id="043f6-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="043f6-138">VpnGw2</span></span>
- <span data-ttu-id="043f6-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="043f6-139">VpnGw3</span></span>
- <span data-ttu-id="043f6-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="043f6-140">VpnGw1AZ</span></span>
- <span data-ttu-id="043f6-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="043f6-141">VpnGw2AZ</span></span>
- <span data-ttu-id="043f6-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="043f6-142">VpnGw3AZ</span></span>
- <span data-ttu-id="043f6-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="043f6-143">ErGw1AZ</span></span>
- <span data-ttu-id="043f6-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="043f6-144">ErGw2AZ</span></span>
- <span data-ttu-id="043f6-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="043f6-145">ErGw3AZ</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="043f6-146">-PeerWeight</span></span>
<span data-ttu-id="043f6-147">Itt adhatja meg, hogy a virtuális hálózati átjárótól kapott, a BGP-ról származó összes útvonalhoz hozzáadott súly</span><span class="sxs-lookup"><span data-stu-id="043f6-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="043f6-148">-RadiusServerAddress</span></span>
<span data-ttu-id="043f6-149">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="043f6-149">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="043f6-150">-RadiusServerSecret</span></span>
<span data-ttu-id="043f6-151">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="043f6-151">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="043f6-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="043f6-153">Annak a virtuális hálózati átjáró objektumnak a meghatározása, amelynek alapján a módosítások le vannak kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="043f6-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="043f6-154">A virtuális hálózati átjáró objektum beszerzéséhez használhatja az Get-AzureRmVirtualNetworkGateway parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="043f6-154">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="043f6-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="043f6-156">Azt a Címterület-címet adja meg, amelyre a parancsmag a VPN-ügyfél IP-címeinek hozzárendelését használja.</span><span class="sxs-lookup"><span data-stu-id="043f6-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="043f6-157">Ennek a virtuális hálózatnak vagy a helyszíni tartományoknak nem szabad átfedésben lennie.</span><span class="sxs-lookup"><span data-stu-id="043f6-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="043f6-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="043f6-159">Az IPSec-házirendek listája az P2S VPN-ügyfél bújtatási protokolljaihoz.</span><span class="sxs-lookup"><span data-stu-id="043f6-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="043f6-160">-VpnClientProtocol</span></span>
<span data-ttu-id="043f6-161">A P2S VPN-ügyfél bújtatási protokolljainak listája</span><span class="sxs-lookup"><span data-stu-id="043f6-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="043f6-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="043f6-163">A visszavont VPN-ügyfél tanúsítványainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="043f6-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="043f6-164">A VPN-ügyfél egy olyan tanúsítványt ad, amely megfelel az egyik ilyen elemnek.</span><span class="sxs-lookup"><span data-stu-id="043f6-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="043f6-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="043f6-166">A virtuális magánhálózati ügyfél-hitelesítéshez használni kívánt virtuális magánhálózati tanúsítványok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="043f6-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="043f6-167">A VPN-ügyfeleknek való csatlakozáskor az ilyen főtanúsítványokból származó tanúsítványokat kell bemutatnia.</span><span class="sxs-lookup"><span data-stu-id="043f6-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043f6-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="043f6-168">-Confirm</span></span>
<span data-ttu-id="043f6-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="043f6-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="043f6-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="043f6-170">-WhatIf</span></span>
<span data-ttu-id="043f6-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="043f6-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="043f6-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="043f6-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="043f6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="043f6-173">CommonParameters</span></span>
<span data-ttu-id="043f6-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="043f6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="043f6-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="043f6-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="043f6-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="043f6-176">INPUTS</span></span>

### <span data-ttu-id="043f6-177">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="043f6-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="043f6-178">Paraméterek: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="043f6-178">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="043f6-179">System. String</span><span class="sxs-lookup"><span data-stu-id="043f6-179">System.String</span></span>

### <span data-ttu-id="043f6-180">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="043f6-180">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="043f6-181">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="043f6-181">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="043f6-182">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="043f6-182">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="043f6-183">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="043f6-183">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="043f6-184">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSIpsecPolicy, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="043f6-184">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="043f6-185">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="043f6-185">System.UInt32</span></span>

### <span data-ttu-id="043f6-186">System. Int32</span><span class="sxs-lookup"><span data-stu-id="043f6-186">System.Int32</span></span>

### <span data-ttu-id="043f6-187">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="043f6-187">System.Security.SecureString</span></span>

## <span data-ttu-id="043f6-188">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="043f6-188">OUTPUTS</span></span>

### <span data-ttu-id="043f6-189">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="043f6-189">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="043f6-190">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="043f6-190">NOTES</span></span>
* <span data-ttu-id="043f6-191">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="043f6-191">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="043f6-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="043f6-192">RELATED LINKS</span></span>

[<span data-ttu-id="043f6-193">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="043f6-193">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="043f6-194">Új – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="043f6-194">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="043f6-195">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="043f6-195">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="043f6-196">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="043f6-196">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="043f6-197">Átméretezés-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="043f6-197">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


