---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
schema: 2.0.0
ms.openlocfilehash: 1450a35252a3bd5e749a8ebdb60fda0e8ad35f88
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017059"
---
# <span data-ttu-id="2d9b7-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2d9b7-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="2d9b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d9b7-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9b7-103">Az összes terheléselosztó lista beszerzése.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="2d9b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d9b7-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2d9b7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d9b7-105">DESCRIPTION</span></span>
<span data-ttu-id="2d9b7-106">Az összes terheléselosztó lista beszerzése.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="2d9b7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2d9b7-107">EXAMPLES</span></span>

### <span data-ttu-id="2d9b7-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2d9b7-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsLoadBalancer
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
```



## <span data-ttu-id="2d9b7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d9b7-109">PARAMETERS</span></span>

### <span data-ttu-id="2d9b7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9b7-110">-DefaultProfile</span></span>
<span data-ttu-id="2d9b7-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2d9b7-112">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="2d9b7-112">-Filter</span></span>
<span data-ttu-id="2d9b7-113">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="2d9b7-113">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2d9b7-114">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="2d9b7-114">-InlineCount</span></span>
<span data-ttu-id="2d9b7-115">OData a szövegközi Count paramétert.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-115">OData inline count parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2d9b7-116">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="2d9b7-116">-OrderBy</span></span>
<span data-ttu-id="2d9b7-117">OData orderBy paraméter</span><span class="sxs-lookup"><span data-stu-id="2d9b7-117">OData orderBy parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2d9b7-118">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="2d9b7-118">-Skip</span></span>
<span data-ttu-id="2d9b7-119">OData-kihagyás paraméter</span><span class="sxs-lookup"><span data-stu-id="2d9b7-119">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2d9b7-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d9b7-120">-SubscriptionId</span></span>
<span data-ttu-id="2d9b7-121">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-121">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2d9b7-122">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-122">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2d9b7-123">-Top</span><span class="sxs-lookup"><span data-stu-id="2d9b7-123">-Top</span></span>
<span data-ttu-id="2d9b7-124">OData Top paraméter</span><span class="sxs-lookup"><span data-stu-id="2d9b7-124">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2d9b7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9b7-125">CommonParameters</span></span>
<span data-ttu-id="2d9b7-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d9b7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9b7-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2d9b7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9b7-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d9b7-128">INPUTS</span></span>

## <span data-ttu-id="2d9b7-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d9b7-129">OUTPUTS</span></span>

### <span data-ttu-id="2d9b7-130">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. modellek. Api20150615. ILoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2d9b7-130">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.ILoadBalancer</span></span>



## <span data-ttu-id="2d9b7-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d9b7-131">NOTES</span></span>

## <span data-ttu-id="2d9b7-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d9b7-132">RELATED LINKS</span></span>

