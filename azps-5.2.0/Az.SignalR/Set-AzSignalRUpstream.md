---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338957"
---
# <span data-ttu-id="456a2-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="456a2-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="456a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="456a2-102">SYNOPSIS</span></span>
<span data-ttu-id="456a2-103">Adja meg a SignalR szolgáltatás upstream beállításait.</span><span class="sxs-lookup"><span data-stu-id="456a2-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="456a2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="456a2-104">SYNTAX</span></span>

### <span data-ttu-id="456a2-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="456a2-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="456a2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="456a2-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="456a2-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="456a2-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="456a2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="456a2-108">DESCRIPTION</span></span>
<span data-ttu-id="456a2-109">Adja meg a SignalR szolgáltatás upstream beállításait.</span><span class="sxs-lookup"><span data-stu-id="456a2-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="456a2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="456a2-110">EXAMPLES</span></span>

### <span data-ttu-id="456a2-111">Két rendezett upstream sablon beállítása</span><span class="sxs-lookup"><span data-stu-id="456a2-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="456a2-112">Az alábbi JSON a tényleges sablonok készletét jelöli.</span><span class="sxs-lookup"><span data-stu-id="456a2-112">The following JSON represents the actual templates set.</span></span> 

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

### <span data-ttu-id="456a2-113">Az összes felfelé irányuló beállítás módosítása</span><span class="sxs-lookup"><span data-stu-id="456a2-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="456a2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="456a2-114">PARAMETERS</span></span>

### <span data-ttu-id="456a2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="456a2-115">-AsJob</span></span>
<span data-ttu-id="456a2-116">Futtassa a parancsmagot a háttérben futó feladatban.</span><span class="sxs-lookup"><span data-stu-id="456a2-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="456a2-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="456a2-117">-Clear</span></span>
<span data-ttu-id="456a2-118">Törölje az összes felfelé irányuló beállítást.</span><span class="sxs-lookup"><span data-stu-id="456a2-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="456a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="456a2-119">-DefaultProfile</span></span>
<span data-ttu-id="456a2-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="456a2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="456a2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="456a2-121">-InputObject</span></span>
<span data-ttu-id="456a2-122">A SignalR erőforrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="456a2-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="456a2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="456a2-123">-Name</span></span>
<span data-ttu-id="456a2-124">A SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="456a2-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="456a2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="456a2-125">-ResourceGroupName</span></span>
<span data-ttu-id="456a2-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="456a2-126">The resource group name.</span></span>
<span data-ttu-id="456a2-127">Ha nincs megadva, a program az alapértelmezett beállítást használja.</span><span class="sxs-lookup"><span data-stu-id="456a2-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="456a2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="456a2-128">-ResourceId</span></span>
<span data-ttu-id="456a2-129">A SignalR szolgáltatáserőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="456a2-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="456a2-130">-Template</span><span class="sxs-lookup"><span data-stu-id="456a2-130">-Template</span></span>
<span data-ttu-id="456a2-131">Template item(s) for upstream settings.</span><span class="sxs-lookup"><span data-stu-id="456a2-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="456a2-132">Kötelező kulcs: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="456a2-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="456a2-133">Választható kulcsok: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="456a2-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="456a2-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate=' http://host-connections1.com ', HubPattern= 'chat'; EventPattern='broadcast' },@{UrlTemplate=' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="456a2-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

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

### <span data-ttu-id="456a2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="456a2-135">-Confirm</span></span>
<span data-ttu-id="456a2-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="456a2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="456a2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="456a2-137">-WhatIf</span></span>
<span data-ttu-id="456a2-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="456a2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="456a2-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="456a2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="456a2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456a2-140">CommonParameters</span></span>
<span data-ttu-id="456a2-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="456a2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456a2-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="456a2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456a2-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="456a2-143">INPUTS</span></span>

### <span data-ttu-id="456a2-144">System.String</span><span class="sxs-lookup"><span data-stu-id="456a2-144">System.String</span></span>

## <span data-ttu-id="456a2-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="456a2-145">OUTPUTS</span></span>

### <span data-ttu-id="456a2-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="456a2-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="456a2-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="456a2-147">NOTES</span></span>

## <span data-ttu-id="456a2-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="456a2-148">RELATED LINKS</span></span>

[<span data-ttu-id="456a2-149">Paraméterek bérlete a PowerShell parancsaiba splatting használatával</span><span class="sxs-lookup"><span data-stu-id="456a2-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
