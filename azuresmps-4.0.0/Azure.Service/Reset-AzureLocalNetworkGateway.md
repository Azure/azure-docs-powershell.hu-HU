---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0E4D44EE-BF28-46FE-B2FA-D35C1651016F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3940a5e6fc69ebee02f3e0de963bc87f790f8860
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015472"
---
# <span data-ttu-id="ace38-101">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ace38-101">Reset-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="ace38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ace38-102">SYNOPSIS</span></span>
<span data-ttu-id="ace38-103">Visszaállít egy helyi hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="ace38-103">Resets a local network gateway.</span></span>

## <span data-ttu-id="ace38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ace38-104">SYNTAX</span></span>

```
Reset-AzureLocalNetworkGateway -GatewayId <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ace38-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ace38-105">DESCRIPTION</span></span>
<span data-ttu-id="ace38-106">A **reset-AzureLocalNetworkGateway** parancsmag visszaállítja a helyi hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="ace38-106">The **Reset-AzureLocalNetworkGateway** cmdlet resets a local network gateway.</span></span>

## <span data-ttu-id="ace38-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ace38-107">EXAMPLES</span></span>

## <span data-ttu-id="ace38-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ace38-108">PARAMETERS</span></span>

### <span data-ttu-id="ace38-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="ace38-109">-AddressSpace</span></span>
<span data-ttu-id="ace38-110">Itt adhatja meg a Címterület címét.</span><span class="sxs-lookup"><span data-stu-id="ace38-110">Specifies the address space.</span></span>

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

### <span data-ttu-id="ace38-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="ace38-111">-Asn</span></span>
<span data-ttu-id="ace38-112">Az autonóm rendszer számát adja meg (ASN).</span><span class="sxs-lookup"><span data-stu-id="ace38-112">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="ace38-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="ace38-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="ace38-114">A Border Gateway Protocol (BGP) társközi címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ace38-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="ace38-115">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="ace38-115">-GatewayId</span></span>
<span data-ttu-id="ace38-116">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ace38-116">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="ace38-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="ace38-117">-PeerWeight</span></span>
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

### <span data-ttu-id="ace38-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="ace38-118">-Profile</span></span>
<span data-ttu-id="ace38-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ace38-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ace38-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ace38-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ace38-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace38-121">CommonParameters</span></span>
<span data-ttu-id="ace38-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ace38-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace38-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace38-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace38-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ace38-124">INPUTS</span></span>

## <span data-ttu-id="ace38-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ace38-125">OUTPUTS</span></span>

## <span data-ttu-id="ace38-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ace38-126">NOTES</span></span>

## <span data-ttu-id="ace38-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ace38-127">RELATED LINKS</span></span>

[<span data-ttu-id="ace38-128">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ace38-128">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="ace38-129">Új – AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ace38-129">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="ace38-130">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ace38-130">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)


