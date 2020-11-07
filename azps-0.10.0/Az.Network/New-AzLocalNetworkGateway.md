---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 37255dfda50d7c055aad6941bbf417d1aa852d35
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841322"
---
# <span data-ttu-id="1a4d7-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a4d7-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="1a4d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a4d7-102">SYNOPSIS</span></span>
<span data-ttu-id="1a4d7-103">Helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="1a4d7-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="1a4d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a4d7-104">SYNTAX</span></span>

```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a4d7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a4d7-105">DESCRIPTION</span></span>
<span data-ttu-id="1a4d7-106">A helyi hálózat átjárója a helyszíni VPN-eszközt jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="1a4d7-107">A **New-AzLocalNetworkGateway** parancsmag a helyszíni hálózat neve, az erőforráscsoport neve, a hely és az IP-cím, valamint a helyszíni hálózat, amely az Azure-hoz csatlakozik, és a helyszíni hálózat címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-107">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="1a4d7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1a4d7-108">EXAMPLES</span></span>

### <span data-ttu-id="1a4d7-109">1: helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="1a4d7-109">1: Create a Local Network Gateway</span></span>
```
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="1a4d7-110">A helyi hálózati átjáró objektumát hozza létre a "myLocalGW" nevű erőforráscsoport "myRG" nevű erőforráscsoporthoz a "Nyugat-amerikai" néven az "23.99.221.164" IP-címmel és a "10.5.51.0/24" előtaggal.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="1a4d7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a4d7-111">PARAMETERS</span></span>

### <span data-ttu-id="1a4d7-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1a4d7-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="1a4d7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a4d7-113">-AsJob</span></span>
<span data-ttu-id="1a4d7-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1a4d7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a4d7-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="1a4d7-115">-Asn</span></span>
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

### <span data-ttu-id="1a4d7-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="1a4d7-116">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a4d7-117">-DefaultProfile</span></span>
<span data-ttu-id="1a4d7-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a4d7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1a4d7-119">-Force</span></span>
<span data-ttu-id="1a4d7-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1a4d7-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="1a4d7-121">-GatewayIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4d7-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="1a4d7-122">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4d7-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1a4d7-123">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4d7-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="1a4d7-124">-PeerWeight</span></span>
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

### <span data-ttu-id="1a4d7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a4d7-125">-ResourceGroupName</span></span>
<span data-ttu-id="1a4d7-126">Azt az erőforráscsoport-csoportot adja meg, amelyhez a helyi hálózat átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-126">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4d7-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="1a4d7-127">-Tag</span></span>
<span data-ttu-id="1a4d7-128">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1a4d7-129">Példa:</span><span class="sxs-lookup"><span data-stu-id="1a4d7-129">For example:</span></span>

<span data-ttu-id="1a4d7-130">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="1a4d7-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4d7-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1a4d7-131">-Confirm</span></span>
<span data-ttu-id="1a4d7-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a4d7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a4d7-133">-WhatIf</span></span>
<span data-ttu-id="1a4d7-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a4d7-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a4d7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a4d7-136">CommonParameters</span></span>
<span data-ttu-id="1a4d7-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a4d7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a4d7-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a4d7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a4d7-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a4d7-139">INPUTS</span></span>

## <span data-ttu-id="1a4d7-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a4d7-140">OUTPUTS</span></span>

### <span data-ttu-id="1a4d7-141">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a4d7-141">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="1a4d7-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a4d7-142">NOTES</span></span>

## <span data-ttu-id="1a4d7-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a4d7-143">RELATED LINKS</span></span>

[<span data-ttu-id="1a4d7-144">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a4d7-144">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="1a4d7-145">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a4d7-145">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="1a4d7-146">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a4d7-146">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
