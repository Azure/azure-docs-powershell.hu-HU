---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349037"
---
# <span data-ttu-id="a5507-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a5507-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="a5507-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5507-102">SYNOPSIS</span></span>
<span data-ttu-id="a5507-103">A CDN-forráscsoport frissítése</span><span class="sxs-lookup"><span data-stu-id="a5507-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="a5507-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5507-104">SYNTAX</span></span>

### <span data-ttu-id="a5507-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5507-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5507-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5507-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5507-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5507-107">DESCRIPTION</span></span>
<span data-ttu-id="a5507-108">Set-AzCdnOriginGroup frissíti a megadott origincsoportot a megadott végponton belül.</span><span class="sxs-lookup"><span data-stu-id="a5507-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="a5507-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5507-109">EXAMPLES</span></span>

### <span data-ttu-id="a5507-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a5507-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="a5507-111">Ezzel a parancsmagtal frissítheti az Origin csoportBan található ABerevalInSeconds tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="a5507-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="a5507-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5507-112">PARAMETERS</span></span>

### <span data-ttu-id="a5507-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a5507-113">-CdnOriginGroup</span></span>
<span data-ttu-id="a5507-114">A CDN-forráscsoport objektuma.</span><span class="sxs-lookup"><span data-stu-id="a5507-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="a5507-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5507-115">-DefaultProfile</span></span>
<span data-ttu-id="a5507-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5507-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5507-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a5507-117">-EndpointName</span></span>
<span data-ttu-id="a5507-118">Azure CDN-végpont neve.</span><span class="sxs-lookup"><span data-stu-id="a5507-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="a5507-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="a5507-119">-OriginGroupName</span></span>
<span data-ttu-id="a5507-120">Azure CDN-forráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5507-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="a5507-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="a5507-121">-OriginId</span></span>
<span data-ttu-id="a5507-122">Azure CDN-forráscsoport-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="a5507-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="a5507-123">-Az ÉtiIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a5507-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="a5507-124">Az állapotok közti másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="a5507-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="a5507-125">-PathPath</span><span class="sxs-lookup"><span data-stu-id="a5507-125">-ProbePath</span></span>
<span data-ttu-id="a5507-126">A forrás állapotának meghatározásához használt forráshoz viszonyított elérési út.</span><span class="sxs-lookup"><span data-stu-id="a5507-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="a5507-127">-EgyszokProtocol</span><span class="sxs-lookup"><span data-stu-id="a5507-127">-ProbeProtocol</span></span>
<span data-ttu-id="a5507-128">Protokoll egészségügyi problémákhoz.</span><span class="sxs-lookup"><span data-stu-id="a5507-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="a5507-129">-HcRequestType</span><span class="sxs-lookup"><span data-stu-id="a5507-129">-ProbeRequestType</span></span>
<span data-ttu-id="a5507-130">Az állapotkérés típusa.</span><span class="sxs-lookup"><span data-stu-id="a5507-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="a5507-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a5507-131">-ProfileName</span></span>
<span data-ttu-id="a5507-132">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="a5507-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="a5507-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5507-133">-ResourceGroupName</span></span>
<span data-ttu-id="a5507-134">Az Azure CDN-profil erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="a5507-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="a5507-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5507-135">-Confirm</span></span>
<span data-ttu-id="a5507-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a5507-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5507-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5507-137">-WhatIf</span></span>
<span data-ttu-id="a5507-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a5507-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5507-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5507-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5507-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5507-140">CommonParameters</span></span>
<span data-ttu-id="a5507-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5507-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5507-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5507-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5507-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5507-143">INPUTS</span></span>

### <span data-ttu-id="a5507-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="a5507-144">System.Object</span></span>

## <span data-ttu-id="a5507-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5507-145">OUTPUTS</span></span>

### <span data-ttu-id="a5507-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="a5507-146">System.Object</span></span>

## <span data-ttu-id="a5507-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5507-147">NOTES</span></span>

## <span data-ttu-id="a5507-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5507-148">RELATED LINKS</span></span>
