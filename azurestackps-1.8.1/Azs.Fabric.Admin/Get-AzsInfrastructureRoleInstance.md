---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c5fe6e28ff87cfd3f365441d0e09f09ef21dc454
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840551"
---
# <span data-ttu-id="81bf7-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="81bf7-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="81bf7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81bf7-102">SYNOPSIS</span></span>
<span data-ttu-id="81bf7-103">A helyhez tartozó összes infrastruktúra-szerepkör-példány listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="81bf7-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="81bf7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81bf7-104">SYNTAX</span></span>

### <span data-ttu-id="81bf7-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81bf7-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="81bf7-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="81bf7-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="81bf7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="81bf7-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="81bf7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="81bf7-108">DESCRIPTION</span></span>
<span data-ttu-id="81bf7-109">A helyhez tartozó összes infrastruktúra-szerepkör-példány listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="81bf7-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="81bf7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="81bf7-110">EXAMPLES</span></span>

### <span data-ttu-id="81bf7-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="81bf7-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="81bf7-112">Visszaadja az összes infrastruktúra-szerepkör-példány listáját.</span><span class="sxs-lookup"><span data-stu-id="81bf7-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="81bf7-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="81bf7-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="81bf7-114">A név alapján egyetlen infrastrukturális szerepkört ad vissza.</span><span class="sxs-lookup"><span data-stu-id="81bf7-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="81bf7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81bf7-115">PARAMETERS</span></span>

### <span data-ttu-id="81bf7-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81bf7-116">-Name</span></span>
<span data-ttu-id="81bf7-117">Egy infrastruktúra-szerepkör példányának neve.</span><span class="sxs-lookup"><span data-stu-id="81bf7-117">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="81bf7-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="81bf7-118">-Location</span></span>
<span data-ttu-id="81bf7-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="81bf7-119">Location of the resource.</span></span>

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

### <span data-ttu-id="81bf7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81bf7-120">-ResourceGroupName</span></span>
<span data-ttu-id="81bf7-121">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="81bf7-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="81bf7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81bf7-122">-ResourceId</span></span>
<span data-ttu-id="81bf7-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="81bf7-123">The resource id.</span></span>

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

### <span data-ttu-id="81bf7-124">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="81bf7-124">-Filter</span></span>
<span data-ttu-id="81bf7-125">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="81bf7-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="81bf7-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="81bf7-126">-Skip</span></span>
<span data-ttu-id="81bf7-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="81bf7-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="81bf7-128">-Top</span><span class="sxs-lookup"><span data-stu-id="81bf7-128">-Top</span></span>
<span data-ttu-id="81bf7-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="81bf7-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="81bf7-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="81bf7-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="81bf7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bf7-131">CommonParameters</span></span>
<span data-ttu-id="81bf7-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81bf7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bf7-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81bf7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bf7-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81bf7-134">INPUTS</span></span>

## <span data-ttu-id="81bf7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81bf7-135">OUTPUTS</span></span>

### <span data-ttu-id="81bf7-136">Microsoft. AzureStack. Management. Fabric. admin. models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="81bf7-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="81bf7-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81bf7-137">NOTES</span></span>

## <span data-ttu-id="81bf7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81bf7-138">RELATED LINKS</span></span>
