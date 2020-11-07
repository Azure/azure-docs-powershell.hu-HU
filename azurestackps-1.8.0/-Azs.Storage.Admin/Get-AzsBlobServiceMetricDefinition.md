---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b43acb45bc5b606303cbd33c20f0975919bb6b59
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840427"
---
# <span data-ttu-id="5f75e-101">Get-AzsBlobServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="5f75e-101">Get-AzsBlobServiceMetricDefinition</span></span>

## <span data-ttu-id="5f75e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f75e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f75e-103">A blob-szolgáltatás metrikák definíciójának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="5f75e-103">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="5f75e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f75e-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="5f75e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f75e-105">DESCRIPTION</span></span>
<span data-ttu-id="5f75e-106">A blob-szolgáltatás metrikák definíciójának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="5f75e-106">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="5f75e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5f75e-107">EXAMPLES</span></span>

### <span data-ttu-id="5f75e-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5f75e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBlobServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="5f75e-109">A blob-szolgáltatás metrikájának definíciójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="5f75e-109">Get a list of metric definitions for the blob service.</span></span>

## <span data-ttu-id="5f75e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f75e-110">PARAMETERS</span></span>

### <span data-ttu-id="5f75e-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="5f75e-111">-FarmName</span></span>
<span data-ttu-id="5f75e-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="5f75e-112">Farm Id.</span></span>

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

### <span data-ttu-id="5f75e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f75e-113">-ResourceGroupName</span></span>
<span data-ttu-id="5f75e-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="5f75e-114">Resource group name.</span></span>

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

### <span data-ttu-id="5f75e-115">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="5f75e-115">-Skip</span></span>
<span data-ttu-id="5f75e-116">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="5f75e-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5f75e-117">-Top</span><span class="sxs-lookup"><span data-stu-id="5f75e-117">-Top</span></span>
<span data-ttu-id="5f75e-118">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="5f75e-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5f75e-119">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="5f75e-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5f75e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f75e-120">CommonParameters</span></span>
<span data-ttu-id="5f75e-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f75e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f75e-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f75e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f75e-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f75e-123">INPUTS</span></span>

## <span data-ttu-id="5f75e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f75e-124">OUTPUTS</span></span>

### <span data-ttu-id="5f75e-125">Microsoft. AzureStack. Management. Storage. admin. models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="5f75e-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="5f75e-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f75e-126">NOTES</span></span>

## <span data-ttu-id="5f75e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f75e-127">RELATED LINKS</span></span>

