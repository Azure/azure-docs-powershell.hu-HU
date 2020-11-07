---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0bbd694fff313f4c7b8983521dee8cd1c01f7561
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840137"
---
# <span data-ttu-id="12962-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="12962-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="12962-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12962-102">SYNOPSIS</span></span>
<span data-ttu-id="12962-103">A frissítési futások listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="12962-103">Get the list of update runs.</span></span>

## <span data-ttu-id="12962-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12962-104">SYNTAX</span></span>

### <span data-ttu-id="12962-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12962-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="12962-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="12962-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="12962-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="12962-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="12962-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="12962-108">DESCRIPTION</span></span>
<span data-ttu-id="12962-109">A frissítési futások listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="12962-109">Get the list of update runs.</span></span> <span data-ttu-id="12962-110">A visszaadott UpdateRun-objektumok példányai átállíthatók az újraindítás AzsUpdateRun, ha szükséges.</span><span class="sxs-lookup"><span data-stu-id="12962-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="12962-111">Példák</span><span class="sxs-lookup"><span data-stu-id="12962-111">EXAMPLES</span></span>

### <span data-ttu-id="12962-112">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="12962-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="12962-113">Bemutatjuk, hogy milyen kísérletekre van érvényes frissítés.</span><span class="sxs-lookup"><span data-stu-id="12962-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="12962-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12962-114">PARAMETERS</span></span>

### <span data-ttu-id="12962-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="12962-115">-Name</span></span>
<span data-ttu-id="12962-116">A futtatási azonosító frissítése</span><span class="sxs-lookup"><span data-stu-id="12962-116">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12962-117">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="12962-117">-UpdateName</span></span>
<span data-ttu-id="12962-118">A frissítés neve.</span><span class="sxs-lookup"><span data-stu-id="12962-118">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12962-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="12962-119">-Location</span></span>
<span data-ttu-id="12962-120">A frissítési hely neve.</span><span class="sxs-lookup"><span data-stu-id="12962-120">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12962-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12962-121">-ResourceGroupName</span></span>
<span data-ttu-id="12962-122">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="12962-122">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12962-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12962-123">-ResourceId</span></span>
<span data-ttu-id="12962-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="12962-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12962-125">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="12962-125">-Skip</span></span>
<span data-ttu-id="12962-126">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="12962-126">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12962-127">-Top</span><span class="sxs-lookup"><span data-stu-id="12962-127">-Top</span></span>
<span data-ttu-id="12962-128">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="12962-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="12962-129">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="12962-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12962-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12962-130">CommonParameters</span></span>
<span data-ttu-id="12962-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12962-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12962-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12962-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12962-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12962-133">INPUTS</span></span>

## <span data-ttu-id="12962-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12962-134">OUTPUTS</span></span>

### <span data-ttu-id="12962-135">Microsoft. AzureStack. Management. Update. admin. models. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="12962-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="12962-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12962-136">NOTES</span></span>

## <span data-ttu-id="12962-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12962-137">RELATED LINKS</span></span>
