---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b62b8ffbdcdcefff5bbb5c984a19ef0b7cb644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491798"
---
# <span data-ttu-id="b9062-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b9062-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="b9062-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9062-102">SYNOPSIS</span></span>
<span data-ttu-id="b9062-103">Meglévő kvóta törlése</span><span class="sxs-lookup"><span data-stu-id="b9062-103">Delete an existing quota</span></span>

## <span data-ttu-id="b9062-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9062-104">SYNTAX</span></span>

### <span data-ttu-id="b9062-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9062-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9062-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9062-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9062-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9062-107">DESCRIPTION</span></span>
<span data-ttu-id="b9062-108">Meglévő kvóta törlése</span><span class="sxs-lookup"><span data-stu-id="b9062-108">Delete an existing quota</span></span>

## <span data-ttu-id="b9062-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b9062-109">EXAMPLES</span></span>

### <span data-ttu-id="b9062-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b9062-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="b9062-111">Tárolási kvóta eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="b9062-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="b9062-112">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b9062-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="b9062-113">Tárolási kvóta eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b9062-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="b9062-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9062-114">PARAMETERS</span></span>

### <span data-ttu-id="b9062-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b9062-115">-Force</span></span>
<span data-ttu-id="b9062-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9062-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b9062-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="b9062-117">-Location</span></span>
<span data-ttu-id="b9062-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="b9062-118">Resource location.</span></span>

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

### <span data-ttu-id="b9062-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9062-119">-Name</span></span>
<span data-ttu-id="b9062-120">A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="b9062-120">The name of the storage quota.</span></span>

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

### <span data-ttu-id="b9062-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9062-121">-ResourceId</span></span>
<span data-ttu-id="b9062-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b9062-122">The resource id.</span></span>

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

### <span data-ttu-id="b9062-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9062-123">-Confirm</span></span>
<span data-ttu-id="b9062-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9062-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9062-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9062-125">-WhatIf</span></span>
<span data-ttu-id="b9062-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9062-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9062-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9062-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9062-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9062-128">CommonParameters</span></span>
<span data-ttu-id="b9062-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9062-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9062-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9062-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9062-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9062-131">INPUTS</span></span>

## <span data-ttu-id="b9062-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9062-132">OUTPUTS</span></span>

## <span data-ttu-id="b9062-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9062-133">NOTES</span></span>

## <span data-ttu-id="b9062-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9062-134">RELATED LINKS</span></span>

