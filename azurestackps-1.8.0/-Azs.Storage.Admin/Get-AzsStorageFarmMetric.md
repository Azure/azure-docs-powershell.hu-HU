---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95ea9afa5d3dce953f4e51e84d011886e4ba5688
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840407"
---
# <span data-ttu-id="f2c25-101">Get-AzsStorageFarmMetric</span><span class="sxs-lookup"><span data-stu-id="f2c25-101">Get-AzsStorageFarmMetric</span></span>

## <span data-ttu-id="f2c25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2c25-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c25-103">A tárolási gazdaságok metrikájának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="f2c25-103">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="f2c25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2c25-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2c25-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2c25-105">DESCRIPTION</span></span>
<span data-ttu-id="f2c25-106">A tárolási gazdaságok metrikájának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="f2c25-106">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="f2c25-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f2c25-107">EXAMPLES</span></span>

### <span data-ttu-id="f2c25-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f2c25-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarmMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="f2c25-109">A tárterület-mezőgazdasági metrikák listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f2c25-109">Get the list of storage farm metrics.</span></span>

## <span data-ttu-id="f2c25-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2c25-110">PARAMETERS</span></span>

### <span data-ttu-id="f2c25-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="f2c25-111">-FarmName</span></span>
<span data-ttu-id="f2c25-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="f2c25-112">Farm Id.</span></span>

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

### <span data-ttu-id="f2c25-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2c25-113">-ResourceGroupName</span></span>
<span data-ttu-id="f2c25-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f2c25-114">Resource group name.</span></span>

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

### <span data-ttu-id="f2c25-115">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="f2c25-115">-Skip</span></span>
<span data-ttu-id="f2c25-116">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="f2c25-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f2c25-117">-Top</span><span class="sxs-lookup"><span data-stu-id="f2c25-117">-Top</span></span>
<span data-ttu-id="f2c25-118">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="f2c25-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f2c25-119">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="f2c25-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f2c25-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c25-120">CommonParameters</span></span>
<span data-ttu-id="f2c25-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2c25-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c25-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2c25-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c25-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2c25-123">INPUTS</span></span>

## <span data-ttu-id="f2c25-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2c25-124">OUTPUTS</span></span>

### <span data-ttu-id="f2c25-125">Microsoft. AzureStack. Management. Storage. admin. models. metrikus</span><span class="sxs-lookup"><span data-stu-id="f2c25-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="f2c25-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2c25-126">NOTES</span></span>

## <span data-ttu-id="f2c25-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2c25-127">RELATED LINKS</span></span>

