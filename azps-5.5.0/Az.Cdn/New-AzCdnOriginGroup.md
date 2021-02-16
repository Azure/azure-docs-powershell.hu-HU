---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168050"
---
# <span data-ttu-id="0bee1-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="0bee1-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="0bee1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bee1-102">SYNOPSIS</span></span>
<span data-ttu-id="0bee1-103">Új CDN-forráscsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="0bee1-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="0bee1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0bee1-104">SYNTAX</span></span>

### <span data-ttu-id="0bee1-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0bee1-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bee1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bee1-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bee1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0bee1-107">DESCRIPTION</span></span>
<span data-ttu-id="0bee1-108">A New-AzCdnOriginGroup létrehoz egy új origincsoportot a megadott végponton belül.</span><span class="sxs-lookup"><span data-stu-id="0bee1-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="0bee1-109">Ha ez a végpont első origincsoportja, akkor a DefaultOriginGroup tulajdonságot is be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="0bee1-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="0bee1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0bee1-110">EXAMPLES</span></span>

### <span data-ttu-id="0bee1-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="0bee1-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="0bee1-112">Ez a parancsmag egy új origincsoportot hoz létre a megadott végponton belül.</span><span class="sxs-lookup"><span data-stu-id="0bee1-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="0bee1-113">A forráshalmaz a megadott originazonosítókat fogja használni.</span><span class="sxs-lookup"><span data-stu-id="0bee1-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="0bee1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bee1-114">PARAMETERS</span></span>

### <span data-ttu-id="0bee1-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="0bee1-115">-CdnOriginGroup</span></span>
<span data-ttu-id="0bee1-116">A CDN-forráscsoport objektuma.</span><span class="sxs-lookup"><span data-stu-id="0bee1-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="0bee1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bee1-117">-DefaultProfile</span></span>
<span data-ttu-id="0bee1-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0bee1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bee1-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0bee1-119">-EndpointName</span></span>
<span data-ttu-id="0bee1-120">Azure CDN-végpont neve.</span><span class="sxs-lookup"><span data-stu-id="0bee1-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="0bee1-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="0bee1-121">-OriginGroupName</span></span>
<span data-ttu-id="0bee1-122">Azure CDN-forráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0bee1-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="0bee1-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="0bee1-123">-OriginId</span></span>
<span data-ttu-id="0bee1-124">Azure CDN-forráscsoport-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="0bee1-124">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="0bee1-125">-Az ÉtiIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0bee1-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="0bee1-126">Az állapotok közti másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="0bee1-126">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="0bee1-127">-PathPath</span><span class="sxs-lookup"><span data-stu-id="0bee1-127">-ProbePath</span></span>
<span data-ttu-id="0bee1-128">A forrás állapotának meghatározásához használt forráshoz viszonyított elérési út.</span><span class="sxs-lookup"><span data-stu-id="0bee1-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="0bee1-129">-Az 10000000000000</span><span class="sxs-lookup"><span data-stu-id="0bee1-129">-ProbeProtocol</span></span>
<span data-ttu-id="0bee1-130">Protokoll egészségügyi problémákhoz.</span><span class="sxs-lookup"><span data-stu-id="0bee1-130">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="0bee1-131">-HcRequestType</span><span class="sxs-lookup"><span data-stu-id="0bee1-131">-ProbeRequestType</span></span>
<span data-ttu-id="0bee1-132">Az állapotkérés típusa.</span><span class="sxs-lookup"><span data-stu-id="0bee1-132">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="0bee1-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0bee1-133">-ProfileName</span></span>
<span data-ttu-id="0bee1-134">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="0bee1-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="0bee1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bee1-135">-ResourceGroupName</span></span>
<span data-ttu-id="0bee1-136">Az Azure CDN-profil erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="0bee1-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="0bee1-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0bee1-137">-Confirm</span></span>
<span data-ttu-id="0bee1-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0bee1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bee1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bee1-139">-WhatIf</span></span>
<span data-ttu-id="0bee1-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0bee1-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bee1-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0bee1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bee1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bee1-142">CommonParameters</span></span>
<span data-ttu-id="0bee1-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bee1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bee1-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bee1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bee1-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0bee1-145">INPUTS</span></span>

### <span data-ttu-id="0bee1-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="0bee1-146">System.Object</span></span>

## <span data-ttu-id="0bee1-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bee1-147">OUTPUTS</span></span>

### <span data-ttu-id="0bee1-148">System.Object</span><span class="sxs-lookup"><span data-stu-id="0bee1-148">System.Object</span></span>

## <span data-ttu-id="0bee1-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0bee1-149">NOTES</span></span>

## <span data-ttu-id="0bee1-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bee1-150">RELATED LINKS</span></span>
