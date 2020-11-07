---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 80c80cb38013701d3e58d6d6bf77f774e2d61548
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840870"
---
# <span data-ttu-id="df68f-101">Get-AzsStorageShareMetric</span><span class="sxs-lookup"><span data-stu-id="df68f-101">Get-AzsStorageShareMetric</span></span>

## <span data-ttu-id="df68f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df68f-102">SYNOPSIS</span></span>
<span data-ttu-id="df68f-103">A tárterület-megosztás metrikájának listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="df68f-103">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="df68f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df68f-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetric [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="df68f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="df68f-105">DESCRIPTION</span></span>
<span data-ttu-id="df68f-106">A tárterület-megosztás metrikájának listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="df68f-106">Returns a list of metrics for a storage share.</span></span>

## <span data-ttu-id="df68f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="df68f-107">EXAMPLES</span></span>

### <span data-ttu-id="df68f-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="df68f-108">EXAMPLE 1</span></span>
```
Get-AzsStorageShareMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="df68f-109">A tárterület-megosztás metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="df68f-109">Get the list of metrics for a storage share.</span></span>

## <span data-ttu-id="df68f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df68f-110">PARAMETERS</span></span>

### <span data-ttu-id="df68f-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="df68f-111">-FarmName</span></span>
<span data-ttu-id="df68f-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="df68f-112">Farm Id.</span></span>

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

### <span data-ttu-id="df68f-113">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="df68f-113">-ShareName</span></span>
<span data-ttu-id="df68f-114">Megosztási név.</span><span class="sxs-lookup"><span data-stu-id="df68f-114">Share name.</span></span>

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

### <span data-ttu-id="df68f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df68f-115">-ResourceGroupName</span></span>
<span data-ttu-id="df68f-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="df68f-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df68f-117">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="df68f-117">-Skip</span></span>
<span data-ttu-id="df68f-118">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="df68f-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df68f-119">-Top</span><span class="sxs-lookup"><span data-stu-id="df68f-119">-Top</span></span>
<span data-ttu-id="df68f-120">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="df68f-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="df68f-121">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="df68f-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df68f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df68f-122">CommonParameters</span></span>
<span data-ttu-id="df68f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df68f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df68f-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df68f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df68f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df68f-125">INPUTS</span></span>

## <span data-ttu-id="df68f-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df68f-126">OUTPUTS</span></span>

### <span data-ttu-id="df68f-127">Microsoft. AzureStack. Management. Storage. admin. models. metrikus</span><span class="sxs-lookup"><span data-stu-id="df68f-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="df68f-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df68f-128">NOTES</span></span>

## <span data-ttu-id="df68f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df68f-129">RELATED LINKS</span></span>
