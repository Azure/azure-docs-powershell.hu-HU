---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: a33fb510e351a8f1c762801947cf4bbac9a66e28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499708"
---
# <span data-ttu-id="308d9-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="308d9-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="308d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="308d9-102">SYNOPSIS</span></span>
<span data-ttu-id="308d9-103">Módosítja egy helyi hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="308d9-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="308d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="308d9-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="308d9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="308d9-105">DESCRIPTION</span></span>
<span data-ttu-id="308d9-106">A **set-AzureRmLocalNetworkGateway** parancsmag egy helyi hálózati átjárót módosít.</span><span class="sxs-lookup"><span data-stu-id="308d9-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="308d9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="308d9-107">EXAMPLES</span></span>

## <span data-ttu-id="308d9-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="308d9-108">PARAMETERS</span></span>

### <span data-ttu-id="308d9-109">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="308d9-109">-AddressPrefix</span></span>
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

### <span data-ttu-id="308d9-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="308d9-110">-AsJob</span></span>
<span data-ttu-id="308d9-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="308d9-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="308d9-112">-ASN</span><span class="sxs-lookup"><span data-stu-id="308d9-112">-Asn</span></span>
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

### <span data-ttu-id="308d9-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="308d9-113">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="308d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="308d9-114">-DefaultProfile</span></span>
<span data-ttu-id="308d9-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="308d9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="308d9-116">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="308d9-116">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="308d9-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="308d9-117">-PeerWeight</span></span>
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

### <span data-ttu-id="308d9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308d9-118">CommonParameters</span></span>
<span data-ttu-id="308d9-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="308d9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308d9-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="308d9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308d9-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="308d9-121">INPUTS</span></span>

### <span data-ttu-id="308d9-122">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="308d9-122">PSLocalNetworkGateway</span></span>
<span data-ttu-id="308d9-123">A ' LocalNetworkGateway ' paraméter az "PSLocalNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="308d9-123">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="308d9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="308d9-124">OUTPUTS</span></span>

### <span data-ttu-id="308d9-125">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="308d9-125">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="308d9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="308d9-126">NOTES</span></span>

## <span data-ttu-id="308d9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="308d9-127">RELATED LINKS</span></span>

[<span data-ttu-id="308d9-128">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="308d9-128">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="308d9-129">Új – AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="308d9-129">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="308d9-130">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="308d9-130">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


