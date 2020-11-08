---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AD5F4D69-45AF-46FB-ADF0-59CEF9908EF7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d63ac418d2dcee97afef9ae5f351fb2c1eebece0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016086"
---
# <span data-ttu-id="168df-101">Resize-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="168df-101">Resize-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="168df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="168df-102">SYNOPSIS</span></span>
<span data-ttu-id="168df-103">Virtuális hálózati átjáró átméretezése</span><span class="sxs-lookup"><span data-stu-id="168df-103">Resizes a virtual network gateway.</span></span>

## <span data-ttu-id="168df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="168df-104">SYNTAX</span></span>

```
Resize-AzureVirtualNetworkGateway -GatewayId <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="168df-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="168df-105">DESCRIPTION</span></span>
<span data-ttu-id="168df-106">Az Resize-AzureVirtualNetworkGateway parancsmag átméretezi a virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="168df-106">The Resize-AzureVirtualNetworkGateway cmdlet resizes a virtual network gateway.</span></span>

## <span data-ttu-id="168df-107">Példák</span><span class="sxs-lookup"><span data-stu-id="168df-107">EXAMPLES</span></span>

## <span data-ttu-id="168df-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="168df-108">PARAMETERS</span></span>

### <span data-ttu-id="168df-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="168df-109">-GatewayId</span></span>
<span data-ttu-id="168df-110">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="168df-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="168df-111">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="168df-111">-GatewaySKU</span></span>
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

### <span data-ttu-id="168df-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="168df-112">-Profile</span></span>
<span data-ttu-id="168df-113">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="168df-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="168df-114">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="168df-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="168df-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="168df-115">CommonParameters</span></span>
<span data-ttu-id="168df-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="168df-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="168df-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="168df-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="168df-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="168df-118">INPUTS</span></span>

## <span data-ttu-id="168df-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="168df-119">OUTPUTS</span></span>

## <span data-ttu-id="168df-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="168df-120">NOTES</span></span>

## <span data-ttu-id="168df-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="168df-121">RELATED LINKS</span></span>

[<span data-ttu-id="168df-122">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="168df-122">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="168df-123">Új – AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="168df-123">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="168df-124">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="168df-124">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="168df-125">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="168df-125">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)


