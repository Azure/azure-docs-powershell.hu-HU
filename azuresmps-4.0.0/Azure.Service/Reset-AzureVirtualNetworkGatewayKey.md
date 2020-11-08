---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4F1E69B8-15FB-495F-B910-04E450D3215F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a5b53f909b840a761d40f79a311fb61b7e2337b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016088"
---
# <span data-ttu-id="04d60-101">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="04d60-101">Reset-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="04d60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04d60-102">SYNOPSIS</span></span>
<span data-ttu-id="04d60-103">Virtuális hálózati átjáró kulcsának alaphelyzetbe állítása.</span><span class="sxs-lookup"><span data-stu-id="04d60-103">Resets a virtual network gateway key.</span></span>

## <span data-ttu-id="04d60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04d60-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -keyLength <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="04d60-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="04d60-105">DESCRIPTION</span></span>
<span data-ttu-id="04d60-106">A **reset-AzureVirtualNetworkGatewayKey** parancsmag visszaállítja a virtuális hálózati átjáró kulcsát.</span><span class="sxs-lookup"><span data-stu-id="04d60-106">The **Reset-AzureVirtualNetworkGatewayKey** cmdlet resets a virtual network gateway key.</span></span>

## <span data-ttu-id="04d60-107">Példák</span><span class="sxs-lookup"><span data-stu-id="04d60-107">EXAMPLES</span></span>

## <span data-ttu-id="04d60-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04d60-108">PARAMETERS</span></span>

### <span data-ttu-id="04d60-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="04d60-109">-ConnectedEntityId</span></span>
<span data-ttu-id="04d60-110">Egy csatlakoztatott entitás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="04d60-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="04d60-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="04d60-111">-GatewayId</span></span>
<span data-ttu-id="04d60-112">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="04d60-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="04d60-113">-Karakter hossza</span><span class="sxs-lookup"><span data-stu-id="04d60-113">-keyLength</span></span>
<span data-ttu-id="04d60-114">A kulcs hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="04d60-114">Specifies the key length.</span></span>

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

### <span data-ttu-id="04d60-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="04d60-115">-Profile</span></span>
<span data-ttu-id="04d60-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="04d60-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="04d60-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="04d60-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="04d60-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d60-118">CommonParameters</span></span>
<span data-ttu-id="04d60-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04d60-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d60-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04d60-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d60-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04d60-121">INPUTS</span></span>

## <span data-ttu-id="04d60-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04d60-122">OUTPUTS</span></span>

## <span data-ttu-id="04d60-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04d60-123">NOTES</span></span>

## <span data-ttu-id="04d60-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04d60-124">RELATED LINKS</span></span>

[<span data-ttu-id="04d60-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="04d60-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="04d60-126">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="04d60-126">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)
