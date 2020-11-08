---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187639"
---
# <span data-ttu-id="d53b5-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="d53b5-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="d53b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d53b5-102">SYNOPSIS</span></span>
<span data-ttu-id="d53b5-103">A CDN-származási csoport frissítése</span><span class="sxs-lookup"><span data-stu-id="d53b5-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="d53b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d53b5-104">SYNTAX</span></span>

### <span data-ttu-id="d53b5-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d53b5-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d53b5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d53b5-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d53b5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d53b5-107">DESCRIPTION</span></span>
<span data-ttu-id="d53b5-108">A Set-AzCdnOriginGroup frissíti a megadott Origó csoportot az adott végponton belül.</span><span class="sxs-lookup"><span data-stu-id="d53b5-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="d53b5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d53b5-109">EXAMPLES</span></span>

### <span data-ttu-id="d53b5-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d53b5-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="d53b5-111">Ez a parancsmag frissíti a ProbeIntervalInSeconds tulajdonságot a kezdőpont csoportban.</span><span class="sxs-lookup"><span data-stu-id="d53b5-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="d53b5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d53b5-112">PARAMETERS</span></span>

### <span data-ttu-id="d53b5-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="d53b5-113">-CdnOriginGroup</span></span>
<span data-ttu-id="d53b5-114">A CDN származási csoport objektuma.</span><span class="sxs-lookup"><span data-stu-id="d53b5-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="d53b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53b5-115">-DefaultProfile</span></span>
<span data-ttu-id="d53b5-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d53b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d53b5-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d53b5-117">-EndpointName</span></span>
<span data-ttu-id="d53b5-118">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="d53b5-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d53b5-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="d53b5-119">-OriginGroupName</span></span>
<span data-ttu-id="d53b5-120">Azure CDN származási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d53b5-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="d53b5-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="d53b5-121">-OriginId</span></span>
<span data-ttu-id="d53b5-122">Azure CDN Origin Group azonosítók.</span><span class="sxs-lookup"><span data-stu-id="d53b5-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="d53b5-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d53b5-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="d53b5-124">Az egészségügyi Szondák közötti másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="d53b5-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="d53b5-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="d53b5-125">-ProbePath</span></span>
<span data-ttu-id="d53b5-126">A származási állapot meghatározásához használt kezdőponthoz viszonyított útvonal.</span><span class="sxs-lookup"><span data-stu-id="d53b5-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="d53b5-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="d53b5-127">-ProbeProtocol</span></span>
<span data-ttu-id="d53b5-128">Az egészségi szondához használandó protokoll.</span><span class="sxs-lookup"><span data-stu-id="d53b5-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="d53b5-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="d53b5-129">-ProbeRequestType</span></span>
<span data-ttu-id="d53b5-130">Az elvégzett állapottanúsítvány-kérés típusa.</span><span class="sxs-lookup"><span data-stu-id="d53b5-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="d53b5-131">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="d53b5-131">-ProfileName</span></span>
<span data-ttu-id="d53b5-132">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="d53b5-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d53b5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d53b5-133">-ResourceGroupName</span></span>
<span data-ttu-id="d53b5-134">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="d53b5-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="d53b5-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d53b5-135">-Confirm</span></span>
<span data-ttu-id="d53b5-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d53b5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d53b5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d53b5-137">-WhatIf</span></span>
<span data-ttu-id="d53b5-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d53b5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d53b5-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d53b5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d53b5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53b5-140">CommonParameters</span></span>
<span data-ttu-id="d53b5-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d53b5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53b5-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d53b5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53b5-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d53b5-143">INPUTS</span></span>

### <span data-ttu-id="d53b5-144">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="d53b5-144">System.Object</span></span>

## <span data-ttu-id="d53b5-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d53b5-145">OUTPUTS</span></span>

### <span data-ttu-id="d53b5-146">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="d53b5-146">System.Object</span></span>

## <span data-ttu-id="d53b5-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d53b5-147">NOTES</span></span>

## <span data-ttu-id="d53b5-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d53b5-148">RELATED LINKS</span></span>
