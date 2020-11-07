---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b3fb659c1d11df734bdc95f554e4c100060e185
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840085"
---
# <span data-ttu-id="1d911-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="1d911-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="1d911-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d911-102">SYNOPSIS</span></span>
<span data-ttu-id="1d911-103">Törli a megadott számítási kvótát.</span><span class="sxs-lookup"><span data-stu-id="1d911-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="1d911-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d911-104">SYNTAX</span></span>

### <span data-ttu-id="1d911-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d911-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d911-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d911-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d911-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d911-107">DESCRIPTION</span></span>
<span data-ttu-id="1d911-108">Meglévő kvóta törlése</span><span class="sxs-lookup"><span data-stu-id="1d911-108">Delete an existing quota.</span></span>

## <span data-ttu-id="1d911-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1d911-109">EXAMPLES</span></span>

### <span data-ttu-id="1d911-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1d911-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="1d911-111">Az összes paraméterrel megadott számítási kvóta eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1d911-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="1d911-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d911-112">PARAMETERS</span></span>

### <span data-ttu-id="1d911-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1d911-113">-Force</span></span>
<span data-ttu-id="1d911-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d911-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1d911-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="1d911-115">-Location</span></span>
<span data-ttu-id="1d911-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="1d911-116">Location of the resource.</span></span> <span data-ttu-id="1d911-117">Ha nem adja meg a tenat előfizetéséhez kötött helyet.</span><span class="sxs-lookup"><span data-stu-id="1d911-117">If not given we default to the location bound to the tenat's subscription.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d911-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d911-118">-Name</span></span>
<span data-ttu-id="1d911-119">A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="1d911-119">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d911-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d911-120">-ResourceId</span></span>
<span data-ttu-id="1d911-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="1d911-121">The resource id.</span></span>

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

### <span data-ttu-id="1d911-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1d911-122">-Confirm</span></span>
<span data-ttu-id="1d911-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d911-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d911-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d911-124">-WhatIf</span></span>
<span data-ttu-id="1d911-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1d911-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d911-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d911-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d911-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d911-127">CommonParameters</span></span>
<span data-ttu-id="1d911-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d911-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d911-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d911-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d911-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d911-130">INPUTS</span></span>

## <span data-ttu-id="1d911-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d911-131">OUTPUTS</span></span>

## <span data-ttu-id="1d911-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d911-132">NOTES</span></span>

## <span data-ttu-id="1d911-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d911-133">RELATED LINKS</span></span>

