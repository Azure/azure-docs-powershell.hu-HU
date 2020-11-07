---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840730"
---
# <span data-ttu-id="df446-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="df446-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="df446-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df446-102">SYNOPSIS</span></span>
<span data-ttu-id="df446-103">Áttekintés a hálózati erőforrás-szolgáltató állapotáról</span><span class="sxs-lookup"><span data-stu-id="df446-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="df446-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df446-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="df446-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="df446-105">DESCRIPTION</span></span>
<span data-ttu-id="df446-106">Áttekintés a hálózati erőforrás-szolgáltató állapotáról</span><span class="sxs-lookup"><span data-stu-id="df446-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="df446-107">Az egyes tulajdonságok az Erőforrás kihasználtsága és az állapot szerinti részletezés részletes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="df446-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="df446-108">Példák</span><span class="sxs-lookup"><span data-stu-id="df446-108">EXAMPLES</span></span>

### <span data-ttu-id="df446-109">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="df446-109">EXAMPLE 1</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="df446-110">A hálózati rendszergazda áttekintése című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="df446-110">Get network admin overview.</span></span>

### <span data-ttu-id="df446-111">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="df446-111">EXAMPLE 2</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="df446-112">A nyilvános IP-cím használatba vételéhez.</span><span class="sxs-lookup"><span data-stu-id="df446-112">Get public ip address usage.</span></span>

## <span data-ttu-id="df446-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df446-113">PARAMETERS</span></span>

### <span data-ttu-id="df446-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df446-114">CommonParameters</span></span>
<span data-ttu-id="df446-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df446-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df446-116">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df446-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df446-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df446-117">INPUTS</span></span>

## <span data-ttu-id="df446-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df446-118">OUTPUTS</span></span>

### <span data-ttu-id="df446-119">Microsoft. AzureStack. Management. Network. admin. models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="df446-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="df446-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df446-120">NOTES</span></span>

## <span data-ttu-id="df446-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df446-121">RELATED LINKS</span></span>
