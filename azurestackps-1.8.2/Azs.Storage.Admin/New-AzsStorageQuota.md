---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cc08220a92dce5a49544cf958db79d7243b9ebb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017057"
---
# <span data-ttu-id="66957-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="66957-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="66957-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66957-102">SYNOPSIS</span></span>
<span data-ttu-id="66957-103">Hozzon létre egy új tárolási kvótát.</span><span class="sxs-lookup"><span data-stu-id="66957-103">Create a new storage quota.</span></span>

## <span data-ttu-id="66957-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66957-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66957-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66957-105">DESCRIPTION</span></span>
<span data-ttu-id="66957-106">Hozzon létre egy új tárolási kvótát.</span><span class="sxs-lookup"><span data-stu-id="66957-106">Create a new storage quota.</span></span>

## <span data-ttu-id="66957-107">Példák</span><span class="sxs-lookup"><span data-stu-id="66957-107">EXAMPLES</span></span>

### <span data-ttu-id="66957-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="66957-108">EXAMPLE 1</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="66957-109">Új tárolási kvóta létrehozása megadott értékekkel</span><span class="sxs-lookup"><span data-stu-id="66957-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="66957-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66957-110">PARAMETERS</span></span>

### <span data-ttu-id="66957-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="66957-111">-Name</span></span>
<span data-ttu-id="66957-112">A tárolási kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="66957-112">The name of the storage quota.</span></span>

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

### <span data-ttu-id="66957-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="66957-113">-CapacityInGb</span></span>
<span data-ttu-id="66957-114">Maximális kapacitása (GB)</span><span class="sxs-lookup"><span data-stu-id="66957-114">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="66957-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="66957-115">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="66957-116">A tárolási fiókok teljes száma.</span><span class="sxs-lookup"><span data-stu-id="66957-116">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="66957-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="66957-117">-Location</span></span>
<span data-ttu-id="66957-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="66957-118">Resource location.</span></span>

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

### <span data-ttu-id="66957-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66957-119">-WhatIf</span></span>
<span data-ttu-id="66957-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="66957-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66957-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66957-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66957-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="66957-122">-Confirm</span></span>
<span data-ttu-id="66957-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="66957-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66957-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66957-124">CommonParameters</span></span>
<span data-ttu-id="66957-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66957-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66957-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66957-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66957-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66957-127">INPUTS</span></span>

## <span data-ttu-id="66957-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66957-128">OUTPUTS</span></span>

### <span data-ttu-id="66957-129">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="66957-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="66957-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66957-130">NOTES</span></span>

## <span data-ttu-id="66957-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66957-131">RELATED LINKS</span></span>
