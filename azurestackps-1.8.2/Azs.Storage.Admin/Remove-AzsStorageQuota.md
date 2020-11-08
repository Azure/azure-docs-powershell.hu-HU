---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0983e05a36de72148571ccbbc7f1454343ad393a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016634"
---
# <span data-ttu-id="1ed40-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="1ed40-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="1ed40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ed40-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed40-103">Meglévő kvóta törlése</span><span class="sxs-lookup"><span data-stu-id="1ed40-103">Delete an existing quota</span></span>

## <span data-ttu-id="1ed40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ed40-104">SYNTAX</span></span>

### <span data-ttu-id="1ed40-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ed40-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ed40-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ed40-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ed40-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ed40-107">DESCRIPTION</span></span>
<span data-ttu-id="1ed40-108">Meglévő kvóta törlése</span><span class="sxs-lookup"><span data-stu-id="1ed40-108">Delete an existing quota</span></span>

## <span data-ttu-id="1ed40-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1ed40-109">EXAMPLES</span></span>

### <span data-ttu-id="1ed40-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="1ed40-110">EXAMPLE 1</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="1ed40-111">Tárolási kvóta eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="1ed40-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="1ed40-112">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="1ed40-112">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="1ed40-113">Tárolási kvóta eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1ed40-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="1ed40-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ed40-114">PARAMETERS</span></span>

### <span data-ttu-id="1ed40-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ed40-115">-Name</span></span>
<span data-ttu-id="1ed40-116">A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="1ed40-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="1ed40-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="1ed40-117">-Location</span></span>
<span data-ttu-id="1ed40-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="1ed40-118">Resource location.</span></span>

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

### <span data-ttu-id="1ed40-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ed40-119">-ResourceId</span></span>
<span data-ttu-id="1ed40-120">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="1ed40-120">The resource id.</span></span>

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

### <span data-ttu-id="1ed40-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1ed40-121">-Force</span></span>
<span data-ttu-id="1ed40-122">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ed40-122">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1ed40-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ed40-123">-WhatIf</span></span>
<span data-ttu-id="1ed40-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ed40-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ed40-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ed40-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ed40-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ed40-126">-Confirm</span></span>
<span data-ttu-id="1ed40-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ed40-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ed40-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed40-128">CommonParameters</span></span>
<span data-ttu-id="1ed40-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ed40-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed40-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed40-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed40-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ed40-131">INPUTS</span></span>

## <span data-ttu-id="1ed40-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ed40-132">OUTPUTS</span></span>

## <span data-ttu-id="1ed40-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ed40-133">NOTES</span></span>

## <span data-ttu-id="1ed40-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ed40-134">RELATED LINKS</span></span>
