---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac33f0feae7d54798753637f8f7898ab796f0939
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838685"
---
# <span data-ttu-id="ca717-101">Get-AzsQueueServiceMetric</span><span class="sxs-lookup"><span data-stu-id="ca717-101">Get-AzsQueueServiceMetric</span></span>

## <span data-ttu-id="ca717-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca717-102">SYNOPSIS</span></span>
<span data-ttu-id="ca717-103">A várólista-szolgáltatás metrikáinak listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ca717-103">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="ca717-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca717-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca717-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca717-105">DESCRIPTION</span></span>
<span data-ttu-id="ca717-106">A várólista-szolgáltatás metrikáinak listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ca717-106">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="ca717-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ca717-107">EXAMPLES</span></span>

### <span data-ttu-id="ca717-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ca717-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="ca717-109">A várólista-szolgáltatás metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ca717-109">Get the list of metrics for queue service.</span></span>

## <span data-ttu-id="ca717-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca717-110">PARAMETERS</span></span>

### <span data-ttu-id="ca717-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="ca717-111">-FarmName</span></span>
<span data-ttu-id="ca717-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="ca717-112">Farm Id.</span></span>

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

### <span data-ttu-id="ca717-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca717-113">-ResourceGroupName</span></span>
<span data-ttu-id="ca717-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ca717-114">Resource group name.</span></span>

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

### <span data-ttu-id="ca717-115">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="ca717-115">-Skip</span></span>
<span data-ttu-id="ca717-116">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="ca717-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ca717-117">-Top</span><span class="sxs-lookup"><span data-stu-id="ca717-117">-Top</span></span>
<span data-ttu-id="ca717-118">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="ca717-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ca717-119">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="ca717-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ca717-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca717-120">CommonParameters</span></span>
<span data-ttu-id="ca717-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca717-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca717-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca717-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca717-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca717-123">INPUTS</span></span>

## <span data-ttu-id="ca717-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca717-124">OUTPUTS</span></span>

### <span data-ttu-id="ca717-125">Microsoft. AzureStack. Management. Storage. admin. models. metrikus</span><span class="sxs-lookup"><span data-stu-id="ca717-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="ca717-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca717-126">NOTES</span></span>

## <span data-ttu-id="ca717-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca717-127">RELATED LINKS</span></span>

