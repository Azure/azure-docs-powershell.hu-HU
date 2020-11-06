---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 3acfbf1462a1f0ae75d95b9f3976c46fd07676f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501731"
---
# <span data-ttu-id="e73bd-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e73bd-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="e73bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e73bd-102">SYNOPSIS</span></span>
<span data-ttu-id="e73bd-103">Helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="e73bd-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e73bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e73bd-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e73bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e73bd-105">DESCRIPTION</span></span>
<span data-ttu-id="e73bd-106">A helyi hálózat átjárója a helyszíni VPN-eszközt jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="e73bd-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="e73bd-107">A **New-AzureRmLocalNetworkGateway** parancsmag a helyszíni hálózat neve, az erőforráscsoport neve, a hely és az IP-cím, valamint a helyszíni hálózat, amely az Azure-hoz csatlakozik, és a helyszíni hálózat címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e73bd-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="e73bd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e73bd-108">EXAMPLES</span></span>

### <span data-ttu-id="e73bd-109">1: helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="e73bd-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="e73bd-110">A helyi hálózati átjáró objektumát hozza létre a "myLocalGW" nevű erőforráscsoport "myRG" nevű erőforráscsoporthoz a "Nyugat-amerikai" néven az "23.99.221.164" IP-címmel és a "10.5.51.0/24" előtaggal.</span><span class="sxs-lookup"><span data-stu-id="e73bd-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="e73bd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e73bd-111">PARAMETERS</span></span>

### <span data-ttu-id="e73bd-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e73bd-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="e73bd-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="e73bd-113">-Asn</span></span>
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

### <span data-ttu-id="e73bd-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="e73bd-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="e73bd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e73bd-115">-Force</span></span>
<span data-ttu-id="e73bd-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e73bd-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e73bd-117">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="e73bd-117">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="e73bd-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="e73bd-118">-Location</span></span>
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

### <span data-ttu-id="e73bd-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e73bd-119">-Name</span></span>
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

### <span data-ttu-id="e73bd-120">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="e73bd-120">-PeerWeight</span></span>
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

### <span data-ttu-id="e73bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e73bd-121">-ResourceGroupName</span></span>
<span data-ttu-id="e73bd-122">Azt az erőforráscsoport-csoportot adja meg, amelyhez a helyi hálózat átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="e73bd-122">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="e73bd-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="e73bd-123">-Tag</span></span>
<span data-ttu-id="e73bd-124">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="e73bd-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e73bd-125">Példa:</span><span class="sxs-lookup"><span data-stu-id="e73bd-125">For example:</span></span>

<span data-ttu-id="e73bd-126">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="e73bd-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e73bd-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e73bd-127">-Confirm</span></span>
<span data-ttu-id="e73bd-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e73bd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e73bd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e73bd-129">-WhatIf</span></span>
<span data-ttu-id="e73bd-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e73bd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e73bd-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e73bd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e73bd-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e73bd-132">-DefaultProfile</span></span>
<span data-ttu-id="e73bd-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e73bd-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e73bd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e73bd-134">CommonParameters</span></span>
<span data-ttu-id="e73bd-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e73bd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e73bd-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e73bd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e73bd-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e73bd-137">INPUTS</span></span>

## <span data-ttu-id="e73bd-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e73bd-138">OUTPUTS</span></span>

### <span data-ttu-id="e73bd-139">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e73bd-139">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="e73bd-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e73bd-140">NOTES</span></span>

## <span data-ttu-id="e73bd-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e73bd-141">RELATED LINKS</span></span>

[<span data-ttu-id="e73bd-142">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e73bd-142">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="e73bd-143">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e73bd-143">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="e73bd-144">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e73bd-144">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
