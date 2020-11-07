---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb535146787c4c33a57ad406f05544f18ba74eb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840203"
---
# <span data-ttu-id="a3205-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="a3205-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="a3205-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3205-102">SYNOPSIS</span></span>
<span data-ttu-id="a3205-103">Az összes logikai alhálózat listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a3205-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="a3205-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3205-104">SYNTAX</span></span>

### <span data-ttu-id="a3205-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3205-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a3205-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="a3205-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3205-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3205-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a3205-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3205-108">DESCRIPTION</span></span>
<span data-ttu-id="a3205-109">Az összes logikai alhálózat listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="a3205-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="a3205-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a3205-110">EXAMPLES</span></span>

### <span data-ttu-id="a3205-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="a3205-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="a3205-112">Az összes logikai alhálózat listája az adott logikai hálózat és hely számára</span><span class="sxs-lookup"><span data-stu-id="a3205-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="a3205-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="a3205-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="a3205-114">Adott logikai hálózat és hely esetén a név alapján meghatározott logikai alhálózat beszerzése.</span><span class="sxs-lookup"><span data-stu-id="a3205-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="a3205-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3205-115">PARAMETERS</span></span>

### <span data-ttu-id="a3205-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a3205-116">-Name</span></span>
<span data-ttu-id="a3205-117">A logikai alhálózat neve</span><span class="sxs-lookup"><span data-stu-id="a3205-117">Name of the logical subnet.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3205-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="a3205-118">-LogicalNetwork</span></span>
<span data-ttu-id="a3205-119">A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="a3205-119">Name of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3205-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="a3205-120">-Location</span></span>
<span data-ttu-id="a3205-121">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="a3205-121">Location of the resource.</span></span>

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

### <span data-ttu-id="a3205-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3205-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3205-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="a3205-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a3205-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3205-124">-ResourceId</span></span>
<span data-ttu-id="a3205-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a3205-125">The resource id.</span></span>

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

### <span data-ttu-id="a3205-126">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="a3205-126">-Filter</span></span>
<span data-ttu-id="a3205-127">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="a3205-127">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3205-128">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="a3205-128">-Skip</span></span>
<span data-ttu-id="a3205-129">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="a3205-129">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3205-130">-Top</span><span class="sxs-lookup"><span data-stu-id="a3205-130">-Top</span></span>
<span data-ttu-id="a3205-131">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="a3205-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a3205-132">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="a3205-132">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3205-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3205-133">CommonParameters</span></span>
<span data-ttu-id="a3205-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3205-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3205-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3205-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3205-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3205-136">INPUTS</span></span>

## <span data-ttu-id="a3205-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3205-137">OUTPUTS</span></span>

### <span data-ttu-id="a3205-138">Microsoft. AzureStack. Management. Fabric. admin. models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="a3205-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="a3205-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3205-139">NOTES</span></span>

## <span data-ttu-id="a3205-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3205-140">RELATED LINKS</span></span>
