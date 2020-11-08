---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d81043e165600a549bace91458449577b23dbd8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017050"
---
# <span data-ttu-id="beb3b-101">Get-AzsQueueServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="beb3b-101">Get-AzsQueueServiceMetricDefinition</span></span>

## <span data-ttu-id="beb3b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="beb3b-102">SYNOPSIS</span></span>
<span data-ttu-id="beb3b-103">A várólista-szolgáltatás metrikus definícióinak listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="beb3b-103">Returns a list of metric definitions for queue service.</span></span>

## <span data-ttu-id="beb3b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="beb3b-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="beb3b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="beb3b-105">DESCRIPTION</span></span>
<span data-ttu-id="beb3b-106">A várólista-szolgáltatás metrikus definícióinak listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="beb3b-106">Returns a list of metric definitions for queue service.</span></span>

## <span data-ttu-id="beb3b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="beb3b-107">EXAMPLES</span></span>

### <span data-ttu-id="beb3b-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="beb3b-108">EXAMPLE 1</span></span>
```
Get-AzsQueueServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="beb3b-109">A várólista-szolgáltatáshoz tartozó metrikus definíciók listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="beb3b-109">Get the list of metric definitions for queue service.</span></span>

## <span data-ttu-id="beb3b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="beb3b-110">PARAMETERS</span></span>

### <span data-ttu-id="beb3b-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="beb3b-111">-FarmName</span></span>
<span data-ttu-id="beb3b-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="beb3b-112">Farm Id.</span></span>

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

### <span data-ttu-id="beb3b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beb3b-113">-ResourceGroupName</span></span>
<span data-ttu-id="beb3b-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="beb3b-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb3b-115">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="beb3b-115">-Skip</span></span>
<span data-ttu-id="beb3b-116">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="beb3b-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb3b-117">-Top</span><span class="sxs-lookup"><span data-stu-id="beb3b-117">-Top</span></span>
<span data-ttu-id="beb3b-118">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="beb3b-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="beb3b-119">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="beb3b-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb3b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beb3b-120">CommonParameters</span></span>
<span data-ttu-id="beb3b-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="beb3b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beb3b-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beb3b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beb3b-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="beb3b-123">INPUTS</span></span>

## <span data-ttu-id="beb3b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="beb3b-124">OUTPUTS</span></span>

### <span data-ttu-id="beb3b-125">Microsoft. AzureStack. Management. Storage. admin. models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="beb3b-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="beb3b-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="beb3b-126">NOTES</span></span>

## <span data-ttu-id="beb3b-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="beb3b-127">RELATED LINKS</span></span>
