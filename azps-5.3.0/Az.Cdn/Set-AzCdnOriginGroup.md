---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480931"
---
# <span data-ttu-id="4e44a-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="4e44a-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="4e44a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e44a-102">SYNOPSIS</span></span>
<span data-ttu-id="4e44a-103">A CDN-forráscsoport frissítése</span><span class="sxs-lookup"><span data-stu-id="4e44a-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="4e44a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4e44a-104">SYNTAX</span></span>

### <span data-ttu-id="4e44a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e44a-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e44a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e44a-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e44a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4e44a-107">DESCRIPTION</span></span>
<span data-ttu-id="4e44a-108">Set-AzCdnOriginGroup frissíti a megadott origincsoportot a megadott végponton belül.</span><span class="sxs-lookup"><span data-stu-id="4e44a-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="4e44a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4e44a-109">EXAMPLES</span></span>

### <span data-ttu-id="4e44a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="4e44a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="4e44a-111">Ezzel a parancsmagtal frissítheti az Origin csoportBan található ABerevalInSeconds tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="4e44a-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="4e44a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e44a-112">PARAMETERS</span></span>

### <span data-ttu-id="4e44a-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="4e44a-113">-CdnOriginGroup</span></span>
<span data-ttu-id="4e44a-114">A CDN-forráscsoport objektuma.</span><span class="sxs-lookup"><span data-stu-id="4e44a-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="4e44a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e44a-115">-DefaultProfile</span></span>
<span data-ttu-id="4e44a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e44a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e44a-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4e44a-117">-EndpointName</span></span>
<span data-ttu-id="4e44a-118">Azure CDN-végpont neve.</span><span class="sxs-lookup"><span data-stu-id="4e44a-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="4e44a-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="4e44a-119">-OriginGroupName</span></span>
<span data-ttu-id="4e44a-120">Azure CDN-forráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4e44a-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="4e44a-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="4e44a-121">-OriginId</span></span>
<span data-ttu-id="4e44a-122">Azure CDN-forráscsoport-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="4e44a-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="4e44a-123">-Az ÉtiIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="4e44a-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="4e44a-124">Az állapotok közti másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="4e44a-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="4e44a-125">-PathPath</span><span class="sxs-lookup"><span data-stu-id="4e44a-125">-ProbePath</span></span>
<span data-ttu-id="4e44a-126">A forrás állapotának meghatározásához használt forráshoz viszonyított elérési út.</span><span class="sxs-lookup"><span data-stu-id="4e44a-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="4e44a-127">-Az 10000000000000</span><span class="sxs-lookup"><span data-stu-id="4e44a-127">-ProbeProtocol</span></span>
<span data-ttu-id="4e44a-128">Protokoll egészségügyi problémákhoz.</span><span class="sxs-lookup"><span data-stu-id="4e44a-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="4e44a-129">-HcRequestType</span><span class="sxs-lookup"><span data-stu-id="4e44a-129">-ProbeRequestType</span></span>
<span data-ttu-id="4e44a-130">Az állapotkérés típusa.</span><span class="sxs-lookup"><span data-stu-id="4e44a-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="4e44a-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4e44a-131">-ProfileName</span></span>
<span data-ttu-id="4e44a-132">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="4e44a-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="4e44a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e44a-133">-ResourceGroupName</span></span>
<span data-ttu-id="4e44a-134">Az Azure CDN-profil erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="4e44a-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="4e44a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e44a-135">-Confirm</span></span>
<span data-ttu-id="4e44a-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4e44a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e44a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e44a-137">-WhatIf</span></span>
<span data-ttu-id="4e44a-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4e44a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e44a-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e44a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e44a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e44a-140">CommonParameters</span></span>
<span data-ttu-id="4e44a-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e44a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e44a-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e44a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e44a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e44a-143">INPUTS</span></span>

### <span data-ttu-id="4e44a-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="4e44a-144">System.Object</span></span>

## <span data-ttu-id="4e44a-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e44a-145">OUTPUTS</span></span>

### <span data-ttu-id="4e44a-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="4e44a-146">System.Object</span></span>

## <span data-ttu-id="4e44a-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4e44a-147">NOTES</span></span>

## <span data-ttu-id="4e44a-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e44a-148">RELATED LINKS</span></span>
