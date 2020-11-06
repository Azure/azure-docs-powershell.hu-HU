---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67a49abc82ba1ec8d9411141d456b8f71f75600f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490704"
---
# <span data-ttu-id="e1d43-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="e1d43-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="e1d43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1d43-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d43-103">Átjáró-alkalmazáskészlet-objektumokat ad eredményül egy helyen.</span><span class="sxs-lookup"><span data-stu-id="e1d43-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="e1d43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1d43-104">SYNTAX</span></span>

### <span data-ttu-id="e1d43-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1d43-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e1d43-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e1d43-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e1d43-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1d43-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e1d43-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1d43-108">DESCRIPTION</span></span>
<span data-ttu-id="e1d43-109">Az Edge Gateway Pool objektumait visszaszámítja egy helyen.</span><span class="sxs-lookup"><span data-stu-id="e1d43-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="e1d43-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e1d43-110">EXAMPLES</span></span>

### <span data-ttu-id="e1d43-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e1d43-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="e1d43-112">A teljes peremhálózat-átjárók listájának beolvasása</span><span class="sxs-lookup"><span data-stu-id="e1d43-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="e1d43-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e1d43-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="e1d43-114">Egy adott Edge-átjárót tartalmazó alkalmazáskészlet beszerzése.</span><span class="sxs-lookup"><span data-stu-id="e1d43-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="e1d43-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1d43-115">PARAMETERS</span></span>

### <span data-ttu-id="e1d43-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="e1d43-116">-Filter</span></span>
<span data-ttu-id="e1d43-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="e1d43-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e1d43-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="e1d43-118">-Location</span></span>
<span data-ttu-id="e1d43-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="e1d43-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e1d43-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e1d43-120">-Name</span></span>
<span data-ttu-id="e1d43-121">Az Edge átjáró-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="e1d43-121">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="e1d43-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d43-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1d43-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="e1d43-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e1d43-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1d43-124">-ResourceId</span></span>
<span data-ttu-id="e1d43-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e1d43-125">The resource id.</span></span>

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

### <span data-ttu-id="e1d43-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="e1d43-126">-Skip</span></span>
<span data-ttu-id="e1d43-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="e1d43-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e1d43-128">-Top</span><span class="sxs-lookup"><span data-stu-id="e1d43-128">-Top</span></span>
<span data-ttu-id="e1d43-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="e1d43-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e1d43-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="e1d43-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e1d43-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d43-131">CommonParameters</span></span>
<span data-ttu-id="e1d43-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1d43-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d43-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d43-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d43-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1d43-134">INPUTS</span></span>

## <span data-ttu-id="e1d43-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1d43-135">OUTPUTS</span></span>

### <span data-ttu-id="e1d43-136">Microsoft. AzureStack. Management. Fabric. admin. models. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="e1d43-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="e1d43-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1d43-137">NOTES</span></span>

## <span data-ttu-id="e1d43-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1d43-138">RELATED LINKS</span></span>

