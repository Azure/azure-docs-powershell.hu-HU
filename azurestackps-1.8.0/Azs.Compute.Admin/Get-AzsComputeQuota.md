---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840252"
---
# <span data-ttu-id="e643d-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="e643d-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="e643d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e643d-102">SYNOPSIS</span></span>
<span data-ttu-id="e643d-103">Olyan kvótákat ad eredményül, amelyek meghatározzák az objektumok számítási kvótáit.</span><span class="sxs-lookup"><span data-stu-id="e643d-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="e643d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e643d-104">SYNTAX</span></span>

### <span data-ttu-id="e643d-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e643d-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="e643d-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e643d-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="e643d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e643d-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e643d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e643d-108">DESCRIPTION</span></span>
<span data-ttu-id="e643d-109">A meglévő kvóták listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e643d-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="e643d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e643d-110">EXAMPLES</span></span>

### <span data-ttu-id="e643d-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e643d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="e643d-112">A megadott helyen minden számítási kvóta beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e643d-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="e643d-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e643d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="e643d-114">Meghatározott számítási kvóta beszerzése</span><span class="sxs-lookup"><span data-stu-id="e643d-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="e643d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e643d-115">PARAMETERS</span></span>

### <span data-ttu-id="e643d-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="e643d-116">-Location</span></span>
<span data-ttu-id="e643d-117">{{Kitöltési hely leírása}}</span><span class="sxs-lookup"><span data-stu-id="e643d-117">{{Fill Location Description}}</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e643d-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e643d-118">-Name</span></span>
<span data-ttu-id="e643d-119">A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="e643d-119">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e643d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e643d-120">-ResourceId</span></span>
<span data-ttu-id="e643d-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e643d-121">The resource id.</span></span>

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

### <span data-ttu-id="e643d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e643d-122">CommonParameters</span></span>
<span data-ttu-id="e643d-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e643d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e643d-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e643d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e643d-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e643d-125">INPUTS</span></span>

## <span data-ttu-id="e643d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e643d-126">OUTPUTS</span></span>

### <span data-ttu-id="e643d-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="e643d-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="e643d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e643d-128">NOTES</span></span>

## <span data-ttu-id="e643d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e643d-129">RELATED LINKS</span></span>

