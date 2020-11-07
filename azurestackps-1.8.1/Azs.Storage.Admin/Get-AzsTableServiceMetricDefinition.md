---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f5d91226a4762c5f1429d8d05b48defd83b4e2df
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840838"
---
# <span data-ttu-id="ed72c-101">Get-AzsTableServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="ed72c-101">Get-AzsTableServiceMetricDefinition</span></span>

## <span data-ttu-id="ed72c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed72c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed72c-103">A Table Service metrikus definícióinak listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ed72c-103">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="ed72c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed72c-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ed72c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed72c-105">DESCRIPTION</span></span>
<span data-ttu-id="ed72c-106">A Table Service metrikus definícióinak listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ed72c-106">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="ed72c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ed72c-107">EXAMPLES</span></span>

### <span data-ttu-id="ed72c-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="ed72c-108">EXAMPLE 1</span></span>
```
Get-AzsTableServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="ed72c-109">A táblázatos szolgáltatás metrikus definícióinak listája</span><span class="sxs-lookup"><span data-stu-id="ed72c-109">Get the list of metric definitions for table service.</span></span>

## <span data-ttu-id="ed72c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed72c-110">PARAMETERS</span></span>

### <span data-ttu-id="ed72c-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="ed72c-111">-FarmName</span></span>
<span data-ttu-id="ed72c-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="ed72c-112">Farm Id.</span></span>

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

### <span data-ttu-id="ed72c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed72c-113">-ResourceGroupName</span></span>
<span data-ttu-id="ed72c-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ed72c-114">Resource group name.</span></span>

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

### <span data-ttu-id="ed72c-115">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="ed72c-115">-Skip</span></span>
<span data-ttu-id="ed72c-116">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="ed72c-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ed72c-117">-Top</span><span class="sxs-lookup"><span data-stu-id="ed72c-117">-Top</span></span>
<span data-ttu-id="ed72c-118">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="ed72c-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ed72c-119">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="ed72c-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ed72c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed72c-120">CommonParameters</span></span>
<span data-ttu-id="ed72c-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed72c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed72c-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed72c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed72c-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed72c-123">INPUTS</span></span>

## <span data-ttu-id="ed72c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed72c-124">OUTPUTS</span></span>

### <span data-ttu-id="ed72c-125">Microsoft. AzureStack. Management. Storage. admin. models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="ed72c-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="ed72c-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed72c-126">NOTES</span></span>

## <span data-ttu-id="ed72c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed72c-127">RELATED LINKS</span></span>
