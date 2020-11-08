---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C4F876DF-FA9A-4446-8B7B-735137CEFE5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: eccd46bac70cb6555277b66f45cf2e79ad10e1e7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016525"
---
# <span data-ttu-id="2c131-101">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c131-101">Get-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="2c131-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c131-102">SYNOPSIS</span></span>
<span data-ttu-id="2c131-103">Virtuális hálózati átjárót kap.</span><span class="sxs-lookup"><span data-stu-id="2c131-103">Gets a virtual network gateway.</span></span>

## <span data-ttu-id="2c131-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c131-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGateway [-GatewayId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2c131-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c131-105">DESCRIPTION</span></span>
<span data-ttu-id="2c131-106">A **Get-AzureVirtualNetworkGateway** parancsmag Azure virtuális hálózati átjárót kap.</span><span class="sxs-lookup"><span data-stu-id="2c131-106">The **Get-AzureVirtualNetworkGateway** cmdlet gets an Azure virtual network gateway.</span></span>

## <span data-ttu-id="2c131-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2c131-107">EXAMPLES</span></span>

## <span data-ttu-id="2c131-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c131-108">PARAMETERS</span></span>

### <span data-ttu-id="2c131-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="2c131-109">-GatewayId</span></span>
<span data-ttu-id="2c131-110">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c131-110">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="2c131-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="2c131-111">-Profile</span></span>
<span data-ttu-id="2c131-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="2c131-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2c131-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="2c131-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2c131-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c131-114">CommonParameters</span></span>
<span data-ttu-id="2c131-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c131-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c131-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c131-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c131-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c131-117">INPUTS</span></span>

## <span data-ttu-id="2c131-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c131-118">OUTPUTS</span></span>

## <span data-ttu-id="2c131-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c131-119">NOTES</span></span>

## <span data-ttu-id="2c131-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c131-120">RELATED LINKS</span></span>

[<span data-ttu-id="2c131-121">Új – AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c131-121">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="2c131-122">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c131-122">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="2c131-123">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c131-123">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="2c131-124">Átméretezés-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c131-124">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)


