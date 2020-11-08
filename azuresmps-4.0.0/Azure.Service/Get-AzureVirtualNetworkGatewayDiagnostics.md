---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F6A89D39-18AD-4087-823C-63FA0A3690E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36c51d0ceae42aab50e2df9e0532c98dd6800747
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016520"
---
# <span data-ttu-id="ebb28-101">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ebb28-101">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="ebb28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ebb28-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb28-103">Megkapja az Azure Virtual Network Gateway Diagnostics eredményeit.</span><span class="sxs-lookup"><span data-stu-id="ebb28-103">Gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="ebb28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ebb28-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ebb28-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ebb28-105">DESCRIPTION</span></span>
<span data-ttu-id="ebb28-106">A **Get-AzureVirtualNetworkGatewayDiagnostics** parancsmag az Azure Virtual Network Gateway Diagnostics eredményeinek eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="ebb28-106">The **Get-AzureVirtualNetworkGatewayDiagnostics** cmdlet gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="ebb28-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ebb28-107">EXAMPLES</span></span>

## <span data-ttu-id="ebb28-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ebb28-108">PARAMETERS</span></span>

### <span data-ttu-id="ebb28-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="ebb28-109">-GatewayId</span></span>
<span data-ttu-id="ebb28-110">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebb28-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="ebb28-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="ebb28-111">-Profile</span></span>
<span data-ttu-id="ebb28-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ebb28-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ebb28-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ebb28-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ebb28-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb28-114">CommonParameters</span></span>
<span data-ttu-id="ebb28-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ebb28-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb28-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebb28-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb28-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebb28-117">INPUTS</span></span>

## <span data-ttu-id="ebb28-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebb28-118">OUTPUTS</span></span>

## <span data-ttu-id="ebb28-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ebb28-119">NOTES</span></span>

## <span data-ttu-id="ebb28-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebb28-120">RELATED LINKS</span></span>

[<span data-ttu-id="ebb28-121">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ebb28-121">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="ebb28-122">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ebb28-122">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


