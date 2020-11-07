---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fac65e094352d399f5392b26a8ed314616125ba0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839741"
---
# <span data-ttu-id="6982d-101">Get-AzsTableServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="6982d-101">Get-AzsTableServiceMetricDefinition</span></span>

## <span data-ttu-id="6982d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6982d-102">SYNOPSIS</span></span>
<span data-ttu-id="6982d-103">A Table Service metrikus definícióinak listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="6982d-103">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="6982d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6982d-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6982d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6982d-105">DESCRIPTION</span></span>
<span data-ttu-id="6982d-106">A Table Service metrikus definícióinak listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="6982d-106">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="6982d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6982d-107">EXAMPLES</span></span>

### <span data-ttu-id="6982d-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6982d-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsTableServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="6982d-109">A táblázatos szolgáltatás metrikus definícióinak listája</span><span class="sxs-lookup"><span data-stu-id="6982d-109">Get the list of metric definitions for table service.</span></span>

## <span data-ttu-id="6982d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6982d-110">PARAMETERS</span></span>

### <span data-ttu-id="6982d-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="6982d-111">-FarmName</span></span>
<span data-ttu-id="6982d-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="6982d-112">Farm Id.</span></span>

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

### <span data-ttu-id="6982d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6982d-113">-ResourceGroupName</span></span>
<span data-ttu-id="6982d-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6982d-114">Resource group name.</span></span>

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

### <span data-ttu-id="6982d-115">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="6982d-115">-Skip</span></span>
<span data-ttu-id="6982d-116">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="6982d-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6982d-117">-Top</span><span class="sxs-lookup"><span data-stu-id="6982d-117">-Top</span></span>
<span data-ttu-id="6982d-118">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="6982d-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6982d-119">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="6982d-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6982d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6982d-120">CommonParameters</span></span>
<span data-ttu-id="6982d-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6982d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6982d-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6982d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6982d-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6982d-123">INPUTS</span></span>

## <span data-ttu-id="6982d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6982d-124">OUTPUTS</span></span>

### <span data-ttu-id="6982d-125">Microsoft. AzureStack. Management. Storage. admin. models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="6982d-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="6982d-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6982d-126">NOTES</span></span>

## <span data-ttu-id="6982d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6982d-127">RELATED LINKS</span></span>

