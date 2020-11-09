---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302715"
---
# <span data-ttu-id="1dc3f-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1dc3f-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="1dc3f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1dc3f-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc3f-103">Helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="1dc3f-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="1dc3f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1dc3f-104">SYNTAX</span></span>

### <span data-ttu-id="1dc3f-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="1dc3f-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc3f-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="1dc3f-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dc3f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1dc3f-107">DESCRIPTION</span></span>
<span data-ttu-id="1dc3f-108">A helyi hálózat átjárója a helyszíni VPN-eszközt jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="1dc3f-109">A **New-AzLocalNetworkGateway** parancsmag a helyszíni hálózat neve, az erőforráscsoport neve, a hely és az IP-cím, valamint a helyszíni hálózat, amely az Azure-hoz csatlakozik, és a helyszíni hálózat címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="1dc3f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1dc3f-110">EXAMPLES</span></span>

### <span data-ttu-id="1dc3f-111">Példa 1: helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="1dc3f-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="1dc3f-112">A helyi hálózati átjáró objektumát hozza létre a "myLocalGW" nevű erőforráscsoport "myRG" nevű erőforráscsoporthoz a "Nyugat-amerikai" néven az "23.99.221.164" IP-címmel és a "10.5.51.0/24" előtaggal.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="1dc3f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1dc3f-113">PARAMETERS</span></span>

### <span data-ttu-id="1dc3f-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1dc3f-114">-AddressPrefix</span></span>
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

### <span data-ttu-id="1dc3f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dc3f-115">-AsJob</span></span>
<span data-ttu-id="1dc3f-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1dc3f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dc3f-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="1dc3f-117">-Asn</span></span>
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

### <span data-ttu-id="1dc3f-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="1dc3f-118">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc3f-119">-DefaultProfile</span></span>
<span data-ttu-id="1dc3f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dc3f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1dc3f-121">-Force</span></span>
<span data-ttu-id="1dc3f-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1dc3f-123">-FQDN</span><span class="sxs-lookup"><span data-stu-id="1dc3f-123">-Fqdn</span></span>
<span data-ttu-id="1dc3f-124">A helyi hálózati átjáró FQDN-je.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3f-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="1dc3f-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3f-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="1dc3f-126">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3f-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1dc3f-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3f-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="1dc3f-128">-PeerWeight</span></span>
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

### <span data-ttu-id="1dc3f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc3f-129">-ResourceGroupName</span></span>
<span data-ttu-id="1dc3f-130">Azt az erőforráscsoport-csoportot adja meg, amelyhez a helyi hálózat átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-130">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3f-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="1dc3f-131">-Tag</span></span>
<span data-ttu-id="1dc3f-132">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1dc3f-133">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="1dc3f-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3f-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1dc3f-134">-Confirm</span></span>
<span data-ttu-id="1dc3f-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc3f-136">-WhatIf</span></span>
<span data-ttu-id="1dc3f-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc3f-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc3f-139">CommonParameters</span></span>
<span data-ttu-id="1dc3f-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1dc3f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc3f-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1dc3f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc3f-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1dc3f-142">INPUTS</span></span>

### <span data-ttu-id="1dc3f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1dc3f-143">System.String</span></span>

### <span data-ttu-id="1dc3f-144">System. string []</span><span class="sxs-lookup"><span data-stu-id="1dc3f-144">System.String[]</span></span>

### <span data-ttu-id="1dc3f-145">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="1dc3f-145">System.UInt32</span></span>

### <span data-ttu-id="1dc3f-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1dc3f-146">System.Int32</span></span>

### <span data-ttu-id="1dc3f-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1dc3f-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1dc3f-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1dc3f-148">OUTPUTS</span></span>

### <span data-ttu-id="1dc3f-149">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1dc3f-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="1dc3f-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1dc3f-150">NOTES</span></span>

## <span data-ttu-id="1dc3f-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1dc3f-151">RELATED LINKS</span></span>

[<span data-ttu-id="1dc3f-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1dc3f-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="1dc3f-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1dc3f-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="1dc3f-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1dc3f-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
