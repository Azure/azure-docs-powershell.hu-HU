---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8099942A-B6EB-4C01-9F57-378B0EB7B3C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c933b716095392a215543cfc61d334cd347835
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015437"
---
# <span data-ttu-id="98434-101">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="98434-101">Set-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="98434-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98434-102">SYNOPSIS</span></span>
<span data-ttu-id="98434-103">Egy Azure virtuális hálózati átjáró kulcsát állítja be.</span><span class="sxs-lookup"><span data-stu-id="98434-103">Sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="98434-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98434-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="98434-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98434-105">DESCRIPTION</span></span>
<span data-ttu-id="98434-106">A **set-AzureVirtualNetworkGatewayKey** parancsmag az Azure virtuális hálózati átjáró kulcsát állítja be.</span><span class="sxs-lookup"><span data-stu-id="98434-106">The **Set-AzureVirtualNetworkGatewayKey** cmdlet sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="98434-107">Példák</span><span class="sxs-lookup"><span data-stu-id="98434-107">EXAMPLES</span></span>

## <span data-ttu-id="98434-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98434-108">PARAMETERS</span></span>

### <span data-ttu-id="98434-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="98434-109">-ConnectedEntityId</span></span>
<span data-ttu-id="98434-110">Egy csatlakoztatott entitás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="98434-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="98434-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="98434-111">-GatewayId</span></span>
<span data-ttu-id="98434-112">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="98434-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="98434-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="98434-113">-Profile</span></span>
<span data-ttu-id="98434-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="98434-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="98434-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="98434-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="98434-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="98434-116">-SharedKey</span></span>
<span data-ttu-id="98434-117">Egy megosztott kulcsot ad meg.</span><span class="sxs-lookup"><span data-stu-id="98434-117">Specifies a shared key.</span></span>

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

### <span data-ttu-id="98434-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98434-118">CommonParameters</span></span>
<span data-ttu-id="98434-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98434-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98434-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98434-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98434-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98434-121">INPUTS</span></span>

## <span data-ttu-id="98434-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98434-122">OUTPUTS</span></span>

## <span data-ttu-id="98434-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98434-123">NOTES</span></span>

## <span data-ttu-id="98434-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98434-124">RELATED LINKS</span></span>

[<span data-ttu-id="98434-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="98434-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="98434-126">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="98434-126">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)


