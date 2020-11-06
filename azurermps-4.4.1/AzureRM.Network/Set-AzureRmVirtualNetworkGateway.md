---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 41c94d0dd8401399f360af89f1744cc10e900e1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497036"
---
# <span data-ttu-id="98015-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="98015-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="98015-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98015-102">SYNOPSIS</span></span>
<span data-ttu-id="98015-103">Virtuális hálózati átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="98015-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98015-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98015-104">SYNTAX</span></span>

### <span data-ttu-id="98015-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98015-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98015-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="98015-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98015-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="98015-107">DESCRIPTION</span></span>
<span data-ttu-id="98015-108">A **set-AzureRmVirtualNetworkGateway** parancsmag frissíti a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="98015-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="98015-109">Példák</span><span class="sxs-lookup"><span data-stu-id="98015-109">EXAMPLES</span></span>

### <span data-ttu-id="98015-110">Példa 1: a cél állapotának beállítása virtuális hálózati átjáróval</span><span class="sxs-lookup"><span data-stu-id="98015-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="98015-111">Az első parancs beolvassa a Gateway01 nevű virtuális hálózati átjárót, amely az erőforráscsoport ResourceGroup001 tartozik, és a nevet a $Gateway nevű változóra menti.</span><span class="sxs-lookup"><span data-stu-id="98015-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="98015-112">A második parancs az $Gateway változóban tárolt virtuális hálózati átjáró céljának állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="98015-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="98015-113">A parancs az ASN-1337 is beállítja.</span><span class="sxs-lookup"><span data-stu-id="98015-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="98015-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98015-114">PARAMETERS</span></span>

### <span data-ttu-id="98015-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="98015-115">-Asn</span></span>
<span data-ttu-id="98015-116">Annak a virtuális hálózati átjárónak az autonóm rendszerszámát adja meg, amely az IPsec-alagutakban a Border Gateway Protocol (BGP) munkamenetek beállításához használatos.</span><span class="sxs-lookup"><span data-stu-id="98015-116">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="98015-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98015-117">-DefaultProfile</span></span>
<span data-ttu-id="98015-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98015-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="98015-119">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="98015-119">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="98015-120">Letiltja az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="98015-120">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="98015-121">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="98015-121">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="98015-122">Engedélyezi az aktív aktív funkciókat.</span><span class="sxs-lookup"><span data-stu-id="98015-122">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="98015-123">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="98015-123">-GatewayDefaultSite</span></span>
<span data-ttu-id="98015-124">Itt adhatja meg, hogy milyen alapértelmezett webhely legyen használható a kényszerítő bújtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="98015-124">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="98015-125">Ha meg van adva egy alapértelmezett webhely, az átjáró virtuális magánhálózat (VPN) minden internetes forgalmát átirányítja az adott webhelyre.</span><span class="sxs-lookup"><span data-stu-id="98015-125">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="98015-126">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="98015-126">-GatewaySku</span></span>
<span data-ttu-id="98015-127">A virtuális hálózati átjáró készlet-megőrzési egységét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98015-127">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="98015-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="98015-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="98015-129">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="98015-129">Basic</span></span>
- <span data-ttu-id="98015-130">Standard</span><span class="sxs-lookup"><span data-stu-id="98015-130">Standard</span></span>
- <span data-ttu-id="98015-131">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="98015-131">HighPerformance</span></span>
- <span data-ttu-id="98015-132">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="98015-132">VpnGw1</span></span>
- <span data-ttu-id="98015-133">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="98015-133">VpnGw2</span></span>
- <span data-ttu-id="98015-134">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="98015-134">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98015-135">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="98015-135">-PeerWeight</span></span>
<span data-ttu-id="98015-136">Itt adhatja meg, hogy a virtuális hálózati átjárótól kapott, a BGP-ról származó összes útvonalhoz hozzáadott súly</span><span class="sxs-lookup"><span data-stu-id="98015-136">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="98015-137">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="98015-137">-RadiusServerAddress</span></span>
<span data-ttu-id="98015-138">P2S külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="98015-138">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="98015-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="98015-139">-RadiusServerSecret</span></span>
<span data-ttu-id="98015-140">P2S külső RADIUS-kiszolgáló titka.</span><span class="sxs-lookup"><span data-stu-id="98015-140">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="98015-141">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="98015-141">-VirtualNetworkGateway</span></span>
<span data-ttu-id="98015-142">Annak a virtuális hálózati átjáró objektumnak a meghatározása, amelynek alapján a módosítások le vannak kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="98015-142">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="98015-143">A virtuális hálózati átjáró objektum beszerzéséhez használhatja az Get-AzureRmVirtualNetworkGateway parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="98015-143">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="98015-144">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="98015-144">-VpnClientAddressPool</span></span>
<span data-ttu-id="98015-145">Azt a Címterület-címet adja meg, amelyre a parancsmag a VPN-ügyfél IP-címeinek hozzárendelését használja.</span><span class="sxs-lookup"><span data-stu-id="98015-145">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="98015-146">Ennek a virtuális hálózatnak vagy a helyszíni tartományoknak nem szabad átfedésben lennie.</span><span class="sxs-lookup"><span data-stu-id="98015-146">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="98015-147">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="98015-147">-VpnClientProtocol</span></span>
<span data-ttu-id="98015-148">A P2S VPN-ügyfél bújtatási protokolljainak listája</span><span class="sxs-lookup"><span data-stu-id="98015-148">A list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="98015-149">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="98015-149">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="98015-150">A visszavont VPN-ügyfél tanúsítványainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="98015-150">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="98015-151">A VPN-ügyfél egy olyan tanúsítványt ad, amely megfelel az egyik ilyen elemnek.</span><span class="sxs-lookup"><span data-stu-id="98015-151">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="98015-152">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="98015-152">-VpnClientRootCertificates</span></span>
<span data-ttu-id="98015-153">A virtuális magánhálózati ügyfél-hitelesítéshez használni kívánt virtuális magánhálózati tanúsítványok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="98015-153">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="98015-154">A VPN-ügyfeleknek való csatlakozáskor az ilyen főtanúsítványokból származó tanúsítványokat kell bemutatnia.</span><span class="sxs-lookup"><span data-stu-id="98015-154">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="98015-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98015-155">-Confirm</span></span>
<span data-ttu-id="98015-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98015-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98015-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98015-157">-WhatIf</span></span>
<span data-ttu-id="98015-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98015-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98015-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98015-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98015-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98015-160">CommonParameters</span></span>
<span data-ttu-id="98015-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98015-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98015-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98015-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98015-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98015-163">INPUTS</span></span>

### <span data-ttu-id="98015-164">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="98015-164">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="98015-165">A ' VirtualNetworkGateway ' paraméter az "PSVirtualNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="98015-165">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="98015-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98015-166">OUTPUTS</span></span>

### <span data-ttu-id="98015-167">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="98015-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="98015-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98015-168">NOTES</span></span>
* <span data-ttu-id="98015-169">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="98015-169">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="98015-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98015-170">RELATED LINKS</span></span>

[<span data-ttu-id="98015-171">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="98015-171">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="98015-172">Új – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="98015-172">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="98015-173">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="98015-173">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="98015-174">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="98015-174">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="98015-175">Átméretezés-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="98015-175">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


