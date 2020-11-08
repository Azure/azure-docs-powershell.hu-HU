---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9F2CADC2-1053-404F-96DA-D992AA39D0FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d410a521d1fd4032b647650b12cfc764aa52e0ad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015486"
---
# <span data-ttu-id="42265-101">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42265-101">Remove-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="42265-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42265-102">SYNOPSIS</span></span>
<span data-ttu-id="42265-103">Virtuális hálózati átjáró eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="42265-103">Removes a virtual network gateway.</span></span>

## <span data-ttu-id="42265-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42265-104">SYNTAX</span></span>

```
Remove-AzureVirtualNetworkGateway -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="42265-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="42265-105">DESCRIPTION</span></span>
<span data-ttu-id="42265-106">A **Remove-AzureVirtualNetworkGateway** parancsmag eltávolítja a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="42265-106">The **Remove-AzureVirtualNetworkGateway** cmdlet removes a virtual network gateway.</span></span>

## <span data-ttu-id="42265-107">Példák</span><span class="sxs-lookup"><span data-stu-id="42265-107">EXAMPLES</span></span>

## <span data-ttu-id="42265-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42265-108">PARAMETERS</span></span>

### <span data-ttu-id="42265-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="42265-109">-GatewayId</span></span>
<span data-ttu-id="42265-110">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42265-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="42265-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="42265-111">-Profile</span></span>
<span data-ttu-id="42265-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="42265-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="42265-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="42265-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42265-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42265-114">CommonParameters</span></span>
<span data-ttu-id="42265-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42265-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42265-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42265-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42265-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42265-117">INPUTS</span></span>

## <span data-ttu-id="42265-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42265-118">OUTPUTS</span></span>

## <span data-ttu-id="42265-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42265-119">NOTES</span></span>

## <span data-ttu-id="42265-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42265-120">RELATED LINKS</span></span>

[<span data-ttu-id="42265-121">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42265-121">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="42265-122">Új – AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42265-122">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="42265-123">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42265-123">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)


