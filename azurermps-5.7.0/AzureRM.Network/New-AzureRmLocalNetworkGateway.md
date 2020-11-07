---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 6db2d9defaed434aa74f64d6f13af4f029edf482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672730"
---
# <span data-ttu-id="2ae5f-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2ae5f-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="2ae5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ae5f-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae5f-103">Helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="2ae5f-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ae5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ae5f-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ae5f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ae5f-105">DESCRIPTION</span></span>
<span data-ttu-id="2ae5f-106">A helyi hálózat átjárója a helyszíni VPN-eszközt jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="2ae5f-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="2ae5f-107">A **New-AzureRmLocalNetworkGateway** parancsmag a helyszíni hálózat neve, az erőforráscsoport neve, a hely és az IP-cím, valamint a helyszíni hálózat, amely az Azure-hoz csatlakozik, és a helyszíni hálózat címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ae5f-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="2ae5f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2ae5f-108">EXAMPLES</span></span>

### <span data-ttu-id="2ae5f-109">1: helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="2ae5f-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="2ae5f-110">A helyi hálózati átjáró objektumát hozza létre a "myLocalGW" nevű erőforráscsoport "myRG" nevű erőforráscsoporthoz a "Nyugat-amerikai" néven az "23.99.221.164" IP-címmel és a "10.5.51.0/24" előtaggal.</span><span class="sxs-lookup"><span data-stu-id="2ae5f-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="2ae5f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ae5f-111">PARAMETERS</span></span>

### <span data-ttu-id="2ae5f-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2ae5f-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="2ae5f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ae5f-113">-AsJob</span></span>
<span data-ttu-id="2ae5f-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2ae5f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ae5f-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="2ae5f-115">-Asn</span></span>
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

### <span data-ttu-id="2ae5f-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="2ae5f-116">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="2ae5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ae5f-117">-DefaultProfile</span></span>
<span data-ttu-id="2ae5f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ae5f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ae5f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2ae5f-119">-Force</span></span>
<span data-ttu-id="2ae5f-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2ae5f-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2ae5f-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="2ae5f-121">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="2ae5f-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="2ae5f-122">-Location</span></span>
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

### <span data-ttu-id="2ae5f-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ae5f-123">-Name</span></span>
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

### <span data-ttu-id="2ae5f-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="2ae5f-124">-PeerWeight</span></span>
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

### <span data-ttu-id="2ae5f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ae5f-125">-ResourceGroupName</span></span>
<span data-ttu-id="2ae5f-126">Azt az erőforráscsoport-csoportot adja meg, amelyhez a helyi hálózat átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="2ae5f-126">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="2ae5f-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="2ae5f-127">-Tag</span></span>
<span data-ttu-id="2ae5f-128">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="2ae5f-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2ae5f-129">Példa:</span><span class="sxs-lookup"><span data-stu-id="2ae5f-129">For example:</span></span>

<span data-ttu-id="2ae5f-130">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="2ae5f-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2ae5f-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2ae5f-131">-Confirm</span></span>
<span data-ttu-id="2ae5f-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ae5f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ae5f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ae5f-133">-WhatIf</span></span>
<span data-ttu-id="2ae5f-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2ae5f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ae5f-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ae5f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ae5f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae5f-136">CommonParameters</span></span>
<span data-ttu-id="2ae5f-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ae5f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae5f-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ae5f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae5f-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ae5f-139">INPUTS</span></span>

### <span data-ttu-id="2ae5f-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="2ae5f-140">None</span></span>
<span data-ttu-id="2ae5f-141">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2ae5f-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ae5f-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ae5f-142">OUTPUTS</span></span>

### <span data-ttu-id="2ae5f-143">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2ae5f-143">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="2ae5f-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ae5f-144">NOTES</span></span>

## <span data-ttu-id="2ae5f-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ae5f-145">RELATED LINKS</span></span>

[<span data-ttu-id="2ae5f-146">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2ae5f-146">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="2ae5f-147">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2ae5f-147">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="2ae5f-148">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2ae5f-148">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
