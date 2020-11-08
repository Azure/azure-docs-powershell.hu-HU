---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsoffermetric
schema: 2.0.0
ms.openlocfilehash: 515cf3d9c26c9ca4ed59178e49854e23edfea84c
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94015117"
---
# <span data-ttu-id="f6f0a-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="f6f0a-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="f6f0a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f0a-103">Az ajánlat metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f6f0a-103">Get the offer metrics.</span></span>

## <span data-ttu-id="f6f0a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6f0a-104">SYNTAX</span></span>

```
Get-AzsOfferMetric -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f6f0a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6f0a-105">DESCRIPTION</span></span>
<span data-ttu-id="f6f0a-106">Az ajánlat metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f6f0a-106">Get the offer metrics.</span></span>

## <span data-ttu-id="f6f0a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f6f0a-107">EXAMPLES</span></span>

### <span data-ttu-id="f6f0a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f6f0a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferMetric -OfferName "testoffer" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="f6f0a-109">Az ajánlat metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f6f0a-109">Get the offer metrics.</span></span>

## <span data-ttu-id="f6f0a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6f0a-110">PARAMETERS</span></span>

### <span data-ttu-id="f6f0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f0a-111">-DefaultProfile</span></span>
<span data-ttu-id="f6f0a-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6f0a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6f0a-113">-OfferName</span><span class="sxs-lookup"><span data-stu-id="f6f0a-113">-OfferName</span></span>
<span data-ttu-id="f6f0a-114">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="f6f0a-114">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f6f0a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6f0a-115">-ResourceGroupName</span></span>
<span data-ttu-id="f6f0a-116">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="f6f0a-116">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f6f0a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6f0a-117">-SubscriptionId</span></span>
<span data-ttu-id="f6f0a-118">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f6f0a-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f6f0a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f0a-119">CommonParameters</span></span>
<span data-ttu-id="f6f0a-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6f0a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f0a-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f6f0a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f0a-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6f0a-122">INPUTS</span></span>

## <span data-ttu-id="f6f0a-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6f0a-123">OUTPUTS</span></span>

### <span data-ttu-id="f6f0a-124">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="f6f0a-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="f6f0a-125">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f6f0a-125">ALIASES</span></span>

## <span data-ttu-id="f6f0a-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6f0a-126">NOTES</span></span>

## <span data-ttu-id="f6f0a-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6f0a-127">RELATED LINKS</span></span>

