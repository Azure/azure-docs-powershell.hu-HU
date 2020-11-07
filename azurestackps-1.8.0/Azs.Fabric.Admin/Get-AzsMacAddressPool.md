---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e22024b1b246a60104db0832860ed0aff699ff5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840202"
---
# <span data-ttu-id="5291f-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="5291f-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="5291f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5291f-102">SYNOPSIS</span></span>
<span data-ttu-id="5291f-103">Az összes MAC-címkészlet listáját jeleníti meg egy helyen.</span><span class="sxs-lookup"><span data-stu-id="5291f-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="5291f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5291f-104">SYNTAX</span></span>

### <span data-ttu-id="5291f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5291f-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5291f-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="5291f-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5291f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5291f-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5291f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5291f-108">DESCRIPTION</span></span>
<span data-ttu-id="5291f-109">Az összes MAC-címkészlet listáját jeleníti meg egy helyen.</span><span class="sxs-lookup"><span data-stu-id="5291f-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="5291f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5291f-110">EXAMPLES</span></span>

### <span data-ttu-id="5291f-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="5291f-111">EXAMPLE 1</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="5291f-112">Letölthet minden MAC-címkészletet a helyről.</span><span class="sxs-lookup"><span data-stu-id="5291f-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="5291f-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="5291f-113">EXAMPLE 2</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="5291f-114">A megfelelő MAC-címkészlet beszerzése a név alapján meghatározott helyre</span><span class="sxs-lookup"><span data-stu-id="5291f-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="5291f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5291f-115">PARAMETERS</span></span>

### <span data-ttu-id="5291f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5291f-116">-Name</span></span>
<span data-ttu-id="5291f-117">A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="5291f-117">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="5291f-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="5291f-118">-Location</span></span>
<span data-ttu-id="5291f-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="5291f-119">Location of the resource.</span></span>

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

### <span data-ttu-id="5291f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5291f-120">-ResourceGroupName</span></span>
<span data-ttu-id="5291f-121">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="5291f-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5291f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5291f-122">-ResourceId</span></span>
<span data-ttu-id="5291f-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5291f-123">The resource id.</span></span>

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

### <span data-ttu-id="5291f-124">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="5291f-124">-Filter</span></span>
<span data-ttu-id="5291f-125">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="5291f-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="5291f-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="5291f-126">-Skip</span></span>
<span data-ttu-id="5291f-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="5291f-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5291f-128">-Top</span><span class="sxs-lookup"><span data-stu-id="5291f-128">-Top</span></span>
<span data-ttu-id="5291f-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="5291f-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5291f-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="5291f-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5291f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5291f-131">CommonParameters</span></span>
<span data-ttu-id="5291f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5291f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5291f-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5291f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5291f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5291f-134">INPUTS</span></span>

## <span data-ttu-id="5291f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5291f-135">OUTPUTS</span></span>

### <span data-ttu-id="5291f-136">Microsoft. AzureStack. Management. Fabric. admin. models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="5291f-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="5291f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5291f-137">NOTES</span></span>

## <span data-ttu-id="5291f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5291f-138">RELATED LINKS</span></span>
