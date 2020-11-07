---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd353b28b095178e83f488f3fd05a54146610b01
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840527"
---
# <span data-ttu-id="fd88a-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="fd88a-101">New-AzsIpPool</span></span>

## <span data-ttu-id="fd88a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd88a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd88a-103">Infrastruktúra-IP-készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="fd88a-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="fd88a-104">Miután létrehozta az IP-készletet, nem lehet törölni vagy módosítani.</span><span class="sxs-lookup"><span data-stu-id="fd88a-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="fd88a-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd88a-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd88a-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd88a-106">DESCRIPTION</span></span>
<span data-ttu-id="fd88a-107">Infrastruktúra-IP-készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="fd88a-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="fd88a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fd88a-108">EXAMPLES</span></span>

### <span data-ttu-id="fd88a-109">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="fd88a-109">EXAMPLE 1</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="fd88a-110">Új IP-készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="fd88a-110">Create a new IP pool.</span></span>

## <span data-ttu-id="fd88a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd88a-111">PARAMETERS</span></span>

### <span data-ttu-id="fd88a-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd88a-112">-Name</span></span>
<span data-ttu-id="fd88a-113">Az IP-készlet neve</span><span class="sxs-lookup"><span data-stu-id="fd88a-113">IP pool name.</span></span>

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

### <span data-ttu-id="fd88a-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fd88a-114">-AddressPrefix</span></span>
<span data-ttu-id="fd88a-115">A cím előtagja.</span><span class="sxs-lookup"><span data-stu-id="fd88a-115">The address prefix.</span></span>

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

### <span data-ttu-id="fd88a-116">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="fd88a-116">-StartIpAddress</span></span>
<span data-ttu-id="fd88a-117">A kezdő IP-cím.</span><span class="sxs-lookup"><span data-stu-id="fd88a-117">The starting IP address.</span></span>

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

### <span data-ttu-id="fd88a-118">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="fd88a-118">-EndIpAddress</span></span>
<span data-ttu-id="fd88a-119">A záró IP-cím.</span><span class="sxs-lookup"><span data-stu-id="fd88a-119">The ending IP address.</span></span>

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

### <span data-ttu-id="fd88a-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="fd88a-120">-Location</span></span>
<span data-ttu-id="fd88a-121">Az a terület, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="fd88a-121">The region where the resource is located.</span></span>

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

### <span data-ttu-id="fd88a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd88a-122">-ResourceGroupName</span></span>
<span data-ttu-id="fd88a-123">Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.</span><span class="sxs-lookup"><span data-stu-id="fd88a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="fd88a-124">-Címkék</span><span class="sxs-lookup"><span data-stu-id="fd88a-124">-Tags</span></span>
<span data-ttu-id="fd88a-125">A kulcs-érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="fd88a-125">List of key-value pairs.</span></span>

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

### <span data-ttu-id="fd88a-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd88a-126">-AsJob</span></span>
<span data-ttu-id="fd88a-127">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="fd88a-127">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="fd88a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd88a-128">-WhatIf</span></span>
<span data-ttu-id="fd88a-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd88a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd88a-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd88a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd88a-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd88a-131">-Confirm</span></span>
<span data-ttu-id="fd88a-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd88a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd88a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd88a-133">CommonParameters</span></span>
<span data-ttu-id="fd88a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd88a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd88a-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd88a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd88a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd88a-136">INPUTS</span></span>

## <span data-ttu-id="fd88a-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd88a-137">OUTPUTS</span></span>

### <span data-ttu-id="fd88a-138">Microsoft. AzureStack. Management. Fabric. admin. models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="fd88a-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="fd88a-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd88a-139">NOTES</span></span>

## <span data-ttu-id="fd88a-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd88a-140">RELATED LINKS</span></span>
