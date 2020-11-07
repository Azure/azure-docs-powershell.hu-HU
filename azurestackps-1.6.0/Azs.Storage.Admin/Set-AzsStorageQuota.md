---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2eec56d9fc157da994521a5b258cd28132344c52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671788"
---
# <span data-ttu-id="f6aca-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="f6aca-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="f6aca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6aca-102">SYNOPSIS</span></span>
<span data-ttu-id="f6aca-103">Meglévő tárolási kvóta létrehozása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="f6aca-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="f6aca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6aca-104">SYNTAX</span></span>

### <span data-ttu-id="f6aca-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6aca-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6aca-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6aca-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6aca-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f6aca-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6aca-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6aca-108">DESCRIPTION</span></span>
<span data-ttu-id="f6aca-109">Meglévő tárolási kvóta létrehozása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="f6aca-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="f6aca-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f6aca-110">EXAMPLES</span></span>

### <span data-ttu-id="f6aca-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f6aca-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="f6aca-112">Meglévő tárolási kvóta frissítése</span><span class="sxs-lookup"><span data-stu-id="f6aca-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="f6aca-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6aca-113">PARAMETERS</span></span>

### <span data-ttu-id="f6aca-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="f6aca-114">-CapacityInGb</span></span>
<span data-ttu-id="f6aca-115">Maximális kapacitása (GB)</span><span class="sxs-lookup"><span data-stu-id="f6aca-115">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="f6aca-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6aca-116">-InputObject</span></span>
<span data-ttu-id="f6aca-117">A Posbbily módosított tárolási kvótáját a Get-AzsStorageQuota adja vissza.</span><span class="sxs-lookup"><span data-stu-id="f6aca-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="f6aca-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="f6aca-118">-Location</span></span>
<span data-ttu-id="f6aca-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="f6aca-119">Resource location.</span></span>

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

### <span data-ttu-id="f6aca-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f6aca-120">-Name</span></span>
<span data-ttu-id="f6aca-121">A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="f6aca-121">The name of the storage quota.</span></span>

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

### <span data-ttu-id="f6aca-122">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="f6aca-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="f6aca-123">A tárolási fiókok teljes száma.</span><span class="sxs-lookup"><span data-stu-id="f6aca-123">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="f6aca-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6aca-124">-ResourceId</span></span>
<span data-ttu-id="f6aca-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f6aca-125">The resource id.</span></span>

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

### <span data-ttu-id="f6aca-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6aca-126">-Confirm</span></span>
<span data-ttu-id="f6aca-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6aca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6aca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6aca-128">-WhatIf</span></span>
<span data-ttu-id="f6aca-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6aca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6aca-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6aca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6aca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6aca-131">CommonParameters</span></span>
<span data-ttu-id="f6aca-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6aca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6aca-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6aca-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6aca-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6aca-134">INPUTS</span></span>

## <span data-ttu-id="f6aca-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6aca-135">OUTPUTS</span></span>

### <span data-ttu-id="f6aca-136">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="f6aca-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="f6aca-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6aca-137">NOTES</span></span>

## <span data-ttu-id="f6aca-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6aca-138">RELATED LINKS</span></span>

