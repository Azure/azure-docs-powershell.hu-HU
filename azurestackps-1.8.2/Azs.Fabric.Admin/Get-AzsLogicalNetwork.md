---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88d9fc8456c86f0806313bb0234e145b7f4d727a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016605"
---
# <span data-ttu-id="b4daf-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="b4daf-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="b4daf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4daf-102">SYNOPSIS</span></span>
<span data-ttu-id="b4daf-103">Az összes logikai hálózat listáját számítja ki egy helyen.</span><span class="sxs-lookup"><span data-stu-id="b4daf-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="b4daf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4daf-104">SYNTAX</span></span>

### <span data-ttu-id="b4daf-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4daf-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b4daf-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b4daf-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4daf-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4daf-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b4daf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4daf-108">DESCRIPTION</span></span>
<span data-ttu-id="b4daf-109">Az összes logikai hálózat listáját számítja ki egy helyen.</span><span class="sxs-lookup"><span data-stu-id="b4daf-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="b4daf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b4daf-110">EXAMPLES</span></span>

### <span data-ttu-id="b4daf-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="b4daf-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="b4daf-112">Minden logikai hálózat beolvasása egy helyen.</span><span class="sxs-lookup"><span data-stu-id="b4daf-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="b4daf-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="b4daf-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="b4daf-114">Meghatározott logikai hálózatok beszerzése egy név alapján</span><span class="sxs-lookup"><span data-stu-id="b4daf-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="b4daf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4daf-115">PARAMETERS</span></span>

### <span data-ttu-id="b4daf-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4daf-116">-Name</span></span>
<span data-ttu-id="b4daf-117">A logikai hálózat neve.</span><span class="sxs-lookup"><span data-stu-id="b4daf-117">Name of the logical network.</span></span>

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

### <span data-ttu-id="b4daf-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="b4daf-118">-Location</span></span>
<span data-ttu-id="b4daf-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="b4daf-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b4daf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4daf-120">-ResourceGroupName</span></span>
<span data-ttu-id="b4daf-121">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="b4daf-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b4daf-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4daf-122">-ResourceId</span></span>
<span data-ttu-id="b4daf-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b4daf-123">The resource id.</span></span>

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

### <span data-ttu-id="b4daf-124">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="b4daf-124">-Filter</span></span>
<span data-ttu-id="b4daf-125">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="b4daf-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="b4daf-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="b4daf-126">-Skip</span></span>
<span data-ttu-id="b4daf-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="b4daf-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b4daf-128">-Top</span><span class="sxs-lookup"><span data-stu-id="b4daf-128">-Top</span></span>
<span data-ttu-id="b4daf-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="b4daf-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b4daf-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="b4daf-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b4daf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4daf-131">CommonParameters</span></span>
<span data-ttu-id="b4daf-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4daf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4daf-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4daf-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4daf-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4daf-134">INPUTS</span></span>

## <span data-ttu-id="b4daf-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4daf-135">OUTPUTS</span></span>

### <span data-ttu-id="b4daf-136">Microsoft. AzureStack. Management. Fabric. admin. models. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="b4daf-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="b4daf-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4daf-137">NOTES</span></span>

## <span data-ttu-id="b4daf-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4daf-138">RELATED LINKS</span></span>
