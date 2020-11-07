---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cc08220a92dce5a49544cf958db79d7243b9ebb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840834"
---
# <span data-ttu-id="aa45b-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="aa45b-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="aa45b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa45b-102">SYNOPSIS</span></span>
<span data-ttu-id="aa45b-103">Hozzon létre egy új tárolási kvótát.</span><span class="sxs-lookup"><span data-stu-id="aa45b-103">Create a new storage quota.</span></span>

## <span data-ttu-id="aa45b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa45b-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa45b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa45b-105">DESCRIPTION</span></span>
<span data-ttu-id="aa45b-106">Hozzon létre egy új tárolási kvótát.</span><span class="sxs-lookup"><span data-stu-id="aa45b-106">Create a new storage quota.</span></span>

## <span data-ttu-id="aa45b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa45b-107">EXAMPLES</span></span>

### <span data-ttu-id="aa45b-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="aa45b-108">EXAMPLE 1</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="aa45b-109">Új tárolási kvóta létrehozása megadott értékekkel</span><span class="sxs-lookup"><span data-stu-id="aa45b-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="aa45b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa45b-110">PARAMETERS</span></span>

### <span data-ttu-id="aa45b-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa45b-111">-Name</span></span>
<span data-ttu-id="aa45b-112">A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="aa45b-112">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa45b-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="aa45b-113">-CapacityInGb</span></span>
<span data-ttu-id="aa45b-114">Maximális kapacitása (GB)</span><span class="sxs-lookup"><span data-stu-id="aa45b-114">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa45b-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="aa45b-115">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="aa45b-116">A tárolási fiókok teljes száma.</span><span class="sxs-lookup"><span data-stu-id="aa45b-116">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa45b-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="aa45b-117">-Location</span></span>
<span data-ttu-id="aa45b-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="aa45b-118">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa45b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa45b-119">-WhatIf</span></span>
<span data-ttu-id="aa45b-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa45b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa45b-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa45b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa45b-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa45b-122">-Confirm</span></span>
<span data-ttu-id="aa45b-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa45b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa45b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa45b-124">CommonParameters</span></span>
<span data-ttu-id="aa45b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa45b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa45b-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa45b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa45b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa45b-127">INPUTS</span></span>

## <span data-ttu-id="aa45b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa45b-128">OUTPUTS</span></span>

### <span data-ttu-id="aa45b-129">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="aa45b-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="aa45b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa45b-130">NOTES</span></span>

## <span data-ttu-id="aa45b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa45b-131">RELATED LINKS</span></span>
