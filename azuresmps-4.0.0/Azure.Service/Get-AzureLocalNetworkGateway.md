---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7A50D71-1D23-431E-9ACD-3A0D1BDC2B17
online version: ''
schema: 2.0.0
ms.openlocfilehash: e6c1bfbf98b1d53d9c5ba5867b2948625f8a5f3b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016339"
---
# <span data-ttu-id="b9057-101">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9057-101">Get-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="b9057-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9057-102">SYNOPSIS</span></span>
<span data-ttu-id="b9057-103">Helyi hálózati átjárót kap.</span><span class="sxs-lookup"><span data-stu-id="b9057-103">Gets a local network gateway.</span></span>

## <span data-ttu-id="b9057-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9057-104">SYNTAX</span></span>

```
Get-AzureLocalNetworkGateway [-GatewayId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b9057-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9057-105">DESCRIPTION</span></span>
<span data-ttu-id="b9057-106">A **Get-AzureLocalNetworkGateway** parancsmag helyi hálózati átjárót kap.</span><span class="sxs-lookup"><span data-stu-id="b9057-106">The **Get-AzureLocalNetworkGateway** cmdlet gets a local network gateway.</span></span>

## <span data-ttu-id="b9057-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b9057-107">EXAMPLES</span></span>

## <span data-ttu-id="b9057-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9057-108">PARAMETERS</span></span>

### <span data-ttu-id="b9057-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="b9057-109">-GatewayId</span></span>
<span data-ttu-id="b9057-110">A beolvasott átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9057-110">Specifies the ID of the gateway to get.</span></span>

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

### <span data-ttu-id="b9057-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="b9057-111">-Profile</span></span>
<span data-ttu-id="b9057-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b9057-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b9057-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b9057-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b9057-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9057-114">CommonParameters</span></span>
<span data-ttu-id="b9057-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9057-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9057-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9057-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9057-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9057-117">INPUTS</span></span>

## <span data-ttu-id="b9057-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9057-118">OUTPUTS</span></span>

## <span data-ttu-id="b9057-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9057-119">NOTES</span></span>

## <span data-ttu-id="b9057-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9057-120">RELATED LINKS</span></span>

[<span data-ttu-id="b9057-121">Új – AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9057-121">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="b9057-122">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9057-122">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)

[<span data-ttu-id="b9057-123">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9057-123">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)
