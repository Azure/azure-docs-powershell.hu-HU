---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42d6233a99979687b7031ab58a620319fa675a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839690"
---
# <span data-ttu-id="011cd-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="011cd-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="011cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="011cd-102">SYNOPSIS</span></span>
<span data-ttu-id="011cd-103">Az összes szoftveres terheléselosztó példány listáját jeleníti meg egy helyen.</span><span class="sxs-lookup"><span data-stu-id="011cd-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="011cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="011cd-104">SYNTAX</span></span>

### <span data-ttu-id="011cd-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="011cd-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="011cd-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="011cd-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="011cd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="011cd-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="011cd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="011cd-108">DESCRIPTION</span></span>
<span data-ttu-id="011cd-109">Az összes szoftveres terheléselosztó példány listáját jeleníti meg egy helyen.</span><span class="sxs-lookup"><span data-stu-id="011cd-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="011cd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="011cd-110">EXAMPLES</span></span>

### <span data-ttu-id="011cd-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="011cd-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="011cd-112">Az összes szoftveres terheléselosztó multiplexer-példány beszerzése egy helyen.</span><span class="sxs-lookup"><span data-stu-id="011cd-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="011cd-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="011cd-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="011cd-114">A szoftver egy adott helyről kapott egy olyan, a szoftverhez tartozó terheléselosztó multiplexer-példányát, amely nevet kap.</span><span class="sxs-lookup"><span data-stu-id="011cd-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="011cd-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="011cd-115">PARAMETERS</span></span>

### <span data-ttu-id="011cd-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="011cd-116">-Filter</span></span>
<span data-ttu-id="011cd-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="011cd-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="011cd-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="011cd-118">-Location</span></span>
<span data-ttu-id="011cd-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="011cd-119">Location of the resource.</span></span>

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

### <span data-ttu-id="011cd-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="011cd-120">-Name</span></span>
<span data-ttu-id="011cd-121">A SLB MUX példányának neve.</span><span class="sxs-lookup"><span data-stu-id="011cd-121">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="011cd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="011cd-122">-ResourceGroupName</span></span>
<span data-ttu-id="011cd-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="011cd-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="011cd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="011cd-124">-ResourceId</span></span>
<span data-ttu-id="011cd-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="011cd-125">The resource id.</span></span>

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

### <span data-ttu-id="011cd-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="011cd-126">-Skip</span></span>
<span data-ttu-id="011cd-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="011cd-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="011cd-128">-Top</span><span class="sxs-lookup"><span data-stu-id="011cd-128">-Top</span></span>
<span data-ttu-id="011cd-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="011cd-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="011cd-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="011cd-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="011cd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011cd-131">CommonParameters</span></span>
<span data-ttu-id="011cd-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="011cd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="011cd-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="011cd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011cd-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="011cd-134">INPUTS</span></span>

## <span data-ttu-id="011cd-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="011cd-135">OUTPUTS</span></span>

### <span data-ttu-id="011cd-136">Microsoft. AzureStack. Management. Fabric. admin. models. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="011cd-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="011cd-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="011cd-137">NOTES</span></span>

## <span data-ttu-id="011cd-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="011cd-138">RELATED LINKS</span></span>

