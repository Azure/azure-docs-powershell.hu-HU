---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1f1be36f51aab748ec790c56aea7092f1d3d877
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840220"
---
# <span data-ttu-id="c3b74-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="c3b74-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="c3b74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3b74-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b74-103">Átjáró-alkalmazáskészlet-objektumokat ad eredményül egy helyen.</span><span class="sxs-lookup"><span data-stu-id="c3b74-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="c3b74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3b74-104">SYNTAX</span></span>

### <span data-ttu-id="c3b74-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3b74-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c3b74-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c3b74-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c3b74-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3b74-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c3b74-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3b74-108">DESCRIPTION</span></span>
<span data-ttu-id="c3b74-109">Az Edge Gateway Pool objektumait visszaszámítja egy helyen.</span><span class="sxs-lookup"><span data-stu-id="c3b74-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="c3b74-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c3b74-110">EXAMPLES</span></span>

### <span data-ttu-id="c3b74-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="c3b74-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="c3b74-112">A teljes peremhálózat-átjárók listájának beolvasása</span><span class="sxs-lookup"><span data-stu-id="c3b74-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="c3b74-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="c3b74-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="c3b74-114">Egy adott Edge-átjárót tartalmazó alkalmazáskészlet beszerzése.</span><span class="sxs-lookup"><span data-stu-id="c3b74-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="c3b74-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3b74-115">PARAMETERS</span></span>

### <span data-ttu-id="c3b74-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c3b74-116">-Name</span></span>
<span data-ttu-id="c3b74-117">Az Edge átjáró-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="c3b74-117">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="c3b74-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="c3b74-118">-Location</span></span>
<span data-ttu-id="c3b74-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="c3b74-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c3b74-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3b74-120">-ResourceGroupName</span></span>
<span data-ttu-id="c3b74-121">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="c3b74-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c3b74-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3b74-122">-ResourceId</span></span>
<span data-ttu-id="c3b74-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c3b74-123">The resource id.</span></span>

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

### <span data-ttu-id="c3b74-124">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="c3b74-124">-Filter</span></span>
<span data-ttu-id="c3b74-125">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="c3b74-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="c3b74-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="c3b74-126">-Skip</span></span>
<span data-ttu-id="c3b74-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="c3b74-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c3b74-128">-Top</span><span class="sxs-lookup"><span data-stu-id="c3b74-128">-Top</span></span>
<span data-ttu-id="c3b74-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="c3b74-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c3b74-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="c3b74-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c3b74-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b74-131">CommonParameters</span></span>
<span data-ttu-id="c3b74-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3b74-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b74-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3b74-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b74-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3b74-134">INPUTS</span></span>

## <span data-ttu-id="c3b74-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3b74-135">OUTPUTS</span></span>

### <span data-ttu-id="c3b74-136">Microsoft. AzureStack. Management. Fabric. admin. models. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="c3b74-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="c3b74-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3b74-137">NOTES</span></span>

## <span data-ttu-id="c3b74-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3b74-138">RELATED LINKS</span></span>
