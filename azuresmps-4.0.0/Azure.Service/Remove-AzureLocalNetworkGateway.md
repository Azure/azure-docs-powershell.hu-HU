---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F380D98B-98EA-4013-8744-549A6F18C9B6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04562bd9125617cfa9dbd76d47a3dd6c769e5b25
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016470"
---
# <span data-ttu-id="39359-101">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="39359-101">Remove-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="39359-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39359-102">SYNOPSIS</span></span>
<span data-ttu-id="39359-103">Azure helyi hálózati átjáró eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="39359-103">Removes an Azure local network gateway.</span></span>

## <span data-ttu-id="39359-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39359-104">SYNTAX</span></span>

```
Remove-AzureLocalNetworkGateway -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="39359-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="39359-105">DESCRIPTION</span></span>
<span data-ttu-id="39359-106">A **Remove-AzureLocalNetworkGateway** parancsmag eltávolítja az Azure local Network átjárót.</span><span class="sxs-lookup"><span data-stu-id="39359-106">The **Remove-AzureLocalNetworkGateway** cmdlet removes an Azure local network gateway.</span></span>

## <span data-ttu-id="39359-107">Példák</span><span class="sxs-lookup"><span data-stu-id="39359-107">EXAMPLES</span></span>

## <span data-ttu-id="39359-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39359-108">PARAMETERS</span></span>

### <span data-ttu-id="39359-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="39359-109">-GatewayId</span></span>
<span data-ttu-id="39359-110">Az átjáró AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="39359-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="39359-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="39359-111">-Profile</span></span>
<span data-ttu-id="39359-112">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="39359-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="39359-113">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="39359-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="39359-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39359-114">CommonParameters</span></span>
<span data-ttu-id="39359-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39359-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39359-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39359-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39359-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39359-117">INPUTS</span></span>

## <span data-ttu-id="39359-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39359-118">OUTPUTS</span></span>

## <span data-ttu-id="39359-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39359-119">NOTES</span></span>

## <span data-ttu-id="39359-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39359-120">RELATED LINKS</span></span>

[<span data-ttu-id="39359-121">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="39359-121">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="39359-122">Új – AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="39359-122">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="39359-123">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="39359-123">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)


