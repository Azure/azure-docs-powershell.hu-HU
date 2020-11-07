---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb535146787c4c33a57ad406f05544f18ba74eb0
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840543"
---
# <span data-ttu-id="f5be9-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="f5be9-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="f5be9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5be9-102">SYNOPSIS</span></span>
<span data-ttu-id="f5be9-103">Az összes logikai alhálózat listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="f5be9-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="f5be9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5be9-104">SYNTAX</span></span>

### <span data-ttu-id="f5be9-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5be9-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f5be9-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="f5be9-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5be9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5be9-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f5be9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5be9-108">DESCRIPTION</span></span>
<span data-ttu-id="f5be9-109">Az összes logikai alhálózat listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="f5be9-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="f5be9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f5be9-110">EXAMPLES</span></span>

### <span data-ttu-id="f5be9-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="f5be9-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="f5be9-112">Az összes logikai alhálózat listája az adott logikai hálózat és hely számára</span><span class="sxs-lookup"><span data-stu-id="f5be9-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="f5be9-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="f5be9-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="f5be9-114">Adott logikai hálózat és hely esetén a név alapján meghatározott logikai alhálózat beszerzése.</span><span class="sxs-lookup"><span data-stu-id="f5be9-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="f5be9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5be9-115">PARAMETERS</span></span>

### <span data-ttu-id="f5be9-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5be9-116">-Name</span></span>
<span data-ttu-id="f5be9-117">A logikai alhálózat neve</span><span class="sxs-lookup"><span data-stu-id="f5be9-117">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="f5be9-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="f5be9-118">-LogicalNetwork</span></span>
<span data-ttu-id="f5be9-119">A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="f5be9-119">Name of the logical network.</span></span>

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

### <span data-ttu-id="f5be9-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="f5be9-120">-Location</span></span>
<span data-ttu-id="f5be9-121">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="f5be9-121">Location of the resource.</span></span>

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

### <span data-ttu-id="f5be9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5be9-122">-ResourceGroupName</span></span>
<span data-ttu-id="f5be9-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="f5be9-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f5be9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5be9-124">-ResourceId</span></span>
<span data-ttu-id="f5be9-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f5be9-125">The resource id.</span></span>

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

### <span data-ttu-id="f5be9-126">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="f5be9-126">-Filter</span></span>
<span data-ttu-id="f5be9-127">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="f5be9-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="f5be9-128">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="f5be9-128">-Skip</span></span>
<span data-ttu-id="f5be9-129">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="f5be9-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f5be9-130">-Top</span><span class="sxs-lookup"><span data-stu-id="f5be9-130">-Top</span></span>
<span data-ttu-id="f5be9-131">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="f5be9-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f5be9-132">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="f5be9-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f5be9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5be9-133">CommonParameters</span></span>
<span data-ttu-id="f5be9-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5be9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5be9-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5be9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5be9-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5be9-136">INPUTS</span></span>

## <span data-ttu-id="f5be9-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5be9-137">OUTPUTS</span></span>

### <span data-ttu-id="f5be9-138">Microsoft. AzureStack. Management. Fabric. admin. models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="f5be9-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="f5be9-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5be9-139">NOTES</span></span>

## <span data-ttu-id="f5be9-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5be9-140">RELATED LINKS</span></span>
