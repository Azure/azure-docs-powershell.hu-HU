---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 641017c75243a253a6b9eb0054df7737a674f671
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840805"
---
# <span data-ttu-id="037dd-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="037dd-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="037dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="037dd-102">SYNOPSIS</span></span>
<span data-ttu-id="037dd-103">Meglévő tárolási kvóta létrehozása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="037dd-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="037dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="037dd-104">SYNTAX</span></span>

### <span data-ttu-id="037dd-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="037dd-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="037dd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="037dd-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="037dd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="037dd-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="037dd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="037dd-108">DESCRIPTION</span></span>
<span data-ttu-id="037dd-109">Meglévő tárolási kvóta létrehozása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="037dd-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="037dd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="037dd-110">EXAMPLES</span></span>

### <span data-ttu-id="037dd-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="037dd-111">EXAMPLE 1</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="037dd-112">Meglévő tárolási kvóta frissítése</span><span class="sxs-lookup"><span data-stu-id="037dd-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="037dd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="037dd-113">PARAMETERS</span></span>

### <span data-ttu-id="037dd-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="037dd-114">-Name</span></span>
<span data-ttu-id="037dd-115">A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="037dd-115">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037dd-116">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="037dd-116">-CapacityInGb</span></span>
<span data-ttu-id="037dd-117">Maximális kapacitása (GB)</span><span class="sxs-lookup"><span data-stu-id="037dd-117">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037dd-118">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="037dd-118">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="037dd-119">A tárolási fiókok teljes száma.</span><span class="sxs-lookup"><span data-stu-id="037dd-119">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037dd-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="037dd-120">-Location</span></span>
<span data-ttu-id="037dd-121">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="037dd-121">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037dd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="037dd-122">-ResourceId</span></span>
<span data-ttu-id="037dd-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="037dd-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037dd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="037dd-124">-InputObject</span></span>
<span data-ttu-id="037dd-125">A Posbbily módosított tárolási kvótáját a Get-AzsStorageQuota adja vissza.</span><span class="sxs-lookup"><span data-stu-id="037dd-125">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

```yaml
Type: StorageQuota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="037dd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="037dd-126">-WhatIf</span></span>
<span data-ttu-id="037dd-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="037dd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="037dd-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="037dd-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037dd-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="037dd-129">-Confirm</span></span>
<span data-ttu-id="037dd-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="037dd-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037dd-131">CommonParameters</span></span>
<span data-ttu-id="037dd-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="037dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037dd-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="037dd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037dd-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="037dd-134">INPUTS</span></span>

## <span data-ttu-id="037dd-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="037dd-135">OUTPUTS</span></span>

### <span data-ttu-id="037dd-136">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="037dd-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="037dd-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="037dd-137">NOTES</span></span>

## <span data-ttu-id="037dd-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="037dd-138">RELATED LINKS</span></span>
