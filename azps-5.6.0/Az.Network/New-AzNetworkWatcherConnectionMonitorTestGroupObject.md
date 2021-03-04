---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: 4ab9feb0d99bc808cfabb481baf81bb12e050f28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921818"
---
# <span data-ttu-id="a033b-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="a033b-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="a033b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a033b-102">SYNOPSIS</span></span>
<span data-ttu-id="a033b-103">Kapcsolatfigyelő tesztcsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="a033b-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="a033b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a033b-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a033b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a033b-105">DESCRIPTION</span></span>
<span data-ttu-id="a033b-106">A New-AzNetworkWatcherConnectionMonitorTestGroupObject parancsmag létrehoz egy kapcsolatfigyelő tesztcsoportot.</span><span class="sxs-lookup"><span data-stu-id="a033b-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="a033b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a033b-107">EXAMPLES</span></span>

### <span data-ttu-id="a033b-108">1. példa: Tesztcsoport létrehozása 2 testConfigurations, w source és 2 cél végponttal</span><span class="sxs-lookup"><span data-stu-id="a033b-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="a033b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a033b-109">PARAMETERS</span></span>

### <span data-ttu-id="a033b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a033b-110">-DefaultProfile</span></span>
<span data-ttu-id="a033b-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a033b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a033b-112">-Destination</span><span class="sxs-lookup"><span data-stu-id="a033b-112">-Destination</span></span>
<span data-ttu-id="a033b-113">A cél végpontjainak listája.</span><span class="sxs-lookup"><span data-stu-id="a033b-113">List of destination endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a033b-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="a033b-114">-Disable</span></span>
<span data-ttu-id="a033b-115">Jelölő, amely jelzi, hogy a tesztcsoport le van-e tiltva.</span><span class="sxs-lookup"><span data-stu-id="a033b-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="a033b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a033b-116">-Name</span></span>
<span data-ttu-id="a033b-117">A tesztcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a033b-117">The test group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a033b-118">-Source</span><span class="sxs-lookup"><span data-stu-id="a033b-118">-Source</span></span>
<span data-ttu-id="a033b-119">A forrás végpontjainak listája.</span><span class="sxs-lookup"><span data-stu-id="a033b-119">List of source endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a033b-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="a033b-120">-TestConfiguration</span></span>
<span data-ttu-id="a033b-121">Tesztkonfigurációk listája.</span><span class="sxs-lookup"><span data-stu-id="a033b-121">List of test configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a033b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a033b-122">-Confirm</span></span>
<span data-ttu-id="a033b-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a033b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a033b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a033b-124">-WhatIf</span></span>
<span data-ttu-id="a033b-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a033b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a033b-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a033b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a033b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a033b-127">CommonParameters</span></span>
<span data-ttu-id="a033b-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a033b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a033b-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a033b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a033b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a033b-130">INPUTS</span></span>

### <span data-ttu-id="a033b-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="a033b-131">None</span></span>

## <span data-ttu-id="a033b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a033b-132">OUTPUTS</span></span>

### <span data-ttu-id="a033b-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="a033b-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="a033b-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a033b-134">NOTES</span></span>

## <span data-ttu-id="a033b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a033b-135">RELATED LINKS</span></span>
