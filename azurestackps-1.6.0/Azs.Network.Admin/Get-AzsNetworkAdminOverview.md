---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671776"
---
# <span data-ttu-id="045de-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="045de-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="045de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="045de-102">SYNOPSIS</span></span>
<span data-ttu-id="045de-103">Áttekintés a hálózati erőforrás-szolgáltató állapotáról</span><span class="sxs-lookup"><span data-stu-id="045de-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="045de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="045de-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="045de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="045de-105">DESCRIPTION</span></span>
<span data-ttu-id="045de-106">Áttekintés a hálózati erőforrás-szolgáltató állapotáról</span><span class="sxs-lookup"><span data-stu-id="045de-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="045de-107">Az egyes tulajdonságok az Erőforrás kihasználtsága és az állapot szerinti részletezés részletes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="045de-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="045de-108">Példák</span><span class="sxs-lookup"><span data-stu-id="045de-108">EXAMPLES</span></span>

### <span data-ttu-id="045de-109">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="045de-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="045de-110">A hálózati rendszergazda áttekintése című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="045de-110">Get network admin overview.</span></span>

### <span data-ttu-id="045de-111">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="045de-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="045de-112">A nyilvános IP-cím használatba vételéhez.</span><span class="sxs-lookup"><span data-stu-id="045de-112">Get public ip address usage.</span></span>

## <span data-ttu-id="045de-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="045de-113">PARAMETERS</span></span>

### <span data-ttu-id="045de-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="045de-114">CommonParameters</span></span>
<span data-ttu-id="045de-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="045de-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="045de-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="045de-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="045de-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="045de-117">INPUTS</span></span>

## <span data-ttu-id="045de-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="045de-118">OUTPUTS</span></span>

### <span data-ttu-id="045de-119">Microsoft. AzureStack. Management. Network. admin. models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="045de-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="045de-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="045de-120">NOTES</span></span>

## <span data-ttu-id="045de-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="045de-121">RELATED LINKS</span></span>

