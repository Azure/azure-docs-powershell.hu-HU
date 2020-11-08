---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: E3C0C3AA-3941-469E-A6CC-A92ADD7377B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bf6824219879af52549d7815d65dcb502a2a752
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016185"
---
# <span data-ttu-id="704a6-101">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="704a6-101">New-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="704a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="704a6-102">SYNOPSIS</span></span>
<span data-ttu-id="704a6-103">Azure virtuális átjáró hálózati kapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="704a6-103">Creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="704a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="704a6-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGatewayConnection -ConnectedEntityId <String> -GatewayConnectionName <String>
 -GatewayConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>]
 -VirtualNetworkGatewayId <String> [-EnableBgp <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="704a6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="704a6-105">DESCRIPTION</span></span>
<span data-ttu-id="704a6-106">A **New-AzureVirtualNetworkGatewayConnection** parancsmag az Azure virtuális átjáró hálózati kapcsolatát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="704a6-106">The **New-AzureVirtualNetworkGatewayConnection** cmdlet creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="704a6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="704a6-107">EXAMPLES</span></span>

## <span data-ttu-id="704a6-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="704a6-108">PARAMETERS</span></span>

### <span data-ttu-id="704a6-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="704a6-109">-ConnectedEntityId</span></span>
<span data-ttu-id="704a6-110">Egy csatlakoztatott entitás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="704a6-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="704a6-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="704a6-111">-EnableBgp</span></span>
<span data-ttu-id="704a6-112">Engedélyezi a Border Gateway Protocol (BGP) protokollt.</span><span class="sxs-lookup"><span data-stu-id="704a6-112">Enables Border Gateway Protocol (BGP).</span></span>

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

### <span data-ttu-id="704a6-113">-GatewayConnectionName</span><span class="sxs-lookup"><span data-stu-id="704a6-113">-GatewayConnectionName</span></span>
<span data-ttu-id="704a6-114">Az átjáró kapcsolatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="704a6-114">Specifies a name for the gateway connection.</span></span>

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

### <span data-ttu-id="704a6-115">-GatewayConnectionType</span><span class="sxs-lookup"><span data-stu-id="704a6-115">-GatewayConnectionType</span></span>
<span data-ttu-id="704a6-116">Az átjáró-kapcsolat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="704a6-116">Specifies the type of gateway connection.</span></span>

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

### <span data-ttu-id="704a6-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="704a6-117">-Profile</span></span>
<span data-ttu-id="704a6-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="704a6-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="704a6-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="704a6-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="704a6-120">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="704a6-120">-RoutingWeight</span></span>
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

### <span data-ttu-id="704a6-121">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="704a6-121">-SharedKey</span></span>
<span data-ttu-id="704a6-122">Egy megosztott kulcsot ad meg.</span><span class="sxs-lookup"><span data-stu-id="704a6-122">Specifies a shared key.</span></span>

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

### <span data-ttu-id="704a6-123">-VirtualNetworkGatewayId</span><span class="sxs-lookup"><span data-stu-id="704a6-123">-VirtualNetworkGatewayId</span></span>
<span data-ttu-id="704a6-124">A virtuális hálózati átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="704a6-124">Specifies the ID of a virtual network gateway.</span></span>

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

### <span data-ttu-id="704a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704a6-125">CommonParameters</span></span>
<span data-ttu-id="704a6-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="704a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704a6-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="704a6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704a6-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="704a6-128">INPUTS</span></span>

## <span data-ttu-id="704a6-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="704a6-129">OUTPUTS</span></span>

## <span data-ttu-id="704a6-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="704a6-130">NOTES</span></span>

## <span data-ttu-id="704a6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="704a6-131">RELATED LINKS</span></span>

[<span data-ttu-id="704a6-132">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="704a6-132">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="704a6-133">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="704a6-133">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="704a6-134">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="704a6-134">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


