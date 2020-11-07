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
ms.locfileid: "93839738"
---
# <span data-ttu-id="5563c-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="5563c-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="5563c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5563c-102">SYNOPSIS</span></span>
<span data-ttu-id="5563c-103">Meglévő kvóta törlése</span><span class="sxs-lookup"><span data-stu-id="5563c-103">Delete an existing quota</span></span>

## <span data-ttu-id="5563c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5563c-104">SYNTAX</span></span>

### <span data-ttu-id="5563c-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5563c-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5563c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5563c-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5563c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5563c-107">DESCRIPTION</span></span>
<span data-ttu-id="5563c-108">Meglévő kvóta törlése</span><span class="sxs-lookup"><span data-stu-id="5563c-108">Delete an existing quota</span></span>

## <span data-ttu-id="5563c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5563c-109">EXAMPLES</span></span>

### <span data-ttu-id="5563c-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5563c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="5563c-111">Tárolási kvóta eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="5563c-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="5563c-112">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5563c-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="5563c-113">Tárolási kvóta eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5563c-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="5563c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5563c-114">PARAMETERS</span></span>

### <span data-ttu-id="5563c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5563c-115">-Force</span></span>
<span data-ttu-id="5563c-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5563c-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5563c-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="5563c-117">-Location</span></span>
<span data-ttu-id="5563c-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="5563c-118">Resource location.</span></span>

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

### <span data-ttu-id="5563c-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5563c-119">-Name</span></span>
<span data-ttu-id="5563c-120">A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="5563c-120">The name of the storage quota.</span></span>

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

### <span data-ttu-id="5563c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5563c-121">-ResourceId</span></span>
<span data-ttu-id="5563c-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5563c-122">The resource id.</span></span>

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

### <span data-ttu-id="5563c-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5563c-123">-Confirm</span></span>
<span data-ttu-id="5563c-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5563c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5563c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5563c-125">-WhatIf</span></span>
<span data-ttu-id="5563c-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5563c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5563c-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5563c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5563c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5563c-128">CommonParameters</span></span>
<span data-ttu-id="5563c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5563c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5563c-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5563c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5563c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5563c-131">INPUTS</span></span>

## <span data-ttu-id="5563c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5563c-132">OUTPUTS</span></span>

## <span data-ttu-id="5563c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5563c-133">NOTES</span></span>

## <span data-ttu-id="5563c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5563c-134">RELATED LINKS</span></span>

