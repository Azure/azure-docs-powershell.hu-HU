---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdf0c09e087779e9a08161f2af6f9070f193c31b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490908"
---
# <span data-ttu-id="a980b-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="a980b-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="a980b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a980b-102">SYNOPSIS</span></span>
<span data-ttu-id="a980b-103">Az összes logikai hálózat listáját számítja ki egy helyen.</span><span class="sxs-lookup"><span data-stu-id="a980b-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="a980b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a980b-104">SYNTAX</span></span>

### <span data-ttu-id="a980b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a980b-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a980b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="a980b-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a980b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a980b-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a980b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a980b-108">DESCRIPTION</span></span>
<span data-ttu-id="a980b-109">Az összes logikai hálózat listáját számítja ki egy helyen.</span><span class="sxs-lookup"><span data-stu-id="a980b-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="a980b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a980b-110">EXAMPLES</span></span>

### <span data-ttu-id="a980b-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a980b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="a980b-112">Minden logikai hálózat beolvasása egy helyen.</span><span class="sxs-lookup"><span data-stu-id="a980b-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="a980b-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a980b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="a980b-114">Meghatározott logikai hálózatok beszerzése egy név alapján</span><span class="sxs-lookup"><span data-stu-id="a980b-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="a980b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a980b-115">PARAMETERS</span></span>

### <span data-ttu-id="a980b-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="a980b-116">-Filter</span></span>
<span data-ttu-id="a980b-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="a980b-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="a980b-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="a980b-118">-Location</span></span>
<span data-ttu-id="a980b-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="a980b-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a980b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a980b-120">-Name</span></span>
<span data-ttu-id="a980b-121">A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="a980b-121">Name of the logical network.</span></span>

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

### <span data-ttu-id="a980b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a980b-122">-ResourceGroupName</span></span>
<span data-ttu-id="a980b-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="a980b-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a980b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a980b-124">-ResourceId</span></span>
<span data-ttu-id="a980b-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a980b-125">The resource id.</span></span>

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

### <span data-ttu-id="a980b-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="a980b-126">-Skip</span></span>
<span data-ttu-id="a980b-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="a980b-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a980b-128">-Top</span><span class="sxs-lookup"><span data-stu-id="a980b-128">-Top</span></span>
<span data-ttu-id="a980b-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="a980b-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a980b-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="a980b-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a980b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a980b-131">CommonParameters</span></span>
<span data-ttu-id="a980b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a980b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a980b-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a980b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a980b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a980b-134">INPUTS</span></span>

## <span data-ttu-id="a980b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a980b-135">OUTPUTS</span></span>

### <span data-ttu-id="a980b-136">Microsoft. AzureStack. Management. Fabric. admin. models. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="a980b-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="a980b-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a980b-137">NOTES</span></span>

## <span data-ttu-id="a980b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a980b-138">RELATED LINKS</span></span>

