---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b50cd7f98fd9919ed816314d7cec1222e5c4970c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490959"
---
# <span data-ttu-id="45574-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="45574-101">New-AzsIpPool</span></span>

## <span data-ttu-id="45574-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45574-102">SYNOPSIS</span></span>
<span data-ttu-id="45574-103">Infrastruktúra-IP-készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="45574-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="45574-104">Miután létrehozta az IP-készletet, nem lehet törölni vagy módosítani.</span><span class="sxs-lookup"><span data-stu-id="45574-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="45574-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45574-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45574-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="45574-106">DESCRIPTION</span></span>
<span data-ttu-id="45574-107">Infrastruktúra-IP-készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="45574-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="45574-108">Példák</span><span class="sxs-lookup"><span data-stu-id="45574-108">EXAMPLES</span></span>

### <span data-ttu-id="45574-109">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="45574-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="45574-110">Új IP-készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="45574-110">Create a new IP pool.</span></span>

## <span data-ttu-id="45574-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45574-111">PARAMETERS</span></span>

### <span data-ttu-id="45574-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="45574-112">-AddressPrefix</span></span>
<span data-ttu-id="45574-113">A cím előtagja.</span><span class="sxs-lookup"><span data-stu-id="45574-113">The address prefix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45574-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45574-114">-AsJob</span></span>
<span data-ttu-id="45574-115">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="45574-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45574-116">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="45574-116">-EndIpAddress</span></span>
<span data-ttu-id="45574-117">A záró IP-cím.</span><span class="sxs-lookup"><span data-stu-id="45574-117">The ending IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45574-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="45574-118">-Location</span></span>
<span data-ttu-id="45574-119">Az a terület, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="45574-119">The region where the resource is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45574-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45574-120">-Name</span></span>
<span data-ttu-id="45574-121">Az IP-készlet neve</span><span class="sxs-lookup"><span data-stu-id="45574-121">IP pool name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45574-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45574-122">-ResourceGroupName</span></span>
<span data-ttu-id="45574-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="45574-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45574-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="45574-124">-StartIpAddress</span></span>
<span data-ttu-id="45574-125">A kezdő IP-cím.</span><span class="sxs-lookup"><span data-stu-id="45574-125">The starting IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45574-126">-Címkék</span><span class="sxs-lookup"><span data-stu-id="45574-126">-Tags</span></span>
<span data-ttu-id="45574-127">A kulcs-érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="45574-127">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45574-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45574-128">-Confirm</span></span>
<span data-ttu-id="45574-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45574-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45574-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45574-130">-WhatIf</span></span>
<span data-ttu-id="45574-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45574-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45574-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45574-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45574-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45574-133">CommonParameters</span></span>
<span data-ttu-id="45574-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45574-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45574-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45574-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45574-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45574-136">INPUTS</span></span>

## <span data-ttu-id="45574-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45574-137">OUTPUTS</span></span>

### <span data-ttu-id="45574-138">Microsoft. AzureStack. Management. Fabric. admin. models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="45574-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="45574-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45574-139">NOTES</span></span>

## <span data-ttu-id="45574-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45574-140">RELATED LINKS</span></span>

