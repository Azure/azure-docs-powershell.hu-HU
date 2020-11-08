---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F3D44471-50F0-4737-9AF5-3DE7222EAF9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9aa386b47c02ed945cad63c00425534d68e66f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015485"
---
# <span data-ttu-id="8727a-101">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8727a-101">Remove-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8727a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8727a-102">SYNOPSIS</span></span>
<span data-ttu-id="8727a-103">Virtuális hálózati átjáró kapcsolatának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8727a-103">Removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="8727a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8727a-104">SYNTAX</span></span>

```
Remove-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8727a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8727a-105">DESCRIPTION</span></span>
<span data-ttu-id="8727a-106">A **Remove-AzureVirtualNetworkGatewayConnection** parancsmag eltávolítja a virtuális hálózati átjáró kapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="8727a-106">The **Remove-AzureVirtualNetworkGatewayConnection** cmdlet removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="8727a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8727a-107">EXAMPLES</span></span>

## <span data-ttu-id="8727a-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8727a-108">PARAMETERS</span></span>

### <span data-ttu-id="8727a-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="8727a-109">-ConnectedEntityId</span></span>
<span data-ttu-id="8727a-110">Egy csatlakoztatott entitás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8727a-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="8727a-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="8727a-111">-GatewayId</span></span>
<span data-ttu-id="8727a-112">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8727a-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="8727a-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="8727a-113">-Profile</span></span>
<span data-ttu-id="8727a-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8727a-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8727a-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8727a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8727a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8727a-116">CommonParameters</span></span>
<span data-ttu-id="8727a-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8727a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8727a-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8727a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8727a-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8727a-119">INPUTS</span></span>

## <span data-ttu-id="8727a-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8727a-120">OUTPUTS</span></span>

## <span data-ttu-id="8727a-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8727a-121">NOTES</span></span>

## <span data-ttu-id="8727a-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8727a-122">RELATED LINKS</span></span>

[<span data-ttu-id="8727a-123">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8727a-123">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="8727a-124">Új – AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8727a-124">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="8727a-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8727a-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


