---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4e3e69a0c55188514a31dbe7377f8336784b114
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840267"
---
# <span data-ttu-id="febea-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="febea-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="febea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="febea-102">SYNOPSIS</span></span>
<span data-ttu-id="febea-103">Törölt tárolási fiók törlésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="febea-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="febea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="febea-104">SYNTAX</span></span>

### <span data-ttu-id="febea-105">Törlés visszavonása (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="febea-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="febea-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="febea-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="febea-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="febea-107">DESCRIPTION</span></span>
<span data-ttu-id="febea-108">Törölt tárolási fiók törlésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="febea-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="febea-109">Példák</span><span class="sxs-lookup"><span data-stu-id="febea-109">EXAMPLES</span></span>

### <span data-ttu-id="febea-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="febea-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="febea-111">Törölt tárolási fiók törlésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="febea-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="febea-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="febea-112">PARAMETERS</span></span>

### <span data-ttu-id="febea-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="febea-113">-FarmName</span></span>
<span data-ttu-id="febea-114">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="febea-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febea-115">-Force</span><span class="sxs-lookup"><span data-stu-id="febea-115">-Force</span></span>
<span data-ttu-id="febea-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="febea-116">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febea-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="febea-117">-Name</span></span>
<span data-ttu-id="febea-118">Belső tárterület-azonosító, amely nem látható a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="febea-118">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="febea-119">-ResourceGroupName</span></span>
<span data-ttu-id="febea-120">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="febea-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febea-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="febea-121">-ResourceId</span></span>
<span data-ttu-id="febea-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="febea-122">The resource id.</span></span>

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

### <span data-ttu-id="febea-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="febea-123">-Confirm</span></span>
<span data-ttu-id="febea-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="febea-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="febea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="febea-125">-WhatIf</span></span>
<span data-ttu-id="febea-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="febea-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="febea-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="febea-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="febea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="febea-128">CommonParameters</span></span>
<span data-ttu-id="febea-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="febea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="febea-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="febea-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="febea-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="febea-131">INPUTS</span></span>

## <span data-ttu-id="febea-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="febea-132">OUTPUTS</span></span>

## <span data-ttu-id="febea-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="febea-133">NOTES</span></span>

## <span data-ttu-id="febea-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="febea-134">RELATED LINKS</span></span>

