---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 425008DB-9761-42F1-8D6D-F35757A3CA6C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37aa0718c4faa637b16ccde61f5e5b241bb9aa92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016515"
---
# <span data-ttu-id="62322-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="62322-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="62322-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62322-102">SYNOPSIS</span></span>
<span data-ttu-id="62322-103">Egy Azure virtuális hálózati átjáró IPsec-paramétereit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="62322-103">Gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="62322-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62322-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="62322-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62322-105">DESCRIPTION</span></span>
<span data-ttu-id="62322-106">A **Get-AzureVirtualNetworkGatewayIPsecParameters** parancsmag egy Azure virtuális hálózati átjáró IPSec-paramétereit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="62322-106">The **Get-AzureVirtualNetworkGatewayIPsecParameters** cmdlet gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="62322-107">Példák</span><span class="sxs-lookup"><span data-stu-id="62322-107">EXAMPLES</span></span>

## <span data-ttu-id="62322-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62322-108">PARAMETERS</span></span>

### <span data-ttu-id="62322-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="62322-109">-ConnectedEntityId</span></span>
<span data-ttu-id="62322-110">A csatlakoztatott entitiy AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="62322-110">Specifies the ID of a connected entitiy.</span></span>

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

### <span data-ttu-id="62322-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="62322-111">-GatewayId</span></span>
<span data-ttu-id="62322-112">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="62322-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="62322-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="62322-113">-Profile</span></span>
<span data-ttu-id="62322-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="62322-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="62322-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="62322-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="62322-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62322-116">CommonParameters</span></span>
<span data-ttu-id="62322-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62322-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62322-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62322-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62322-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62322-119">INPUTS</span></span>

## <span data-ttu-id="62322-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62322-120">OUTPUTS</span></span>

## <span data-ttu-id="62322-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62322-121">NOTES</span></span>

## <span data-ttu-id="62322-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62322-122">RELATED LINKS</span></span>

[<span data-ttu-id="62322-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="62322-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Set-AzureVirtualNetworkGatewayIPsecParameters.md)


