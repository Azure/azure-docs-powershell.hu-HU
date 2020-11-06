---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 8d2b3c6c15a48407b138fa26778bdf906b5a7a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494808"
---
# <span data-ttu-id="3ad18-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ad18-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="3ad18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ad18-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad18-103">Módosítja egy helyi hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="3ad18-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ad18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ad18-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ad18-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ad18-105">DESCRIPTION</span></span>
<span data-ttu-id="3ad18-106">A **set-AzureRmLocalNetworkGateway** parancsmag egy helyi hálózati átjárót módosít.</span><span class="sxs-lookup"><span data-stu-id="3ad18-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="3ad18-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3ad18-107">EXAMPLES</span></span>

## <span data-ttu-id="3ad18-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ad18-108">PARAMETERS</span></span>

### <span data-ttu-id="3ad18-109">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3ad18-109">-AddressPrefix</span></span>
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

### <span data-ttu-id="3ad18-110">-ASN</span><span class="sxs-lookup"><span data-stu-id="3ad18-110">-Asn</span></span>
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

### <span data-ttu-id="3ad18-111">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="3ad18-111">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="3ad18-112">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ad18-112">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad18-113">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="3ad18-113">-PeerWeight</span></span>
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

### <span data-ttu-id="3ad18-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad18-114">-DefaultProfile</span></span>
<span data-ttu-id="3ad18-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ad18-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ad18-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad18-116">CommonParameters</span></span>
<span data-ttu-id="3ad18-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ad18-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad18-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ad18-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad18-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ad18-119">INPUTS</span></span>

### <span data-ttu-id="3ad18-120">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ad18-120">PSLocalNetworkGateway</span></span>
<span data-ttu-id="3ad18-121">A ' LocalNetworkGateway ' paraméter az "PSLocalNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3ad18-121">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="3ad18-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ad18-122">OUTPUTS</span></span>

### <span data-ttu-id="3ad18-123">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ad18-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="3ad18-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ad18-124">NOTES</span></span>

## <span data-ttu-id="3ad18-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ad18-125">RELATED LINKS</span></span>

[<span data-ttu-id="3ad18-126">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ad18-126">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="3ad18-127">Új – AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ad18-127">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="3ad18-128">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ad18-128">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


