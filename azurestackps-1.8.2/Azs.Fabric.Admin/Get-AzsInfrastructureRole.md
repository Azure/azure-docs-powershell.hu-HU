---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a20f0fbc5b059e878f0062569ffba2c16794204
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016642"
---
# <span data-ttu-id="11485-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="11485-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="11485-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11485-102">SYNOPSIS</span></span>
<span data-ttu-id="11485-103">Az infrastruktúra-szerepkörök listáját számítja ki egy helyen.</span><span class="sxs-lookup"><span data-stu-id="11485-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="11485-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11485-104">SYNTAX</span></span>

### <span data-ttu-id="11485-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11485-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="11485-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="11485-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="11485-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="11485-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="11485-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="11485-108">DESCRIPTION</span></span>
<span data-ttu-id="11485-109">Az infrastruktúra-szerepkörök listáját számítja ki egy helyen.</span><span class="sxs-lookup"><span data-stu-id="11485-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="11485-110">Példák</span><span class="sxs-lookup"><span data-stu-id="11485-110">EXAMPLES</span></span>

### <span data-ttu-id="11485-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="11485-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="11485-112">A teljes infrastruktúra-szerepkörök listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="11485-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="11485-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="11485-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="11485-114">A név alapján Ismerje meg az infrastruktúra szerepkört.</span><span class="sxs-lookup"><span data-stu-id="11485-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="11485-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11485-115">PARAMETERS</span></span>

### <span data-ttu-id="11485-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="11485-116">-Name</span></span>
<span data-ttu-id="11485-117">Infrastruktúra-szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="11485-117">Infrastructure role name.</span></span>

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

### <span data-ttu-id="11485-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="11485-118">-Location</span></span>
<span data-ttu-id="11485-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="11485-119">Location of the resource.</span></span>

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

### <span data-ttu-id="11485-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11485-120">-ResourceGroupName</span></span>
<span data-ttu-id="11485-121">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="11485-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="11485-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11485-122">-ResourceId</span></span>
<span data-ttu-id="11485-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="11485-123">The resource id.</span></span>

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

### <span data-ttu-id="11485-124">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="11485-124">-Filter</span></span>
<span data-ttu-id="11485-125">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="11485-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="11485-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="11485-126">-Skip</span></span>
<span data-ttu-id="11485-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="11485-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="11485-128">-Top</span><span class="sxs-lookup"><span data-stu-id="11485-128">-Top</span></span>
<span data-ttu-id="11485-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="11485-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="11485-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="11485-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="11485-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11485-131">CommonParameters</span></span>
<span data-ttu-id="11485-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11485-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11485-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11485-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11485-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11485-134">INPUTS</span></span>

## <span data-ttu-id="11485-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11485-135">OUTPUTS</span></span>

### <span data-ttu-id="11485-136">Microsoft. AzureStack. Management. Fabric. admin. models. InfraRole</span><span class="sxs-lookup"><span data-stu-id="11485-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="11485-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11485-137">NOTES</span></span>

## <span data-ttu-id="11485-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11485-138">RELATED LINKS</span></span>
