---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9F9E4639-A557-4BD8-88C2-894F6C848C4A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa54a7bd236bb561b3de4b9c2a3c0a2710deb61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016007"
---
# <span data-ttu-id="d2798-101">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d2798-101">New-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="d2798-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2798-102">SYNOPSIS</span></span>
<span data-ttu-id="d2798-103">Azure helyi hálózati átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d2798-103">creates an Azure local network gateway.</span></span>

## <span data-ttu-id="d2798-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2798-104">SYNTAX</span></span>

```
New-AzureLocalNetworkGateway -GatewayName <String> -IpAddress <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d2798-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2798-105">DESCRIPTION</span></span>
<span data-ttu-id="d2798-106">A **New-AzureLocalNetworkGateway** parancsmag Azure helyi hálózati átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d2798-106">The **New-AzureLocalNetworkGateway** cmdlet creates an Azure local network gateway.</span></span>

## <span data-ttu-id="d2798-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d2798-107">EXAMPLES</span></span>

## <span data-ttu-id="d2798-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2798-108">PARAMETERS</span></span>

### <span data-ttu-id="d2798-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="d2798-109">-AddressSpace</span></span>
<span data-ttu-id="d2798-110">Itt adhatja meg a Címterület címét.</span><span class="sxs-lookup"><span data-stu-id="d2798-110">Specifies the address space.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2798-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="d2798-111">-Asn</span></span>
<span data-ttu-id="d2798-112">Az autonóm rendszer számát adja meg (ASN).</span><span class="sxs-lookup"><span data-stu-id="d2798-112">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2798-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="d2798-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="d2798-114">A Border Gateway Protocol (BGP) társközi címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2798-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2798-115">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="d2798-115">-GatewayName</span></span>
<span data-ttu-id="d2798-116">Az átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2798-116">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="d2798-117">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="d2798-117">-IpAddress</span></span>
<span data-ttu-id="d2798-118">Az IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2798-118">Specifies the IP address.</span></span>

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

### <span data-ttu-id="d2798-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="d2798-119">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2798-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="d2798-120">-Profile</span></span>
<span data-ttu-id="d2798-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d2798-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d2798-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d2798-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2798-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2798-123">CommonParameters</span></span>
<span data-ttu-id="d2798-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2798-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2798-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2798-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2798-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2798-126">INPUTS</span></span>

## <span data-ttu-id="d2798-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2798-127">OUTPUTS</span></span>

## <span data-ttu-id="d2798-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2798-128">NOTES</span></span>

## <span data-ttu-id="d2798-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2798-129">RELATED LINKS</span></span>

[<span data-ttu-id="d2798-130">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d2798-130">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="d2798-131">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d2798-131">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)

[<span data-ttu-id="d2798-132">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d2798-132">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)


