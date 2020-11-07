---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 6576cedfa49d2ba2215d72b7f31ea85288f5cbda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669962"
---
# <span data-ttu-id="872b6-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="872b6-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="872b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="872b6-102">SYNOPSIS</span></span>
<span data-ttu-id="872b6-103">Virtuális hálózati átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="872b6-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="872b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="872b6-104">SYNTAX</span></span>

### <span data-ttu-id="872b6-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="872b6-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="872b6-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="872b6-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="872b6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="872b6-107">DESCRIPTION</span></span>
<span data-ttu-id="872b6-108">A **set-AzVirtualNetworkGateway** parancsmag frissíti a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="872b6-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="872b6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="872b6-109">EXAMPLES</span></span>

### <span data-ttu-id="872b6-110">Példa 1: virtuális hálózati átjáró ASN-es frissítése</span><span class="sxs-lookup"><span data-stu-id="872b6-110">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="872b6-111">Az első parancs beolvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és a második parancs $Gateway a második parancsban frissíti a $Gateway változóban tárolt virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="872b6-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="872b6-112">A parancs az ASN-1337 is beállítja.</span><span class="sxs-lookup"><span data-stu-id="872b6-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="872b6-113">2. példa: IPsec-házirend hozzáadása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="872b6-113">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="872b6-114">Az első parancs beolvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és $Gateway a második parancsban tárolja a VPN IPSec-házirend-objektumot meghatározott IPSec-paraméterekként.</span><span class="sxs-lookup"><span data-stu-id="872b6-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="872b6-115">A harmadik parancs az $Gateway változóban tárolt virtuális hálózati átjárót frissíti.</span><span class="sxs-lookup"><span data-stu-id="872b6-115">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="872b6-116">A parancs a virtuális hálózati átjárón a $vpnclientipsecpolicy objektumban megadott egyéni virtuális magánhálózati IPSec-házirendet is beállítja.</span><span class="sxs-lookup"><span data-stu-id="872b6-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="872b6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="872b6-117">PARAMETERS</span></span>

### <span data-ttu-id="872b6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="872b6-118">-AsJob</span></span>
<span data-ttu-id="872b6-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="872b6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="872b6-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="872b6-120">-Asn</span></span>
<span data-ttu-id="872b6-121">Annak a virtuális hálózati átjárónak az autonóm rendszerszámát adja meg, amely az IPsec-alagutakban a Border Gateway Protocol (BGP) munkamenetek beállításához használatos.</span><span class="sxs-lookup"><span data-stu-id="872b6-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="872b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872b6-122">-DefaultProfile</span></span>
<span data-ttu-id="872b6-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="872b6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="872b6-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="872b6-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="872b6-125">Letiltja az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="872b6-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="872b6-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="872b6-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="872b6-127">Engedélyezi az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="872b6-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="872b6-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="872b6-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="872b6-129">Itt adhatja meg, hogy milyen alapértelmezett webhely legyen használható a kényszerítő bújtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="872b6-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="872b6-130">Ha meg van adva egy alapértelmezett webhely, az átjáró virtuális magánhálózat (VPN) minden internetes forgalmát átirányítja az adott webhelyre.</span><span class="sxs-lookup"><span data-stu-id="872b6-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="872b6-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="872b6-131">-GatewaySku</span></span>
<span data-ttu-id="872b6-132">A virtuális hálózati átjáró készlet-megőrzési egységét adja meg.</span><span class="sxs-lookup"><span data-stu-id="872b6-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="872b6-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="872b6-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="872b6-134">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="872b6-134">Basic</span></span>
- <span data-ttu-id="872b6-135">Standard</span><span class="sxs-lookup"><span data-stu-id="872b6-135">Standard</span></span>
- <span data-ttu-id="872b6-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="872b6-136">HighPerformance</span></span>
- <span data-ttu-id="872b6-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="872b6-137">VpnGw1</span></span>
- <span data-ttu-id="872b6-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="872b6-138">VpnGw2</span></span>
- <span data-ttu-id="872b6-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="872b6-139">VpnGw3</span></span>
- <span data-ttu-id="872b6-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="872b6-140">VpnGw1AZ</span></span>
- <span data-ttu-id="872b6-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="872b6-141">VpnGw2AZ</span></span>
- <span data-ttu-id="872b6-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="872b6-142">VpnGw3AZ</span></span>
- <span data-ttu-id="872b6-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="872b6-143">ErGw1AZ</span></span>
- <span data-ttu-id="872b6-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="872b6-144">ErGw2AZ</span></span>
- <span data-ttu-id="872b6-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="872b6-145">ErGw3AZ</span></span>

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

### <span data-ttu-id="872b6-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="872b6-146">-PeerWeight</span></span>
<span data-ttu-id="872b6-147">Itt adhatja meg, hogy a virtuális hálózati átjárótól kapott, a BGP-ról származó összes útvonalhoz hozzáadott súly</span><span class="sxs-lookup"><span data-stu-id="872b6-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="872b6-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="872b6-148">-RadiusServerAddress</span></span>
<span data-ttu-id="872b6-149">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="872b6-149">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="872b6-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="872b6-150">-RadiusServerSecret</span></span>
<span data-ttu-id="872b6-151">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="872b6-151">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="872b6-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="872b6-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="872b6-153">Annak a virtuális hálózati átjáró objektumnak a meghatározása, amelynek alapján a módosítások le vannak kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="872b6-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="872b6-154">A virtuális hálózati átjáró objektum beszerzéséhez használhatja az Get-AzVirtualNetworkGateway parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="872b6-154">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="872b6-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="872b6-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="872b6-156">Azt a Címterület-címet adja meg, amelyre a parancsmag a VPN-ügyfél IP-címeinek hozzárendelését használja.</span><span class="sxs-lookup"><span data-stu-id="872b6-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="872b6-157">Ennek a virtuális hálózatnak vagy a helyszíni tartományoknak nem szabad átfedésben lennie.</span><span class="sxs-lookup"><span data-stu-id="872b6-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872b6-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="872b6-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="872b6-159">Az IPSec-házirendek listája az P2S VPN-ügyfél bújtatási protokolljaihoz.</span><span class="sxs-lookup"><span data-stu-id="872b6-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872b6-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="872b6-160">-VpnClientProtocol</span></span>
<span data-ttu-id="872b6-161">A P2S VPN-ügyfél bújtatási protokolljainak listája</span><span class="sxs-lookup"><span data-stu-id="872b6-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872b6-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="872b6-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="872b6-163">A visszavont VPN-ügyfél tanúsítványainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="872b6-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="872b6-164">A VPN-ügyfél egy olyan tanúsítványt ad, amely megfelel az egyik ilyen elemnek.</span><span class="sxs-lookup"><span data-stu-id="872b6-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872b6-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="872b6-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="872b6-166">A virtuális magánhálózati ügyfél-hitelesítéshez használni kívánt virtuális magánhálózati tanúsítványok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="872b6-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="872b6-167">A VPN-ügyfeleknek való csatlakozáskor az ilyen főtanúsítványokból származó tanúsítványokat kell bemutatnia.</span><span class="sxs-lookup"><span data-stu-id="872b6-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872b6-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="872b6-168">-Confirm</span></span>
<span data-ttu-id="872b6-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="872b6-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="872b6-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="872b6-170">-WhatIf</span></span>
<span data-ttu-id="872b6-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="872b6-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="872b6-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="872b6-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="872b6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872b6-173">CommonParameters</span></span>
<span data-ttu-id="872b6-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="872b6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872b6-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="872b6-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872b6-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="872b6-176">INPUTS</span></span>

### <span data-ttu-id="872b6-177">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="872b6-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="872b6-178">System. String</span><span class="sxs-lookup"><span data-stu-id="872b6-178">System.String</span></span>

### <span data-ttu-id="872b6-179">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="872b6-179">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="872b6-180">System. string []</span><span class="sxs-lookup"><span data-stu-id="872b6-180">System.String[]</span></span>

### <span data-ttu-id="872b6-181">Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="872b6-181">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="872b6-182">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="872b6-182">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="872b6-183">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="872b6-183">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="872b6-184">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="872b6-184">System.UInt32</span></span>

### <span data-ttu-id="872b6-185">System. Int32</span><span class="sxs-lookup"><span data-stu-id="872b6-185">System.Int32</span></span>

### <span data-ttu-id="872b6-186">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="872b6-186">System.Security.SecureString</span></span>

## <span data-ttu-id="872b6-187">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="872b6-187">OUTPUTS</span></span>

### <span data-ttu-id="872b6-188">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="872b6-188">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="872b6-189">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="872b6-189">NOTES</span></span>
* <span data-ttu-id="872b6-190">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="872b6-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="872b6-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="872b6-191">RELATED LINKS</span></span>

[<span data-ttu-id="872b6-192">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="872b6-192">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="872b6-193">Új – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="872b6-193">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="872b6-194">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="872b6-194">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="872b6-195">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="872b6-195">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="872b6-196">Átméretezés-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="872b6-196">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
