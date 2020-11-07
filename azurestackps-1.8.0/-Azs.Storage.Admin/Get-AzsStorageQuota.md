---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4277ee88af840674d6fc8e4e2d5f614e745ace
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840401"
---
# <span data-ttu-id="344b1-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="344b1-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="344b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="344b1-102">SYNOPSIS</span></span>
<span data-ttu-id="344b1-103">A megadott helyen lévő tárterület-kvóták listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="344b1-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="344b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="344b1-104">SYNTAX</span></span>

### <span data-ttu-id="344b1-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="344b1-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="344b1-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="344b1-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="344b1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="344b1-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="344b1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="344b1-108">DESCRIPTION</span></span>
<span data-ttu-id="344b1-109">A megadott helyen lévő tárterület-kvóták listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="344b1-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="344b1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="344b1-110">EXAMPLES</span></span>

### <span data-ttu-id="344b1-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="344b1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="344b1-112">A tárterület-kvóták listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="344b1-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="344b1-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="344b1-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="344b1-114">A megadott tárolási kvótáról a név alapján tájékozódhat.</span><span class="sxs-lookup"><span data-stu-id="344b1-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="344b1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="344b1-115">PARAMETERS</span></span>

### <span data-ttu-id="344b1-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="344b1-116">-Location</span></span>
<span data-ttu-id="344b1-117">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="344b1-117">Resource location.</span></span>

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

### <span data-ttu-id="344b1-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="344b1-118">-Name</span></span>
<span data-ttu-id="344b1-119">A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="344b1-119">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344b1-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="344b1-120">-ResourceId</span></span>
<span data-ttu-id="344b1-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="344b1-121">The resource id.</span></span>

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

### <span data-ttu-id="344b1-122">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="344b1-122">-Skip</span></span>
<span data-ttu-id="344b1-123">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="344b1-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="344b1-124">-Top</span><span class="sxs-lookup"><span data-stu-id="344b1-124">-Top</span></span>
<span data-ttu-id="344b1-125">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="344b1-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="344b1-126">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="344b1-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="344b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="344b1-127">CommonParameters</span></span>
<span data-ttu-id="344b1-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="344b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="344b1-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="344b1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="344b1-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="344b1-130">INPUTS</span></span>

## <span data-ttu-id="344b1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="344b1-131">OUTPUTS</span></span>

### <span data-ttu-id="344b1-132">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="344b1-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="344b1-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="344b1-133">NOTES</span></span>

## <span data-ttu-id="344b1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="344b1-134">RELATED LINKS</span></span>

