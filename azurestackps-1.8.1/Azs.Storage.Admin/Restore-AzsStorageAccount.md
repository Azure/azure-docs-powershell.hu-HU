---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 769567562199d33116911f1f1f5e258ae2decbbe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840833"
---
# <span data-ttu-id="8c747-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c747-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="8c747-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c747-102">SYNOPSIS</span></span>
<span data-ttu-id="8c747-103">Törölt tárolási fiók törlésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="8c747-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="8c747-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c747-104">SYNTAX</span></span>

### <span data-ttu-id="8c747-105">Törlés visszavonása (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c747-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c747-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c747-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c747-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c747-107">DESCRIPTION</span></span>
<span data-ttu-id="8c747-108">Törölt tárolási fiók törlésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="8c747-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="8c747-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8c747-109">EXAMPLES</span></span>

### <span data-ttu-id="8c747-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="8c747-110">EXAMPLE 1</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="8c747-111">Törölt tárolási fiók törlésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="8c747-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="8c747-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c747-112">PARAMETERS</span></span>

### <span data-ttu-id="8c747-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="8c747-113">-FarmName</span></span>
<span data-ttu-id="8c747-114">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="8c747-114">Farm Id.</span></span>

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

### <span data-ttu-id="8c747-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c747-115">-Name</span></span>
<span data-ttu-id="8c747-116">Belső tárterület-azonosító, amely nem látható a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="8c747-116">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="8c747-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c747-117">-ResourceGroupName</span></span>
<span data-ttu-id="8c747-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8c747-118">Resource group name.</span></span>

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

### <span data-ttu-id="8c747-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c747-119">-ResourceId</span></span>
<span data-ttu-id="8c747-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="8c747-120">The resource id.</span></span>

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

### <span data-ttu-id="8c747-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8c747-121">-Force</span></span>
<span data-ttu-id="8c747-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c747-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8c747-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c747-123">-WhatIf</span></span>
<span data-ttu-id="8c747-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8c747-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c747-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c747-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c747-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8c747-126">-Confirm</span></span>
<span data-ttu-id="8c747-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c747-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c747-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c747-128">CommonParameters</span></span>
<span data-ttu-id="8c747-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c747-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c747-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c747-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c747-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c747-131">INPUTS</span></span>

## <span data-ttu-id="8c747-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c747-132">OUTPUTS</span></span>

## <span data-ttu-id="8c747-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c747-133">NOTES</span></span>

## <span data-ttu-id="8c747-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c747-134">RELATED LINKS</span></span>
