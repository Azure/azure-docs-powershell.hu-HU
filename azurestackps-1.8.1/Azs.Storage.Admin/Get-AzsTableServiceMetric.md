---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1affc11e3e5ff360cf08468c4935b6d48d68321
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840846"
---
# <span data-ttu-id="82fde-101">Get-AzsTableServiceMetric</span><span class="sxs-lookup"><span data-stu-id="82fde-101">Get-AzsTableServiceMetric</span></span>

## <span data-ttu-id="82fde-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82fde-102">SYNOPSIS</span></span>
<span data-ttu-id="82fde-103">A Table Service metrikájának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="82fde-103">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="82fde-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82fde-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="82fde-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="82fde-105">DESCRIPTION</span></span>
<span data-ttu-id="82fde-106">A Table Service metrikájának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="82fde-106">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="82fde-107">Példák</span><span class="sxs-lookup"><span data-stu-id="82fde-107">EXAMPLES</span></span>

### <span data-ttu-id="82fde-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="82fde-108">EXAMPLE 1</span></span>
```
Get-AzsTableServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="82fde-109">A Table Service metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="82fde-109">Get the list of metrics for table service.</span></span>

## <span data-ttu-id="82fde-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82fde-110">PARAMETERS</span></span>

### <span data-ttu-id="82fde-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="82fde-111">-FarmName</span></span>
<span data-ttu-id="82fde-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="82fde-112">Farm Id.</span></span>

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

### <span data-ttu-id="82fde-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82fde-113">-ResourceGroupName</span></span>
<span data-ttu-id="82fde-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="82fde-114">Resource group name.</span></span>

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

### <span data-ttu-id="82fde-115">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="82fde-115">-Skip</span></span>
<span data-ttu-id="82fde-116">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="82fde-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="82fde-117">-Top</span><span class="sxs-lookup"><span data-stu-id="82fde-117">-Top</span></span>
<span data-ttu-id="82fde-118">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="82fde-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="82fde-119">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="82fde-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="82fde-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82fde-120">CommonParameters</span></span>
<span data-ttu-id="82fde-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82fde-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82fde-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82fde-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82fde-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82fde-123">INPUTS</span></span>

## <span data-ttu-id="82fde-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82fde-124">OUTPUTS</span></span>

### <span data-ttu-id="82fde-125">Microsoft. AzureStack. Management. Storage. admin. models. metrikus</span><span class="sxs-lookup"><span data-stu-id="82fde-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="82fde-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82fde-126">NOTES</span></span>

## <span data-ttu-id="82fde-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82fde-127">RELATED LINKS</span></span>
