---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 88AB3621-7C80-41BA-BE49-4F8F9C46BCF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fb0fa13cb5ea155b945505fd3f99c28494c5dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016523"
---
# <span data-ttu-id="8554d-101">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8554d-101">Get-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8554d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8554d-102">SYNOPSIS</span></span>
<span data-ttu-id="8554d-103">Virtuális hálózati átjáró-kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="8554d-103">Gets a virtual network gateway connection.</span></span>

## <span data-ttu-id="8554d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8554d-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayConnection [-GatewayId <String>] [-ConnectedEntityId <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8554d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8554d-105">DESCRIPTION</span></span>
<span data-ttu-id="8554d-106">A **Get-AzureVirtualNetworkGatewayConnection** parancsmag Azure virtuális hálózati átjáró-kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="8554d-106">The **Get-AzureVirtualNetworkGatewayConnection** cmdlet gets an Azure virtual network gateway connection.</span></span>

## <span data-ttu-id="8554d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8554d-107">EXAMPLES</span></span>

## <span data-ttu-id="8554d-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8554d-108">PARAMETERS</span></span>

### <span data-ttu-id="8554d-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="8554d-109">-ConnectedEntityId</span></span>
<span data-ttu-id="8554d-110">Egy csatlakoztatott entitás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8554d-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="8554d-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="8554d-111">-GatewayId</span></span>
<span data-ttu-id="8554d-112">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8554d-112">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="8554d-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="8554d-113">-Profile</span></span>
<span data-ttu-id="8554d-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8554d-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8554d-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8554d-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8554d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8554d-116">CommonParameters</span></span>
<span data-ttu-id="8554d-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8554d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8554d-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8554d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8554d-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8554d-119">INPUTS</span></span>

## <span data-ttu-id="8554d-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8554d-120">OUTPUTS</span></span>

## <span data-ttu-id="8554d-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8554d-121">NOTES</span></span>

## <span data-ttu-id="8554d-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8554d-122">RELATED LINKS</span></span>

[<span data-ttu-id="8554d-123">Új – AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8554d-123">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="8554d-124">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8554d-124">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="8554d-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8554d-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)
