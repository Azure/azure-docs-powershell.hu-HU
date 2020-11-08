---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 822452c1c6b83669759bae2c861ee3456a13a0dc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016760"
---
# <span data-ttu-id="88d4a-101">Get-AzsBlobServiceMetric</span><span class="sxs-lookup"><span data-stu-id="88d4a-101">Get-AzsBlobServiceMetric</span></span>

## <span data-ttu-id="88d4a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="88d4a-103">A blob-szolgáltatás metrikáinak listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="88d4a-103">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="88d4a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88d4a-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="88d4a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="88d4a-105">DESCRIPTION</span></span>
<span data-ttu-id="88d4a-106">A blob-szolgáltatás metrikáinak listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="88d4a-106">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="88d4a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="88d4a-107">EXAMPLES</span></span>

### <span data-ttu-id="88d4a-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="88d4a-108">EXAMPLE 1</span></span>
```
Get-AzsBlobServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="88d4a-109">A blob-szolgáltatás metrikájának listája</span><span class="sxs-lookup"><span data-stu-id="88d4a-109">Get a list of metrics for blob service.</span></span>

## <span data-ttu-id="88d4a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88d4a-110">PARAMETERS</span></span>

### <span data-ttu-id="88d4a-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="88d4a-111">-FarmName</span></span>
<span data-ttu-id="88d4a-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="88d4a-112">Farm Id.</span></span>

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

### <span data-ttu-id="88d4a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88d4a-113">-ResourceGroupName</span></span>
<span data-ttu-id="88d4a-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="88d4a-114">Resource group name.</span></span>

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

### <span data-ttu-id="88d4a-115">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="88d4a-115">-Skip</span></span>
<span data-ttu-id="88d4a-116">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="88d4a-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="88d4a-117">-Top</span><span class="sxs-lookup"><span data-stu-id="88d4a-117">-Top</span></span>
<span data-ttu-id="88d4a-118">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="88d4a-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="88d4a-119">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="88d4a-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="88d4a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d4a-120">CommonParameters</span></span>
<span data-ttu-id="88d4a-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88d4a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d4a-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88d4a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d4a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88d4a-123">INPUTS</span></span>

## <span data-ttu-id="88d4a-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88d4a-124">OUTPUTS</span></span>

### <span data-ttu-id="88d4a-125">Microsoft. AzureStack. Management. Storage. admin. models. metrikus</span><span class="sxs-lookup"><span data-stu-id="88d4a-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="88d4a-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88d4a-126">NOTES</span></span>

## <span data-ttu-id="88d4a-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88d4a-127">RELATED LINKS</span></span>
