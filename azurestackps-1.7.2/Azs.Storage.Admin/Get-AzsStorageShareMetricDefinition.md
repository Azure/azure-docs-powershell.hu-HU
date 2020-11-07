---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 646ee96dec361ac6318b4cfe48b80ec4c3686321
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839924"
---
# <span data-ttu-id="bf8c6-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="bf8c6-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="bf8c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf8c6-102">SYNOPSIS</span></span>
<span data-ttu-id="bf8c6-103">Egy tárterület-megosztás metrikus definícióinak listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="bf8c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf8c6-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-Name] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="bf8c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf8c6-105">DESCRIPTION</span></span>
<span data-ttu-id="bf8c6-106">Egy tárterület-megosztás metrikus definícióinak listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="bf8c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf8c6-107">EXAMPLES</span></span>

### <span data-ttu-id="bf8c6-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bf8c6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Name "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="bf8c6-109">Megtudhatja, hogy miként érheti el a metrika-definíciók listáját a tárterület-megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="bf8c6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf8c6-110">PARAMETERS</span></span>

### <span data-ttu-id="bf8c6-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="bf8c6-111">-FarmName</span></span>
<span data-ttu-id="bf8c6-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-112">Farm Id.</span></span>

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

### <span data-ttu-id="bf8c6-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf8c6-113">-Name</span></span>
<span data-ttu-id="bf8c6-114">Megosztási név.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf8c6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf8c6-115">-ResourceGroupName</span></span>
<span data-ttu-id="bf8c6-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-116">Resource group name.</span></span>

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

### <span data-ttu-id="bf8c6-117">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="bf8c6-117">-Skip</span></span>
<span data-ttu-id="bf8c6-118">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="bf8c6-119">-Top</span><span class="sxs-lookup"><span data-stu-id="bf8c6-119">-Top</span></span>
<span data-ttu-id="bf8c6-120">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bf8c6-121">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="bf8c6-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="bf8c6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf8c6-122">CommonParameters</span></span>
<span data-ttu-id="bf8c6-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf8c6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf8c6-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf8c6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf8c6-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf8c6-125">INPUTS</span></span>

## <span data-ttu-id="bf8c6-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf8c6-126">OUTPUTS</span></span>

### <span data-ttu-id="bf8c6-127">Microsoft. AzureStack. Management. Storage. admin. models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="bf8c6-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="bf8c6-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf8c6-128">NOTES</span></span>

## <span data-ttu-id="bf8c6-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf8c6-129">RELATED LINKS</span></span>

