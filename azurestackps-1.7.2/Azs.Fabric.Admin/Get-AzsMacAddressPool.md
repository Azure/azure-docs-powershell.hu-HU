---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5c686faa457d83ab0ddffb932b20ab5fcd168ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839854"
---
# <span data-ttu-id="c1fa0-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1fa0-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="c1fa0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="c1fa0-103">Az összes MAC-címkészlet listáját jeleníti meg egy helyen.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="c1fa0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1fa0-104">SYNTAX</span></span>

### <span data-ttu-id="c1fa0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1fa0-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c1fa0-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c1fa0-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c1fa0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1fa0-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c1fa0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1fa0-108">DESCRIPTION</span></span>
<span data-ttu-id="c1fa0-109">Az összes MAC-címkészlet listáját jeleníti meg egy helyen.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="c1fa0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c1fa0-110">EXAMPLES</span></span>

### <span data-ttu-id="c1fa0-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c1fa0-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="c1fa0-112">Letölthet minden MAC-címkészletet a helyről.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="c1fa0-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c1fa0-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="c1fa0-114">A megfelelő MAC-címkészlet beszerzése a név alapján meghatározott helyre</span><span class="sxs-lookup"><span data-stu-id="c1fa0-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="c1fa0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1fa0-115">PARAMETERS</span></span>

### <span data-ttu-id="c1fa0-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="c1fa0-116">-Filter</span></span>
<span data-ttu-id="c1fa0-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="c1fa0-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="c1fa0-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="c1fa0-118">-Location</span></span>
<span data-ttu-id="c1fa0-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c1fa0-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1fa0-120">-Name</span></span>
<span data-ttu-id="c1fa0-121">A MAC-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-121">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="c1fa0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1fa0-122">-ResourceGroupName</span></span>
<span data-ttu-id="c1fa0-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c1fa0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1fa0-124">-ResourceId</span></span>
<span data-ttu-id="c1fa0-125">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-125">The resource id.</span></span>

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

### <span data-ttu-id="c1fa0-126">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="c1fa0-126">-Skip</span></span>
<span data-ttu-id="c1fa0-127">Az első N elem kihagyása a paraméterben megadott értékkel.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c1fa0-128">-Top</span><span class="sxs-lookup"><span data-stu-id="c1fa0-128">-Top</span></span>
<span data-ttu-id="c1fa0-129">A paraméterben megadott módon adja vissza a legfelső N-elemeket.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c1fa0-130">A-kihagyás paraméter után érvényes.</span><span class="sxs-lookup"><span data-stu-id="c1fa0-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c1fa0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1fa0-131">CommonParameters</span></span>
<span data-ttu-id="c1fa0-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1fa0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1fa0-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1fa0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1fa0-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1fa0-134">INPUTS</span></span>

## <span data-ttu-id="c1fa0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1fa0-135">OUTPUTS</span></span>

### <span data-ttu-id="c1fa0-136">Microsoft. AzureStack. Management. Fabric. admin. models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1fa0-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="c1fa0-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1fa0-137">NOTES</span></span>

## <span data-ttu-id="c1fa0-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1fa0-138">RELATED LINKS</span></span>

