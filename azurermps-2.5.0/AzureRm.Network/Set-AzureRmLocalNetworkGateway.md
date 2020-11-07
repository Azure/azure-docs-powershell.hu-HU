---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f01fd5c1c6694c8d16ab34e6aad9f6a52463c726
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850317"
---
# <span data-ttu-id="7a494-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a494-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="7a494-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a494-102">SYNOPSIS</span></span>
<span data-ttu-id="7a494-103">Módosítja egy helyi hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="7a494-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a494-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a494-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a494-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a494-105">DESCRIPTION</span></span>
<span data-ttu-id="7a494-106">A **set-AzureRmLocalNetworkGateway** parancsmag egy helyi hálózati átjárót módosít.</span><span class="sxs-lookup"><span data-stu-id="7a494-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="7a494-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7a494-107">EXAMPLES</span></span>

### <span data-ttu-id="7a494-108">1:</span><span class="sxs-lookup"><span data-stu-id="7a494-108">1:</span></span>
```

```

## <span data-ttu-id="7a494-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a494-109">PARAMETERS</span></span>

### <span data-ttu-id="7a494-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7a494-110">-AddressPrefix</span></span>
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

### <span data-ttu-id="7a494-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a494-111">-AsJob</span></span>
<span data-ttu-id="7a494-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7a494-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a494-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="7a494-113">-Asn</span></span>
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

### <span data-ttu-id="7a494-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="7a494-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="7a494-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a494-115">-DefaultProfile</span></span>
<span data-ttu-id="7a494-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a494-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a494-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a494-117">-LocalNetworkGateway</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a494-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="7a494-118">-PeerWeight</span></span>
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

### <span data-ttu-id="7a494-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a494-119">CommonParameters</span></span>
<span data-ttu-id="7a494-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a494-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a494-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a494-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a494-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a494-122">INPUTS</span></span>

### <span data-ttu-id="7a494-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a494-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="7a494-124">A ' LocalNetworkGateway ' paraméter az "PSLocalNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7a494-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="7a494-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a494-125">OUTPUTS</span></span>

### <span data-ttu-id="7a494-126">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a494-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="7a494-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a494-127">NOTES</span></span>

## <span data-ttu-id="7a494-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a494-128">RELATED LINKS</span></span>

[<span data-ttu-id="7a494-129">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a494-129">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="7a494-130">Új – AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a494-130">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="7a494-131">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a494-131">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


