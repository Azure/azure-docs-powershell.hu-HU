---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ebc1ebae40d6d1726ee6c23def6f82ff1efc8517
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016786"
---
# <span data-ttu-id="c79aa-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="c79aa-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="c79aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c79aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c79aa-103">Törli a megadott számítási kvótát.</span><span class="sxs-lookup"><span data-stu-id="c79aa-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="c79aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c79aa-104">SYNTAX</span></span>

### <span data-ttu-id="c79aa-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c79aa-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c79aa-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c79aa-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c79aa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c79aa-107">DESCRIPTION</span></span>
<span data-ttu-id="c79aa-108">Meglévő kvóta törlése</span><span class="sxs-lookup"><span data-stu-id="c79aa-108">Delete an existing quota.</span></span>

## <span data-ttu-id="c79aa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c79aa-109">EXAMPLES</span></span>

### <span data-ttu-id="c79aa-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c79aa-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="c79aa-111">Az összes paraméterrel megadott számítási kvóta eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="c79aa-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="c79aa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c79aa-112">PARAMETERS</span></span>

### <span data-ttu-id="c79aa-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c79aa-113">-Force</span></span>
<span data-ttu-id="c79aa-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c79aa-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c79aa-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="c79aa-115">-Location</span></span>
<span data-ttu-id="c79aa-116">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="c79aa-116">Location of the resource.</span></span> <span data-ttu-id="c79aa-117">Ha nem adja meg a tenat előfizetéséhez kötött helyet.</span><span class="sxs-lookup"><span data-stu-id="c79aa-117">If not given we default to the location bound to the tenat's subscription.</span></span>

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

### <span data-ttu-id="c79aa-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c79aa-118">-Name</span></span>
<span data-ttu-id="c79aa-119">A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="c79aa-119">Name of the quota.</span></span>

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

### <span data-ttu-id="c79aa-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c79aa-120">-ResourceId</span></span>
<span data-ttu-id="c79aa-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c79aa-121">The resource id.</span></span>

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

### <span data-ttu-id="c79aa-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c79aa-122">-Confirm</span></span>
<span data-ttu-id="c79aa-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c79aa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c79aa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c79aa-124">-WhatIf</span></span>
<span data-ttu-id="c79aa-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c79aa-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c79aa-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c79aa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c79aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c79aa-127">CommonParameters</span></span>
<span data-ttu-id="c79aa-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c79aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c79aa-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c79aa-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c79aa-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c79aa-130">INPUTS</span></span>

## <span data-ttu-id="c79aa-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c79aa-131">OUTPUTS</span></span>

## <span data-ttu-id="c79aa-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c79aa-132">NOTES</span></span>

## <span data-ttu-id="c79aa-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c79aa-133">RELATED LINKS</span></span>

