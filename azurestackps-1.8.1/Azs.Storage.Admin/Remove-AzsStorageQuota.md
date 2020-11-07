---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0983e05a36de72148571ccbbc7f1454343ad393a
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840837"
---
# <span data-ttu-id="a5e83-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="a5e83-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="a5e83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5e83-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e83-103">Meglévő kvóta törlése</span><span class="sxs-lookup"><span data-stu-id="a5e83-103">Delete an existing quota</span></span>

## <span data-ttu-id="a5e83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5e83-104">SYNTAX</span></span>

### <span data-ttu-id="a5e83-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5e83-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e83-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5e83-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5e83-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5e83-107">DESCRIPTION</span></span>
<span data-ttu-id="a5e83-108">Meglévő kvóta törlése</span><span class="sxs-lookup"><span data-stu-id="a5e83-108">Delete an existing quota</span></span>

## <span data-ttu-id="a5e83-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a5e83-109">EXAMPLES</span></span>

### <span data-ttu-id="a5e83-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="a5e83-110">EXAMPLE 1</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="a5e83-111">Tárolási kvóta eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="a5e83-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="a5e83-112">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="a5e83-112">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="a5e83-113">Tárolási kvóta eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a5e83-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="a5e83-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5e83-114">PARAMETERS</span></span>

### <span data-ttu-id="a5e83-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5e83-115">-Name</span></span>
<span data-ttu-id="a5e83-116">A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="a5e83-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="a5e83-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="a5e83-117">-Location</span></span>
<span data-ttu-id="a5e83-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="a5e83-118">Resource location.</span></span>

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

### <span data-ttu-id="a5e83-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5e83-119">-ResourceId</span></span>
<span data-ttu-id="a5e83-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a5e83-120">The resource id.</span></span>

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

### <span data-ttu-id="a5e83-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a5e83-121">-Force</span></span>
<span data-ttu-id="a5e83-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5e83-122">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a5e83-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e83-123">-WhatIf</span></span>
<span data-ttu-id="a5e83-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5e83-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5e83-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5e83-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e83-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5e83-126">-Confirm</span></span>
<span data-ttu-id="a5e83-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5e83-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e83-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e83-128">CommonParameters</span></span>
<span data-ttu-id="a5e83-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5e83-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e83-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e83-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e83-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5e83-131">INPUTS</span></span>

## <span data-ttu-id="a5e83-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5e83-132">OUTPUTS</span></span>

## <span data-ttu-id="a5e83-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5e83-133">NOTES</span></span>

## <span data-ttu-id="a5e83-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5e83-134">RELATED LINKS</span></span>
