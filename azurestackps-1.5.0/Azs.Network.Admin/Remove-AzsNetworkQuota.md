---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f7f40982a4c7d24e02e7e365163cc6250ff8791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490999"
---
# <span data-ttu-id="57eb1-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="57eb1-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="57eb1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="57eb1-103">Kvóta törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="57eb1-103">Delete a quota by name.</span></span>

## <span data-ttu-id="57eb1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57eb1-104">SYNTAX</span></span>

### <span data-ttu-id="57eb1-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="57eb1-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57eb1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="57eb1-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57eb1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="57eb1-107">DESCRIPTION</span></span>
<span data-ttu-id="57eb1-108">Kvóta törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="57eb1-108">Delete a quota by name.</span></span>

## <span data-ttu-id="57eb1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="57eb1-109">EXAMPLES</span></span>

### <span data-ttu-id="57eb1-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="57eb1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="57eb1-111">Hálózati kvóta törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="57eb1-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="57eb1-112">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="57eb1-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="57eb1-113">Hálózati kvóta eltávolítása a pipe segítségével</span><span class="sxs-lookup"><span data-stu-id="57eb1-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="57eb1-114">PÉLDA--------------------------3--------------------------</span><span class="sxs-lookup"><span data-stu-id="57eb1-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="57eb1-115">Hálózati kvóta eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="57eb1-115">Remove a network quota.</span></span>

## <span data-ttu-id="57eb1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57eb1-116">PARAMETERS</span></span>

### <span data-ttu-id="57eb1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57eb1-117">-AsJob</span></span>
<span data-ttu-id="57eb1-118">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="57eb1-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="57eb1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="57eb1-119">-Force</span></span>
<span data-ttu-id="57eb1-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="57eb1-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="57eb1-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="57eb1-121">-Location</span></span>
<span data-ttu-id="57eb1-122">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="57eb1-122">Location of the resource.</span></span>

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

### <span data-ttu-id="57eb1-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="57eb1-123">-Name</span></span>
<span data-ttu-id="57eb1-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="57eb1-124">Name of the resource.</span></span>

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

### <span data-ttu-id="57eb1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57eb1-125">-ResourceId</span></span>
<span data-ttu-id="57eb1-126">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="57eb1-126">The resource id.</span></span>

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

### <span data-ttu-id="57eb1-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="57eb1-127">-Confirm</span></span>
<span data-ttu-id="57eb1-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="57eb1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57eb1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57eb1-129">-WhatIf</span></span>
<span data-ttu-id="57eb1-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="57eb1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57eb1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="57eb1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57eb1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57eb1-132">CommonParameters</span></span>
<span data-ttu-id="57eb1-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57eb1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57eb1-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57eb1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57eb1-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57eb1-135">INPUTS</span></span>

## <span data-ttu-id="57eb1-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57eb1-136">OUTPUTS</span></span>

## <span data-ttu-id="57eb1-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57eb1-137">NOTES</span></span>

## <span data-ttu-id="57eb1-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57eb1-138">RELATED LINKS</span></span>

