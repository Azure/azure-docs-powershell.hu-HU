---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc074d17ea73bf54f623ea3e8ec72567ef2bcffe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840558"
---
# <span data-ttu-id="bd06d-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="bd06d-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="bd06d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd06d-102">SYNOPSIS</span></span>
<span data-ttu-id="bd06d-103">A kelme minden helyének listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="bd06d-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="bd06d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd06d-104">SYNTAX</span></span>

### <span data-ttu-id="bd06d-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd06d-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd06d-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="bd06d-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bd06d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd06d-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bd06d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd06d-108">DESCRIPTION</span></span>
<span data-ttu-id="bd06d-109">A kelme minden helyének listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="bd06d-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="bd06d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bd06d-110">EXAMPLES</span></span>

### <span data-ttu-id="bd06d-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="bd06d-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="bd06d-112">A teljes anyagból álló helyek listájának visszaadása.</span><span class="sxs-lookup"><span data-stu-id="bd06d-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="bd06d-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="bd06d-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="bd06d-114">A név alapján adja vissza a helyet.</span><span class="sxs-lookup"><span data-stu-id="bd06d-114">Return a location based on the name.</span></span>

## <span data-ttu-id="bd06d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd06d-115">PARAMETERS</span></span>

### <span data-ttu-id="bd06d-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="bd06d-116">-Location</span></span>
<span data-ttu-id="bd06d-117">A szövet helye.</span><span class="sxs-lookup"><span data-stu-id="bd06d-117">Fabric location.</span></span>

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

### <span data-ttu-id="bd06d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd06d-118">-ResourceGroupName</span></span>
<span data-ttu-id="bd06d-119">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="bd06d-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="bd06d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd06d-120">-ResourceId</span></span>
<span data-ttu-id="bd06d-121">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="bd06d-121">The resource id.</span></span>

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

### <span data-ttu-id="bd06d-122">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="bd06d-122">-Filter</span></span>
<span data-ttu-id="bd06d-123">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="bd06d-123">OData filter parameter.</span></span>

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

### <span data-ttu-id="bd06d-124">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="bd06d-124">-Skip</span></span>
<span data-ttu-id="bd06d-125">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="bd06d-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="bd06d-126">-Top</span><span class="sxs-lookup"><span data-stu-id="bd06d-126">-Top</span></span>
<span data-ttu-id="bd06d-127">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="bd06d-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bd06d-128">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="bd06d-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="bd06d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd06d-129">CommonParameters</span></span>
<span data-ttu-id="bd06d-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd06d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd06d-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd06d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd06d-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd06d-132">INPUTS</span></span>

## <span data-ttu-id="bd06d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd06d-133">OUTPUTS</span></span>

### <span data-ttu-id="bd06d-134">Microsoft. AzureStack. Management. Fabric. admin. models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="bd06d-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="bd06d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd06d-135">NOTES</span></span>

## <span data-ttu-id="bd06d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd06d-136">RELATED LINKS</span></span>
