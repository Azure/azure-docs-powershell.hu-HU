---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840369"
---
# <span data-ttu-id="4ed48-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="4ed48-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="4ed48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ed48-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed48-103">Kvóta törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="4ed48-103">Delete a quota by name.</span></span>

## <span data-ttu-id="4ed48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ed48-104">SYNTAX</span></span>

### <span data-ttu-id="4ed48-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ed48-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ed48-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ed48-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ed48-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ed48-107">DESCRIPTION</span></span>
<span data-ttu-id="4ed48-108">Kvóta törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="4ed48-108">Delete a quota by name.</span></span>

## <span data-ttu-id="4ed48-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4ed48-109">EXAMPLES</span></span>

### <span data-ttu-id="4ed48-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="4ed48-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="4ed48-111">Hálózati kvóta törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="4ed48-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="4ed48-112">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="4ed48-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="4ed48-113">Hálózati kvóta eltávolítása a pipe segítségével</span><span class="sxs-lookup"><span data-stu-id="4ed48-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="4ed48-114">3. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="4ed48-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="4ed48-115">Hálózati kvóta eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="4ed48-115">Remove a network quota.</span></span>

## <span data-ttu-id="4ed48-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ed48-116">PARAMETERS</span></span>

### <span data-ttu-id="4ed48-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ed48-117">-Name</span></span>
<span data-ttu-id="4ed48-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4ed48-118">Name of the resource.</span></span>

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

### <span data-ttu-id="4ed48-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="4ed48-119">-Location</span></span>
<span data-ttu-id="4ed48-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="4ed48-120">Location of the resource.</span></span>

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

### <span data-ttu-id="4ed48-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ed48-121">-ResourceId</span></span>
<span data-ttu-id="4ed48-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4ed48-122">The resource id.</span></span>

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

### <span data-ttu-id="4ed48-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ed48-123">-AsJob</span></span>
<span data-ttu-id="4ed48-124">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="4ed48-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="4ed48-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4ed48-125">-Force</span></span>
<span data-ttu-id="4ed48-126">Kapcsoló paraméter a megerősítést kérő üzenet mellőzéséhez.</span><span class="sxs-lookup"><span data-stu-id="4ed48-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="4ed48-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed48-127">-WhatIf</span></span>
<span data-ttu-id="4ed48-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4ed48-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ed48-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ed48-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ed48-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ed48-130">-Confirm</span></span>
<span data-ttu-id="4ed48-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ed48-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ed48-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed48-132">CommonParameters</span></span>
<span data-ttu-id="4ed48-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ed48-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed48-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed48-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed48-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ed48-135">INPUTS</span></span>

## <span data-ttu-id="4ed48-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ed48-136">OUTPUTS</span></span>

## <span data-ttu-id="4ed48-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ed48-137">NOTES</span></span>

## <span data-ttu-id="4ed48-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ed48-138">RELATED LINKS</span></span>
