---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcd5d112fea0ec68e372a5ad282b3d661f9481ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671684"
---
# <span data-ttu-id="2bdcc-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="2bdcc-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="2bdcc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2bdcc-102">SYNOPSIS</span></span>
<span data-ttu-id="2bdcc-103">A kelme minden helyének listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2bdcc-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="2bdcc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2bdcc-104">SYNTAX</span></span>

### <span data-ttu-id="2bdcc-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2bdcc-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="2bdcc-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="2bdcc-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2bdcc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bdcc-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2bdcc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2bdcc-108">DESCRIPTION</span></span>
<span data-ttu-id="2bdcc-109">A kelme minden helyének listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2bdcc-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="2bdcc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2bdcc-110">EXAMPLES</span></span>

### <span data-ttu-id="2bdcc-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2bdcc-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="2bdcc-112">A teljes anyagból álló helyek listájának visszaadása.</span><span class="sxs-lookup"><span data-stu-id="2bdcc-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="2bdcc-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2bdcc-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="2bdcc-114">A név alapján adja vissza a helyet.</span><span class="sxs-lookup"><span data-stu-id="2bdcc-114">Return a location based on the name.</span></span>

## <span data-ttu-id="2bdcc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2bdcc-115">PARAMETERS</span></span>

### <span data-ttu-id="2bdcc-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="2bdcc-116">-Filter</span></span>
<span data-ttu-id="2bdcc-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="2bdcc-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="2bdcc-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="2bdcc-118">-Location</span></span>
<span data-ttu-id="2bdcc-119">A szövet helye.</span><span class="sxs-lookup"><span data-stu-id="2bdcc-119">Fabric location.</span></span>

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

### <span data-ttu-id="2bdcc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bdcc-120">-ResourceGroupName</span></span>
<span data-ttu-id="2bdcc-121">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="2bdcc-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="2bdcc-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bdcc-122">-ResourceId</span></span>
<span data-ttu-id="2bdcc-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2bdcc-123">The resource id.</span></span>

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

### <span data-ttu-id="2bdcc-124">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="2bdcc-124">-Skip</span></span>
<span data-ttu-id="2bdcc-125">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="2bdcc-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2bdcc-126">-Top</span><span class="sxs-lookup"><span data-stu-id="2bdcc-126">-Top</span></span>
<span data-ttu-id="2bdcc-127">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="2bdcc-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2bdcc-128">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="2bdcc-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2bdcc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bdcc-129">CommonParameters</span></span>
<span data-ttu-id="2bdcc-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2bdcc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bdcc-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bdcc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bdcc-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bdcc-132">INPUTS</span></span>

## <span data-ttu-id="2bdcc-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bdcc-133">OUTPUTS</span></span>

### <span data-ttu-id="2bdcc-134">Microsoft. AzureStack. Management. Fabric. admin. models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="2bdcc-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="2bdcc-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2bdcc-135">NOTES</span></span>

## <span data-ttu-id="2bdcc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2bdcc-136">RELATED LINKS</span></span>

