---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 013da22d02f091d49e9780585bb8648c9c895ad7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494448"
---
# <span data-ttu-id="86b2c-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86b2c-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="86b2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="86b2c-103">Virtuális hálózati átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="86b2c-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86b2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86b2c-104">SYNTAX</span></span>

### <span data-ttu-id="86b2c-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86b2c-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86b2c-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="86b2c-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86b2c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="86b2c-107">DESCRIPTION</span></span>
<span data-ttu-id="86b2c-108">A **set-AzureRmVirtualNetworkGateway** parancsmag frissíti a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="86b2c-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="86b2c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="86b2c-109">EXAMPLES</span></span>

### <span data-ttu-id="86b2c-110">Példa 1: a cél állapotának beállítása virtuális hálózati átjáróval</span><span class="sxs-lookup"><span data-stu-id="86b2c-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="86b2c-111">Az első parancs beolvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és a nevet a $Gateway nevű változóra menti.</span><span class="sxs-lookup"><span data-stu-id="86b2c-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="86b2c-112">A második parancs az $Gateway változóban tárolt virtuális hálózati átjáró céljának állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="86b2c-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="86b2c-113">A parancs az ASN-1337 is beállítja.</span><span class="sxs-lookup"><span data-stu-id="86b2c-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="86b2c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86b2c-114">PARAMETERS</span></span>

### <span data-ttu-id="86b2c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86b2c-115">-AsJob</span></span>
<span data-ttu-id="86b2c-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="86b2c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86b2c-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="86b2c-117">-Asn</span></span>
<span data-ttu-id="86b2c-118">Annak a virtuális hálózati átjárónak az autonóm rendszerszámát adja meg, amely az IPsec-alagutakban a Border Gateway Protocol (BGP) munkamenetek beállításához használatos.</span><span class="sxs-lookup"><span data-stu-id="86b2c-118">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b2c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86b2c-119">-DefaultProfile</span></span>
<span data-ttu-id="86b2c-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86b2c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86b2c-121">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="86b2c-121">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="86b2c-122">Letiltja az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="86b2c-122">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="86b2c-123">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="86b2c-123">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="86b2c-124">Engedélyezi az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="86b2c-124">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="86b2c-125">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="86b2c-125">-GatewayDefaultSite</span></span>
<span data-ttu-id="86b2c-126">Itt adhatja meg, hogy milyen alapértelmezett webhely legyen használható a kényszerítő bújtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="86b2c-126">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="86b2c-127">Ha meg van adva egy alapértelmezett webhely, az átjáró virtuális magánhálózat (VPN) minden internetes forgalmát átirányítja az adott webhelyre.</span><span class="sxs-lookup"><span data-stu-id="86b2c-127">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b2c-128">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="86b2c-128">-GatewaySku</span></span>
<span data-ttu-id="86b2c-129">A virtuális hálózati átjáró készlet-megőrzési egységét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86b2c-129">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="86b2c-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="86b2c-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="86b2c-131">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="86b2c-131">Basic</span></span>
- <span data-ttu-id="86b2c-132">Standard</span><span class="sxs-lookup"><span data-stu-id="86b2c-132">Standard</span></span>
- <span data-ttu-id="86b2c-133">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="86b2c-133">HighPerformance</span></span>
- <span data-ttu-id="86b2c-134">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="86b2c-134">VpnGw1</span></span>
- <span data-ttu-id="86b2c-135">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="86b2c-135">VpnGw2</span></span>
- <span data-ttu-id="86b2c-136">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="86b2c-136">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b2c-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="86b2c-137">-PeerWeight</span></span>
<span data-ttu-id="86b2c-138">Itt adhatja meg, hogy a virtuális hálózati átjárótól kapott, a BGP-ról származó összes útvonalhoz hozzáadott súly</span><span class="sxs-lookup"><span data-stu-id="86b2c-138">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b2c-139">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="86b2c-139">-RadiusServerAddress</span></span>
<span data-ttu-id="86b2c-140">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="86b2c-140">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b2c-141">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="86b2c-141">-RadiusServerSecret</span></span>
<span data-ttu-id="86b2c-142">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="86b2c-142">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b2c-143">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86b2c-143">-VirtualNetworkGateway</span></span>
<span data-ttu-id="86b2c-144">Annak a virtuális hálózati átjáró objektumnak a meghatározása, amelynek alapján a módosítások le vannak kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="86b2c-144">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="86b2c-145">A virtuális hálózati átjáró objektum beszerzéséhez használhatja az Get-AzureRmVirtualNetworkGateway parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="86b2c-145">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86b2c-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="86b2c-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="86b2c-147">Azt a Címterület-címet adja meg, amelyre a parancsmag a VPN-ügyfél IP-címeinek hozzárendelését használja.</span><span class="sxs-lookup"><span data-stu-id="86b2c-147">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="86b2c-148">Ennek a virtuális hálózatnak vagy a helyszíni tartományoknak nem szabad átfedésben lennie.</span><span class="sxs-lookup"><span data-stu-id="86b2c-148">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="86b2c-149">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="86b2c-149">-VpnClientProtocol</span></span>
<span data-ttu-id="86b2c-150">A P2S VPN-ügyfél bújtatási protokolljainak listája</span><span class="sxs-lookup"><span data-stu-id="86b2c-150">A list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86b2c-151">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="86b2c-151">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="86b2c-152">A visszavont VPN-ügyfél tanúsítványainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="86b2c-152">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="86b2c-153">A VPN-ügyfél egy olyan tanúsítványt ad, amely megfelel az egyik ilyen elemnek.</span><span class="sxs-lookup"><span data-stu-id="86b2c-153">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="86b2c-154">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="86b2c-154">-VpnClientRootCertificates</span></span>
<span data-ttu-id="86b2c-155">A virtuális magánhálózati ügyfél-hitelesítéshez használni kívánt virtuális magánhálózati tanúsítványok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="86b2c-155">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="86b2c-156">A VPN-ügyfeleknek való csatlakozáskor az ilyen főtanúsítványokból származó tanúsítványokat kell bemutatnia.</span><span class="sxs-lookup"><span data-stu-id="86b2c-156">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="86b2c-157">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86b2c-157">-Confirm</span></span>
<span data-ttu-id="86b2c-158">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86b2c-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86b2c-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86b2c-159">-WhatIf</span></span>
<span data-ttu-id="86b2c-160">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86b2c-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86b2c-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86b2c-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86b2c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b2c-162">CommonParameters</span></span>
<span data-ttu-id="86b2c-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86b2c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b2c-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86b2c-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b2c-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86b2c-165">INPUTS</span></span>

### <span data-ttu-id="86b2c-166">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86b2c-166">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="86b2c-167">A ' VirtualNetworkGateway ' paraméter az "PSVirtualNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="86b2c-167">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="86b2c-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86b2c-168">OUTPUTS</span></span>

### <span data-ttu-id="86b2c-169">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86b2c-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="86b2c-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86b2c-170">NOTES</span></span>
* <span data-ttu-id="86b2c-171">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="86b2c-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="86b2c-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86b2c-172">RELATED LINKS</span></span>

[<span data-ttu-id="86b2c-173">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86b2c-173">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="86b2c-174">Új – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86b2c-174">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="86b2c-175">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86b2c-175">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="86b2c-176">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86b2c-176">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="86b2c-177">Átméretezés-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="86b2c-177">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


