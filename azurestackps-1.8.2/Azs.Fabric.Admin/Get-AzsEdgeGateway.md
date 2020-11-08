---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 793bf4a4b5b9dfb448c5b2a1baf9d74af592a23e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016647"
---
# <span data-ttu-id="545e9-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="545e9-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="545e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="545e9-102">SYNOPSIS</span></span>
<span data-ttu-id="545e9-103">Egy adott helyen található összes peremhálózat-átjáró listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="545e9-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="545e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="545e9-104">SYNTAX</span></span>

### <span data-ttu-id="545e9-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="545e9-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="545e9-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="545e9-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="545e9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="545e9-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="545e9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="545e9-108">DESCRIPTION</span></span>
<span data-ttu-id="545e9-109">Egy adott helyen található összes peremhálózat-átjáró listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="545e9-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="545e9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="545e9-110">EXAMPLES</span></span>

### <span data-ttu-id="545e9-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="545e9-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="545e9-112">Az összes Edge-átjáró listájának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="545e9-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="545e9-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="545e9-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="545e9-114">Adott peremhálózat-átjáró beszerzése.</span><span class="sxs-lookup"><span data-stu-id="545e9-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="545e9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="545e9-115">PARAMETERS</span></span>

### <span data-ttu-id="545e9-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="545e9-116">-Name</span></span>
<span data-ttu-id="545e9-117">Az Edge átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="545e9-117">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="545e9-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="545e9-118">-Location</span></span>
<span data-ttu-id="545e9-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="545e9-119">Location of the resource.</span></span>

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

### <span data-ttu-id="545e9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="545e9-120">-ResourceGroupName</span></span>
<span data-ttu-id="545e9-121">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="545e9-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="545e9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="545e9-122">-ResourceId</span></span>
<span data-ttu-id="545e9-123">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="545e9-123">The resource id.</span></span>

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

### <span data-ttu-id="545e9-124">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="545e9-124">-Filter</span></span>
<span data-ttu-id="545e9-125">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="545e9-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="545e9-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="545e9-126">-Skip</span></span>
<span data-ttu-id="545e9-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="545e9-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="545e9-128">-Top</span><span class="sxs-lookup"><span data-stu-id="545e9-128">-Top</span></span>
<span data-ttu-id="545e9-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="545e9-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="545e9-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="545e9-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="545e9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545e9-131">CommonParameters</span></span>
<span data-ttu-id="545e9-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="545e9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545e9-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="545e9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545e9-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="545e9-134">INPUTS</span></span>

## <span data-ttu-id="545e9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="545e9-135">OUTPUTS</span></span>

### <span data-ttu-id="545e9-136">Microsoft. AzureStack. Management. Fabric. admin. models. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="545e9-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="545e9-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="545e9-137">NOTES</span></span>

## <span data-ttu-id="545e9-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="545e9-138">RELATED LINKS</span></span>
