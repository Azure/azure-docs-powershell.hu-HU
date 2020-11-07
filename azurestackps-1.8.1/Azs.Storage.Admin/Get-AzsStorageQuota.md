---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 687838573459c09ceaf08c0d1c3335caa4a99769
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840598"
---
# <span data-ttu-id="12b9d-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="12b9d-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="12b9d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="12b9d-103">A megadott helyen lévő tárterület-kvóták listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="12b9d-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="12b9d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12b9d-104">SYNTAX</span></span>

### <span data-ttu-id="12b9d-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12b9d-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="12b9d-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="12b9d-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="12b9d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="12b9d-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="12b9d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="12b9d-108">DESCRIPTION</span></span>
<span data-ttu-id="12b9d-109">A megadott helyen lévő tárterület-kvóták listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="12b9d-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="12b9d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="12b9d-110">EXAMPLES</span></span>

### <span data-ttu-id="12b9d-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="12b9d-111">EXAMPLE 1</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="12b9d-112">A tárterület-kvóták listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="12b9d-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="12b9d-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="12b9d-113">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="12b9d-114">A megadott tárolási kvótáról a név alapján tájékozódhat.</span><span class="sxs-lookup"><span data-stu-id="12b9d-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="12b9d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12b9d-115">PARAMETERS</span></span>

### <span data-ttu-id="12b9d-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="12b9d-116">-Name</span></span>
<span data-ttu-id="12b9d-117">A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="12b9d-117">The name of the storage quota.</span></span>

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

### <span data-ttu-id="12b9d-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="12b9d-118">-Location</span></span>
<span data-ttu-id="12b9d-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="12b9d-119">Resource location.</span></span>

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

### <span data-ttu-id="12b9d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12b9d-120">-ResourceId</span></span>
<span data-ttu-id="12b9d-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="12b9d-121">The resource id.</span></span>

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

### <span data-ttu-id="12b9d-122">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="12b9d-122">-Skip</span></span>
<span data-ttu-id="12b9d-123">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="12b9d-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="12b9d-124">-Top</span><span class="sxs-lookup"><span data-stu-id="12b9d-124">-Top</span></span>
<span data-ttu-id="12b9d-125">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="12b9d-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="12b9d-126">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="12b9d-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="12b9d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b9d-127">CommonParameters</span></span>
<span data-ttu-id="12b9d-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12b9d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b9d-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b9d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b9d-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12b9d-130">INPUTS</span></span>

## <span data-ttu-id="12b9d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12b9d-131">OUTPUTS</span></span>

### <span data-ttu-id="12b9d-132">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="12b9d-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="12b9d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12b9d-133">NOTES</span></span>

## <span data-ttu-id="12b9d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12b9d-134">RELATED LINKS</span></span>
