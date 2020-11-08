---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplanmetric
schema: 2.0.0
ms.openlocfilehash: 9a8ef074cf6e59d30217b55b956a4d5101708bcc
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94015083"
---
# <span data-ttu-id="e38fc-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="e38fc-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="e38fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e38fc-102">SYNOPSIS</span></span>
<span data-ttu-id="e38fc-103">A megadott csomag metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e38fc-103">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="e38fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e38fc-104">SYNTAX</span></span>

```
Get-AzsPlanMetric -PlanName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e38fc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e38fc-105">DESCRIPTION</span></span>
<span data-ttu-id="e38fc-106">A megadott csomag metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e38fc-106">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="e38fc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e38fc-107">EXAMPLES</span></span>

### <span data-ttu-id="e38fc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e38fc-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlanMetric -PlanName "testplan" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="e38fc-109">A terv metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e38fc-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="e38fc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e38fc-110">PARAMETERS</span></span>

### <span data-ttu-id="e38fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38fc-111">-DefaultProfile</span></span>
<span data-ttu-id="e38fc-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e38fc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e38fc-113">-PlanName</span><span class="sxs-lookup"><span data-stu-id="e38fc-113">-PlanName</span></span>
<span data-ttu-id="e38fc-114">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="e38fc-114">Name of the plan.</span></span>

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

### <span data-ttu-id="e38fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e38fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="e38fc-116">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="e38fc-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e38fc-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e38fc-117">-SubscriptionId</span></span>
<span data-ttu-id="e38fc-118">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e38fc-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e38fc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38fc-119">CommonParameters</span></span>
<span data-ttu-id="e38fc-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e38fc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38fc-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e38fc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38fc-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e38fc-122">INPUTS</span></span>

## <span data-ttu-id="e38fc-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e38fc-123">OUTPUTS</span></span>

### <span data-ttu-id="e38fc-124">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="e38fc-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="e38fc-125">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e38fc-125">ALIASES</span></span>

## <span data-ttu-id="e38fc-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e38fc-126">NOTES</span></span>

## <span data-ttu-id="e38fc-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e38fc-127">RELATED LINKS</span></span>

