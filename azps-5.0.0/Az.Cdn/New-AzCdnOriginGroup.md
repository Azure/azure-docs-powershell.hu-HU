---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186263"
---
# <span data-ttu-id="a3b78-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a3b78-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="a3b78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3b78-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b78-103">Új CDN-származási csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3b78-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="a3b78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3b78-104">SYNTAX</span></span>

### <span data-ttu-id="a3b78-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3b78-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3b78-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b78-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3b78-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3b78-107">DESCRIPTION</span></span>
<span data-ttu-id="a3b78-108">A New-AzCdnOriginGroup új Origó csoportot hoz létre a megadott végponton belül.</span><span class="sxs-lookup"><span data-stu-id="a3b78-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="a3b78-109">Ha a végpont első származási csoportja, akkor a DefaultOriginGroup tulajdonságot is be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="a3b78-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="a3b78-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a3b78-110">EXAMPLES</span></span>

### <span data-ttu-id="a3b78-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a3b78-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="a3b78-112">Ez a parancsmag egy új származási csoportot hoz létre a megadott végponton belül.</span><span class="sxs-lookup"><span data-stu-id="a3b78-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="a3b78-113">A megadott Origin-azonosítókat a származási készlet szerint fogja használni.</span><span class="sxs-lookup"><span data-stu-id="a3b78-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="a3b78-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3b78-114">PARAMETERS</span></span>

### <span data-ttu-id="a3b78-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a3b78-115">-CdnOriginGroup</span></span>
<span data-ttu-id="a3b78-116">A CDN származási csoport objektuma.</span><span class="sxs-lookup"><span data-stu-id="a3b78-116">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b78-117">-DefaultProfile</span></span>
<span data-ttu-id="a3b78-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3b78-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a3b78-119">-EndpointName</span></span>
<span data-ttu-id="a3b78-120">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="a3b78-120">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b78-121">-OriginGroupName</span></span>
<span data-ttu-id="a3b78-122">Azure CDN származási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a3b78-122">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="a3b78-123">-OriginId</span></span>
<span data-ttu-id="a3b78-124">Azure CDN Origin Group azonosítók.</span><span class="sxs-lookup"><span data-stu-id="a3b78-124">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a3b78-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="a3b78-126">Az egészségügyi Szondák közötti másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="a3b78-126">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="a3b78-127">-ProbePath</span></span>
<span data-ttu-id="a3b78-128">A származási állapot meghatározásához használt kezdőponthoz viszonyított útvonal.</span><span class="sxs-lookup"><span data-stu-id="a3b78-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="a3b78-129">-ProbeProtocol</span></span>
<span data-ttu-id="a3b78-130">Az egészségi szondához használandó protokoll.</span><span class="sxs-lookup"><span data-stu-id="a3b78-130">Protocol to use for health probe.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="a3b78-131">-ProbeRequestType</span></span>
<span data-ttu-id="a3b78-132">Az elvégzett állapottanúsítvány-kérés típusa.</span><span class="sxs-lookup"><span data-stu-id="a3b78-132">The type of health probe request that is made.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-133">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="a3b78-133">-ProfileName</span></span>
<span data-ttu-id="a3b78-134">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="a3b78-134">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b78-135">-ResourceGroupName</span></span>
<span data-ttu-id="a3b78-136">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="a3b78-136">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a3b78-137">-Confirm</span></span>
<span data-ttu-id="a3b78-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3b78-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3b78-139">-WhatIf</span></span>
<span data-ttu-id="a3b78-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a3b78-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3b78-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3b78-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b78-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b78-142">CommonParameters</span></span>
<span data-ttu-id="a3b78-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3b78-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b78-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a3b78-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b78-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3b78-145">INPUTS</span></span>

### <span data-ttu-id="a3b78-146">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="a3b78-146">System.Object</span></span>

## <span data-ttu-id="a3b78-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3b78-147">OUTPUTS</span></span>

### <span data-ttu-id="a3b78-148">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="a3b78-148">System.Object</span></span>

## <span data-ttu-id="a3b78-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3b78-149">NOTES</span></span>

## <span data-ttu-id="a3b78-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3b78-150">RELATED LINKS</span></span>
