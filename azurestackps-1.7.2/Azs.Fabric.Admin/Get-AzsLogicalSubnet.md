---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef5db457846f6fdf0dcd0a0a32b37cab96a557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839855"
---
# <span data-ttu-id="7fd1b-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="7fd1b-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="7fd1b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7fd1b-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd1b-103">Az összes logikai alhálózat listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="7fd1b-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="7fd1b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7fd1b-104">SYNTAX</span></span>

### <span data-ttu-id="7fd1b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7fd1b-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7fd1b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="7fd1b-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="7fd1b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fd1b-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7fd1b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7fd1b-108">DESCRIPTION</span></span>
<span data-ttu-id="7fd1b-109">Az összes logikai alhálózat listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="7fd1b-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="7fd1b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7fd1b-110">EXAMPLES</span></span>

### <span data-ttu-id="7fd1b-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7fd1b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="7fd1b-112">Az összes logikai alhálózat listája az adott logikai hálózat és hely számára</span><span class="sxs-lookup"><span data-stu-id="7fd1b-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="7fd1b-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7fd1b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="7fd1b-114">Adott logikai hálózat és hely esetén a név alapján meghatározott logikai alhálózat beszerzése.</span><span class="sxs-lookup"><span data-stu-id="7fd1b-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="7fd1b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7fd1b-115">PARAMETERS</span></span>

### <span data-ttu-id="7fd1b-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="7fd1b-116">-Filter</span></span>
<span data-ttu-id="7fd1b-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="7fd1b-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="7fd1b-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="7fd1b-118">-Location</span></span>
<span data-ttu-id="7fd1b-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="7fd1b-119">Location of the resource.</span></span>

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

### <span data-ttu-id="7fd1b-120">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="7fd1b-120">-LogicalNetwork</span></span>
<span data-ttu-id="7fd1b-121">A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="7fd1b-121">Name of the logical network.</span></span>

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

### <span data-ttu-id="7fd1b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7fd1b-122">-Name</span></span>
<span data-ttu-id="7fd1b-123">A logikai alhálózat neve</span><span class="sxs-lookup"><span data-stu-id="7fd1b-123">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="7fd1b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd1b-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fd1b-125">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="7fd1b-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="7fd1b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fd1b-126">-ResourceId</span></span>
<span data-ttu-id="7fd1b-127">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7fd1b-127">The resource id.</span></span>

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

### <span data-ttu-id="7fd1b-128">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="7fd1b-128">-Skip</span></span>
<span data-ttu-id="7fd1b-129">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="7fd1b-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7fd1b-130">-Top</span><span class="sxs-lookup"><span data-stu-id="7fd1b-130">-Top</span></span>
<span data-ttu-id="7fd1b-131">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="7fd1b-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7fd1b-132">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="7fd1b-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7fd1b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd1b-133">CommonParameters</span></span>
<span data-ttu-id="7fd1b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7fd1b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd1b-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fd1b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd1b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fd1b-136">INPUTS</span></span>

## <span data-ttu-id="7fd1b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fd1b-137">OUTPUTS</span></span>

### <span data-ttu-id="7fd1b-138">Microsoft. AzureStack. Management. Fabric. admin. models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="7fd1b-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="7fd1b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7fd1b-139">NOTES</span></span>

## <span data-ttu-id="7fd1b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fd1b-140">RELATED LINKS</span></span>

