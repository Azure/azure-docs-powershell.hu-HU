---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: ac93b104a8ccc1afbeb41bcd11910b76f7d4039f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184068"
---
# <span data-ttu-id="18991-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18991-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="18991-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18991-102">SYNOPSIS</span></span>
<span data-ttu-id="18991-103">Módosítja egy helyi hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="18991-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="18991-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18991-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway> [-AddressPrefix <String[]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18991-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="18991-105">DESCRIPTION</span></span>
<span data-ttu-id="18991-106">A **set-AzLocalNetworkGateway** parancsmag egy helyi hálózati átjárót módosít.</span><span class="sxs-lookup"><span data-stu-id="18991-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="18991-107">Példák</span><span class="sxs-lookup"><span data-stu-id="18991-107">EXAMPLES</span></span>

### <span data-ttu-id="18991-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="18991-108">Example 1</span></span>
<span data-ttu-id="18991-109">Meglévő átjáró konfigurációjának beállítása</span><span class="sxs-lookup"><span data-stu-id="18991-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzLocalNetworkGateway -LocalNetworkGateway $lgw

Name                     : myLocalGW
ResourceGroupName        : TestRG1
Location                 : westus
Id                       : /subscriptions/81ab786c-56eb-4a4d-bb5f-f60329772466/resourceGroups/TestRG1/providers/Microso
                           ft.Network/localNetworkGateways/myLocalGW
Etag                     : W/"d2de6968-315e-411d-a4b8-a8c335abe61b"
ResourceGuid             : 393acf8b-dbb8-4b08-a9ea-c714570710e1
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : 1.2.3.4
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

## <span data-ttu-id="18991-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18991-110">PARAMETERS</span></span>

### <span data-ttu-id="18991-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="18991-111">-AddressPrefix</span></span>
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

### <span data-ttu-id="18991-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18991-112">-AsJob</span></span>
<span data-ttu-id="18991-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="18991-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18991-114">-ASN</span><span class="sxs-lookup"><span data-stu-id="18991-114">-Asn</span></span>
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

### <span data-ttu-id="18991-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="18991-115">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="18991-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18991-116">-DefaultProfile</span></span>
<span data-ttu-id="18991-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18991-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18991-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18991-118">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="18991-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="18991-119">-PeerWeight</span></span>
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

### <span data-ttu-id="18991-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18991-120">CommonParameters</span></span>
<span data-ttu-id="18991-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18991-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18991-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18991-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18991-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18991-123">INPUTS</span></span>

### <span data-ttu-id="18991-124">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18991-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="18991-125">System. string []</span><span class="sxs-lookup"><span data-stu-id="18991-125">System.String[]</span></span>

### <span data-ttu-id="18991-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="18991-126">System.UInt32</span></span>

### <span data-ttu-id="18991-127">System. String</span><span class="sxs-lookup"><span data-stu-id="18991-127">System.String</span></span>

### <span data-ttu-id="18991-128">System. Int32</span><span class="sxs-lookup"><span data-stu-id="18991-128">System.Int32</span></span>

## <span data-ttu-id="18991-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18991-129">OUTPUTS</span></span>

### <span data-ttu-id="18991-130">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18991-130">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="18991-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18991-131">NOTES</span></span>

## <span data-ttu-id="18991-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18991-132">RELATED LINKS</span></span>

[<span data-ttu-id="18991-133">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18991-133">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="18991-134">Új – AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18991-134">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="18991-135">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18991-135">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)
