---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2eec56d9fc157da994521a5b258cd28132344c52
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840261"
---
# <span data-ttu-id="5ec7d-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="5ec7d-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="5ec7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ec7d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec7d-103">Meglévő tárolási kvóta létrehozása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="5ec7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ec7d-104">SYNTAX</span></span>

### <span data-ttu-id="5ec7d-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ec7d-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ec7d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ec7d-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ec7d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5ec7d-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ec7d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ec7d-108">DESCRIPTION</span></span>
<span data-ttu-id="5ec7d-109">Meglévő tárolási kvóta létrehozása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="5ec7d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5ec7d-110">EXAMPLES</span></span>

### <span data-ttu-id="5ec7d-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5ec7d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="5ec7d-112">Meglévő tárolási kvóta frissítése</span><span class="sxs-lookup"><span data-stu-id="5ec7d-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="5ec7d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ec7d-113">PARAMETERS</span></span>

### <span data-ttu-id="5ec7d-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="5ec7d-114">-CapacityInGb</span></span>
<span data-ttu-id="5ec7d-115">Maximális kapacitása (GB)</span><span class="sxs-lookup"><span data-stu-id="5ec7d-115">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="5ec7d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ec7d-116">-InputObject</span></span>
<span data-ttu-id="5ec7d-117">A Posbbily módosított tárolási kvótáját a Get-AzsStorageQuota adja vissza.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="5ec7d-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="5ec7d-118">-Location</span></span>
<span data-ttu-id="5ec7d-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-119">Resource location.</span></span>

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

### <span data-ttu-id="5ec7d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ec7d-120">-Name</span></span>
<span data-ttu-id="5ec7d-121">A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-121">The name of the storage quota.</span></span>

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

### <span data-ttu-id="5ec7d-122">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="5ec7d-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="5ec7d-123">A tárolási fiókok teljes száma.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-123">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="5ec7d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ec7d-124">-ResourceId</span></span>
<span data-ttu-id="5ec7d-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-125">The resource id.</span></span>

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

### <span data-ttu-id="5ec7d-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ec7d-126">-Confirm</span></span>
<span data-ttu-id="5ec7d-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ec7d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ec7d-128">-WhatIf</span></span>
<span data-ttu-id="5ec7d-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ec7d-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ec7d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ec7d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec7d-131">CommonParameters</span></span>
<span data-ttu-id="5ec7d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ec7d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec7d-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ec7d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec7d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ec7d-134">INPUTS</span></span>

## <span data-ttu-id="5ec7d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ec7d-135">OUTPUTS</span></span>

### <span data-ttu-id="5ec7d-136">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="5ec7d-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="5ec7d-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ec7d-137">NOTES</span></span>

## <span data-ttu-id="5ec7d-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ec7d-138">RELATED LINKS</span></span>

