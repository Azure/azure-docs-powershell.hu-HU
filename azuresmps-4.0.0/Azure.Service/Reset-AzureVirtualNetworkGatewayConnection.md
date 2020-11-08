---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 09642B94-E888-4A22-9E8E-62109DB9394E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f42a788f29f8546e6f402f1685f4c91aa3d7e5cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016089"
---
# <span data-ttu-id="7b382-101">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7b382-101">Reset-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7b382-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b382-102">SYNOPSIS</span></span>
<span data-ttu-id="7b382-103">Virtuális hálózati átjáró kapcsolatának alaphelyzetbe állítása.</span><span class="sxs-lookup"><span data-stu-id="7b382-103">Resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="7b382-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b382-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 -RoutingWeight <Int32> [-SharedKey <String>] [-EnableBgp <Boolean>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b382-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b382-105">DESCRIPTION</span></span>
<span data-ttu-id="7b382-106">A **reset-AzureVirtualNetworkGatewayConnection** parancsmag visszaállítja a virtuális hálózati átjáró kapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="7b382-106">The **Reset-AzureVirtualNetworkGatewayConnection** cmdlet resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="7b382-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7b382-107">EXAMPLES</span></span>

## <span data-ttu-id="7b382-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b382-108">PARAMETERS</span></span>

### <span data-ttu-id="7b382-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="7b382-109">-ConnectedEntityId</span></span>
<span data-ttu-id="7b382-110">Egy csatlakoztatott entitás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b382-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="7b382-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7b382-111">-EnableBgp</span></span>
<span data-ttu-id="7b382-112">Engedélyezi a Border Gateway Protocol (BGP) protokollt.</span><span class="sxs-lookup"><span data-stu-id="7b382-112">Enables Border Gateway Protocol (BGP).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b382-113">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="7b382-113">-GatewayId</span></span>
<span data-ttu-id="7b382-114">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b382-114">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="7b382-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="7b382-115">-Profile</span></span>
<span data-ttu-id="7b382-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="7b382-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7b382-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="7b382-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7b382-118">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="7b382-118">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b382-119">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7b382-119">-SharedKey</span></span>
<span data-ttu-id="7b382-120">Egy megosztott kulcsot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7b382-120">Specifies a shared key.</span></span>

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

### <span data-ttu-id="7b382-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b382-121">CommonParameters</span></span>
<span data-ttu-id="7b382-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b382-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b382-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b382-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b382-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b382-124">INPUTS</span></span>

## <span data-ttu-id="7b382-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b382-125">OUTPUTS</span></span>

## <span data-ttu-id="7b382-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b382-126">NOTES</span></span>

## <span data-ttu-id="7b382-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b382-127">RELATED LINKS</span></span>

[<span data-ttu-id="7b382-128">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7b382-128">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7b382-129">Új – AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7b382-129">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7b382-130">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7b382-130">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)


