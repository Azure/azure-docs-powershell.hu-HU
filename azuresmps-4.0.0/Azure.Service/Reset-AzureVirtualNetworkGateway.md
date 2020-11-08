---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: CD735391-62A8-40EC-B2F1-9044DC0676CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc46fb250a7bc76d05193ea231c81d61668e853
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016090"
---
# <span data-ttu-id="55c94-101">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55c94-101">Reset-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="55c94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55c94-102">SYNOPSIS</span></span>
<span data-ttu-id="55c94-103">Virtuális hálózati átjáró alaphelyzetbe állítása.</span><span class="sxs-lookup"><span data-stu-id="55c94-103">Resets a virtual network gateway.</span></span>

## <span data-ttu-id="55c94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55c94-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGateway -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="55c94-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55c94-105">DESCRIPTION</span></span>
<span data-ttu-id="55c94-106">A **reset-AzureVirtualNetworkGateway** parancsmag visszaállítja a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="55c94-106">The **Reset-AzureVirtualNetworkGateway** cmdlet resets a virtual network gateway.</span></span>

## <span data-ttu-id="55c94-107">Példák</span><span class="sxs-lookup"><span data-stu-id="55c94-107">EXAMPLES</span></span>

## <span data-ttu-id="55c94-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55c94-108">PARAMETERS</span></span>

### <span data-ttu-id="55c94-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="55c94-109">-GatewayId</span></span>
<span data-ttu-id="55c94-110">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="55c94-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="55c94-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="55c94-111">-Profile</span></span>
<span data-ttu-id="55c94-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="55c94-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="55c94-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="55c94-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="55c94-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c94-114">CommonParameters</span></span>
<span data-ttu-id="55c94-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55c94-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c94-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c94-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c94-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55c94-117">INPUTS</span></span>

## <span data-ttu-id="55c94-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55c94-118">OUTPUTS</span></span>

## <span data-ttu-id="55c94-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55c94-119">NOTES</span></span>

## <span data-ttu-id="55c94-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55c94-120">RELATED LINKS</span></span>

[<span data-ttu-id="55c94-121">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55c94-121">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="55c94-122">Új – AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55c94-122">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="55c94-123">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55c94-123">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="55c94-124">Átméretezés-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="55c94-124">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)


