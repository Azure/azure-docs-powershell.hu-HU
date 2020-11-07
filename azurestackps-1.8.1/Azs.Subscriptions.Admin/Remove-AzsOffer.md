---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74772615551979a9ab0cdba3603305489698e212
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840461"
---
# <span data-ttu-id="19ec7-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="19ec7-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="19ec7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="19ec7-103">A megadott ajánlat törlése</span><span class="sxs-lookup"><span data-stu-id="19ec7-103">Delete the specified offer.</span></span>

## <span data-ttu-id="19ec7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19ec7-104">SYNTAX</span></span>

### <span data-ttu-id="19ec7-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19ec7-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19ec7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="19ec7-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19ec7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="19ec7-107">DESCRIPTION</span></span>
<span data-ttu-id="19ec7-108">A megadott ajánlat törlése</span><span class="sxs-lookup"><span data-stu-id="19ec7-108">Delete the specified offer.</span></span>

## <span data-ttu-id="19ec7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="19ec7-109">EXAMPLES</span></span>

### <span data-ttu-id="19ec7-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="19ec7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="19ec7-111">A megadott ajánlat törlése</span><span class="sxs-lookup"><span data-stu-id="19ec7-111">Delete the specified offer.</span></span>

## <span data-ttu-id="19ec7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19ec7-112">PARAMETERS</span></span>

### <span data-ttu-id="19ec7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="19ec7-113">-Force</span></span>
<span data-ttu-id="19ec7-114">Jelölő az elem megerősítés nélküli eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="19ec7-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="19ec7-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19ec7-115">-Name</span></span>
<span data-ttu-id="19ec7-116">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="19ec7-116">Name of an offer.</span></span>

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

### <span data-ttu-id="19ec7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19ec7-117">-ResourceGroupName</span></span>
<span data-ttu-id="19ec7-118">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="19ec7-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="19ec7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19ec7-119">-ResourceId</span></span>
<span data-ttu-id="19ec7-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="19ec7-120">The resource id.</span></span>

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

### <span data-ttu-id="19ec7-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19ec7-121">-Confirm</span></span>
<span data-ttu-id="19ec7-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19ec7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19ec7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19ec7-123">-WhatIf</span></span>
<span data-ttu-id="19ec7-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19ec7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19ec7-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19ec7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19ec7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19ec7-126">CommonParameters</span></span>
<span data-ttu-id="19ec7-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19ec7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19ec7-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19ec7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19ec7-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19ec7-129">INPUTS</span></span>

## <span data-ttu-id="19ec7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19ec7-130">OUTPUTS</span></span>

## <span data-ttu-id="19ec7-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19ec7-131">NOTES</span></span>

## <span data-ttu-id="19ec7-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19ec7-132">RELATED LINKS</span></span>

