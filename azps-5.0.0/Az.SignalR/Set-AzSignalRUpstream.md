---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302420"
---
# <span data-ttu-id="08d2e-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="08d2e-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="08d2e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="08d2e-103">Adja meg a jelző szolgáltatás upstream beállításait.</span><span class="sxs-lookup"><span data-stu-id="08d2e-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="08d2e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08d2e-104">SYNTAX</span></span>

### <span data-ttu-id="08d2e-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08d2e-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08d2e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08d2e-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08d2e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08d2e-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08d2e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="08d2e-108">DESCRIPTION</span></span>
<span data-ttu-id="08d2e-109">Adja meg a jelző szolgáltatás upstream beállításait.</span><span class="sxs-lookup"><span data-stu-id="08d2e-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="08d2e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="08d2e-110">EXAMPLES</span></span>

### <span data-ttu-id="08d2e-111">Két rendezett upstream sablon beállítása</span><span class="sxs-lookup"><span data-stu-id="08d2e-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="08d2e-112">A következő JSON a tényleges sablonokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="08d2e-112">The following JSON represents the actual templates set.</span></span> 

 `
{
    "hubPattern": "chat",
    "eventPattern": "broadcast",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections1.com"
},
{
    "hubPattern": "*",
    "eventPattern": "*",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections2.com"
}
`

### <span data-ttu-id="08d2e-113">Az összes upstream beállítás törlése</span><span class="sxs-lookup"><span data-stu-id="08d2e-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="08d2e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08d2e-114">PARAMETERS</span></span>

### <span data-ttu-id="08d2e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08d2e-115">-AsJob</span></span>
<span data-ttu-id="08d2e-116">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="08d2e-116">Run the cmdlet in background job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d2e-117">-Clear (Törlés)</span><span class="sxs-lookup"><span data-stu-id="08d2e-117">-Clear</span></span>
<span data-ttu-id="08d2e-118">Törölje a jelet az összes upstream beállításból.</span><span class="sxs-lookup"><span data-stu-id="08d2e-118">Clear all the upstream settings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d2e-119">-DefaultProfile</span></span>
<span data-ttu-id="08d2e-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08d2e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08d2e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08d2e-121">-InputObject</span></span>
<span data-ttu-id="08d2e-122">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="08d2e-122">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08d2e-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08d2e-123">-Name</span></span>
<span data-ttu-id="08d2e-124">A szignáló szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="08d2e-124">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d2e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08d2e-125">-ResourceGroupName</span></span>
<span data-ttu-id="08d2e-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="08d2e-126">The resource group name.</span></span>
<span data-ttu-id="08d2e-127">A program az alapértelmezett értéket használja, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="08d2e-127">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d2e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08d2e-128">-ResourceId</span></span>
<span data-ttu-id="08d2e-129">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="08d2e-129">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08d2e-130">-Sablon</span><span class="sxs-lookup"><span data-stu-id="08d2e-130">-Template</span></span>
<span data-ttu-id="08d2e-131">Sablon elem (ek) a upstream beállításokhoz.</span><span class="sxs-lookup"><span data-stu-id="08d2e-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="08d2e-132">Kötelező kulcs: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="08d2e-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="08d2e-133">Választható billentyűk: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="08d2e-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="08d2e-134">Példa: splatting: @ {UrlTemplate = ' http://host-connections1.com ', HubPattern = ' csevegés '; EventPattern = ' Broadcast '}, @ {UrlTemplate = ' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="08d2e-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d2e-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="08d2e-135">-Confirm</span></span>
<span data-ttu-id="08d2e-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="08d2e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08d2e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08d2e-137">-WhatIf</span></span>
<span data-ttu-id="08d2e-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="08d2e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08d2e-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08d2e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08d2e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d2e-140">CommonParameters</span></span>
<span data-ttu-id="08d2e-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08d2e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d2e-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="08d2e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d2e-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08d2e-143">INPUTS</span></span>

### <span data-ttu-id="08d2e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="08d2e-144">System.String</span></span>

## <span data-ttu-id="08d2e-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08d2e-145">OUTPUTS</span></span>

### <span data-ttu-id="08d2e-146">Microsoft. Azure. Command. Signal. models. PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="08d2e-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="08d2e-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08d2e-147">NOTES</span></span>

## <span data-ttu-id="08d2e-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08d2e-148">RELATED LINKS</span></span>

[<span data-ttu-id="08d2e-149">Paraméterek továbbítása a PowerShellben a splatting használatával</span><span class="sxs-lookup"><span data-stu-id="08d2e-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
