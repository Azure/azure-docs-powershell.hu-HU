---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cadf5ad37119ab6b50191e50e8ec281fe4bce2d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490815"
---
# <span data-ttu-id="ed3d6-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="ed3d6-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="ed3d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed3d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3d6-103">A terv metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ed3d6-103">Get the plan metrics.</span></span>

## <span data-ttu-id="ed3d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed3d6-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="ed3d6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed3d6-105">DESCRIPTION</span></span>
<span data-ttu-id="ed3d6-106">A terv metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ed3d6-106">Get the plan metrics.</span></span>

## <span data-ttu-id="ed3d6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ed3d6-107">EXAMPLES</span></span>

### <span data-ttu-id="ed3d6-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ed3d6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="ed3d6-109">A terv metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ed3d6-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="ed3d6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed3d6-110">PARAMETERS</span></span>

### <span data-ttu-id="ed3d6-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ed3d6-111">-PlanName</span></span>
<span data-ttu-id="ed3d6-112">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="ed3d6-112">Name of the plan.</span></span>

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

### <span data-ttu-id="ed3d6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed3d6-113">-ResourceGroupName</span></span>
<span data-ttu-id="ed3d6-114">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="ed3d6-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="ed3d6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3d6-115">CommonParameters</span></span>
<span data-ttu-id="ed3d6-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed3d6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3d6-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed3d6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3d6-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed3d6-118">INPUTS</span></span>

## <span data-ttu-id="ed3d6-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed3d6-119">OUTPUTS</span></span>

### <span data-ttu-id="ed3d6-120">Microsoft. AzureStack. Management. Subscriptions. admin. modellek. metrikus</span><span class="sxs-lookup"><span data-stu-id="ed3d6-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="ed3d6-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed3d6-121">NOTES</span></span>

## <span data-ttu-id="ed3d6-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed3d6-122">RELATED LINKS</span></span>

