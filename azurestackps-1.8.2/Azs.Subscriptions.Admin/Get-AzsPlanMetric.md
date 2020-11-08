---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8ef41d414d12182c15d9ec5b01138e0110dee9f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017096"
---
# <span data-ttu-id="ba01f-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="ba01f-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="ba01f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba01f-102">SYNOPSIS</span></span>
<span data-ttu-id="ba01f-103">A terv metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ba01f-103">Get the plan metrics.</span></span>

## <span data-ttu-id="ba01f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba01f-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="ba01f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba01f-105">DESCRIPTION</span></span>
<span data-ttu-id="ba01f-106">A terv metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ba01f-106">Get the plan metrics.</span></span>

## <span data-ttu-id="ba01f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ba01f-107">EXAMPLES</span></span>

### <span data-ttu-id="ba01f-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ba01f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="ba01f-109">A terv metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ba01f-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="ba01f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba01f-110">PARAMETERS</span></span>

### <span data-ttu-id="ba01f-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ba01f-111">-PlanName</span></span>
<span data-ttu-id="ba01f-112">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="ba01f-112">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba01f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba01f-113">-ResourceGroupName</span></span>
<span data-ttu-id="ba01f-114">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="ba01f-114">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba01f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba01f-115">CommonParameters</span></span>
<span data-ttu-id="ba01f-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba01f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba01f-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba01f-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba01f-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba01f-118">INPUTS</span></span>

## <span data-ttu-id="ba01f-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba01f-119">OUTPUTS</span></span>

### <span data-ttu-id="ba01f-120">Microsoft. AzureStack. Management. Subscriptions. admin. modellek. metrikus</span><span class="sxs-lookup"><span data-stu-id="ba01f-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="ba01f-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba01f-121">NOTES</span></span>

## <span data-ttu-id="ba01f-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba01f-122">RELATED LINKS</span></span>

