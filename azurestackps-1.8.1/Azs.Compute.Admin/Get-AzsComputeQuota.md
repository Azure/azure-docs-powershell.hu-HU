---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840790"
---
# <span data-ttu-id="6f6dc-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="6f6dc-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="6f6dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="6f6dc-103">Olyan kvótákat ad eredményül, amelyek meghatározzák az objektumok számítási kvótáit.</span><span class="sxs-lookup"><span data-stu-id="6f6dc-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="6f6dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f6dc-104">SYNTAX</span></span>

### <span data-ttu-id="6f6dc-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f6dc-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="6f6dc-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="6f6dc-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="6f6dc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f6dc-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6f6dc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f6dc-108">DESCRIPTION</span></span>
<span data-ttu-id="6f6dc-109">A meglévő kvóták listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="6f6dc-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="6f6dc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6f6dc-110">EXAMPLES</span></span>

### <span data-ttu-id="6f6dc-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6f6dc-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="6f6dc-112">A megadott helyen minden számítási kvóta beszerzése.</span><span class="sxs-lookup"><span data-stu-id="6f6dc-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="6f6dc-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6f6dc-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="6f6dc-114">Meghatározott számítási kvóta beszerzése</span><span class="sxs-lookup"><span data-stu-id="6f6dc-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="6f6dc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f6dc-115">PARAMETERS</span></span>

### <span data-ttu-id="6f6dc-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="6f6dc-116">-Location</span></span>
<span data-ttu-id="6f6dc-117">{{Kitöltési hely leírása}}</span><span class="sxs-lookup"><span data-stu-id="6f6dc-117">{{Fill Location Description}}</span></span>

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

### <span data-ttu-id="6f6dc-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6f6dc-118">-Name</span></span>
<span data-ttu-id="6f6dc-119">A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="6f6dc-119">Name of the quota.</span></span>

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

### <span data-ttu-id="6f6dc-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f6dc-120">-ResourceId</span></span>
<span data-ttu-id="6f6dc-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6f6dc-121">The resource id.</span></span>

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

### <span data-ttu-id="6f6dc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f6dc-122">CommonParameters</span></span>
<span data-ttu-id="6f6dc-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f6dc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f6dc-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f6dc-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f6dc-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f6dc-125">INPUTS</span></span>

## <span data-ttu-id="6f6dc-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f6dc-126">OUTPUTS</span></span>

### <span data-ttu-id="6f6dc-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="6f6dc-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="6f6dc-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f6dc-128">NOTES</span></span>

## <span data-ttu-id="6f6dc-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f6dc-129">RELATED LINKS</span></span>

