---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016615"
---
# <span data-ttu-id="d0299-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="d0299-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="d0299-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0299-102">SYNOPSIS</span></span>
<span data-ttu-id="d0299-103">Áttekintés a hálózati erőforrás-szolgáltató állapotáról</span><span class="sxs-lookup"><span data-stu-id="d0299-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="d0299-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0299-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="d0299-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0299-105">DESCRIPTION</span></span>
<span data-ttu-id="d0299-106">Áttekintés a hálózati erőforrás-szolgáltató állapotáról</span><span class="sxs-lookup"><span data-stu-id="d0299-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="d0299-107">Az egyes tulajdonságok az Erőforrás kihasználtsága és az állapot szerinti részletezés részletes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0299-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="d0299-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d0299-108">EXAMPLES</span></span>

### <span data-ttu-id="d0299-109">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="d0299-109">EXAMPLE 1</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="d0299-110">A hálózati rendszergazda áttekintése című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d0299-110">Get network admin overview.</span></span>

### <span data-ttu-id="d0299-111">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="d0299-111">EXAMPLE 2</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="d0299-112">A nyilvános IP-cím használatba vételéhez.</span><span class="sxs-lookup"><span data-stu-id="d0299-112">Get public ip address usage.</span></span>

## <span data-ttu-id="d0299-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0299-113">PARAMETERS</span></span>

### <span data-ttu-id="d0299-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0299-114">CommonParameters</span></span>
<span data-ttu-id="d0299-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0299-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0299-116">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0299-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0299-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0299-117">INPUTS</span></span>

## <span data-ttu-id="d0299-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0299-118">OUTPUTS</span></span>

### <span data-ttu-id="d0299-119">Microsoft. AzureStack. Management. Network. admin. models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="d0299-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="d0299-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0299-120">NOTES</span></span>

## <span data-ttu-id="d0299-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0299-121">RELATED LINKS</span></span>
