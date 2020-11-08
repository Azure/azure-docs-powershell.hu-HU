---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025182"
---
# <span data-ttu-id="d46de-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="d46de-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="d46de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d46de-102">SYNOPSIS</span></span>
<span data-ttu-id="d46de-103">Kapcsolati figyelő tesztelési csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="d46de-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="d46de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d46de-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d46de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d46de-105">DESCRIPTION</span></span>
<span data-ttu-id="d46de-106">Az New-AzNetworkWatcherConnectionMonitorTestGroupObject parancsmag létrehoz egy kapcsolat figyelője tesztelési csoportot.</span><span class="sxs-lookup"><span data-stu-id="d46de-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="d46de-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d46de-107">EXAMPLES</span></span>

### <span data-ttu-id="d46de-108">1. példa: a teszt csoport létrehozása 2 testConfigurations, w forrás és 2 cél végponttal</span><span class="sxs-lookup"><span data-stu-id="d46de-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="d46de-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d46de-109">PARAMETERS</span></span>

### <span data-ttu-id="d46de-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46de-110">-DefaultProfile</span></span>
<span data-ttu-id="d46de-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d46de-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d46de-112">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="d46de-112">-Destination</span></span>
<span data-ttu-id="d46de-113">A cél végpontok listája.</span><span class="sxs-lookup"><span data-stu-id="d46de-113">List of destination endpoints.</span></span>

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

### <span data-ttu-id="d46de-114">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="d46de-114">-Disable</span></span>
<span data-ttu-id="d46de-115">Annak jelzése, hogy a teszt csoport le van-e tiltva.</span><span class="sxs-lookup"><span data-stu-id="d46de-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="d46de-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d46de-116">-Name</span></span>
<span data-ttu-id="d46de-117">A teszt csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d46de-117">The test group name.</span></span>

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

### <span data-ttu-id="d46de-118">-Forrás</span><span class="sxs-lookup"><span data-stu-id="d46de-118">-Source</span></span>
<span data-ttu-id="d46de-119">A forrás végpontok listája.</span><span class="sxs-lookup"><span data-stu-id="d46de-119">List of source endpoints.</span></span>

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

### <span data-ttu-id="d46de-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="d46de-120">-TestConfiguration</span></span>
<span data-ttu-id="d46de-121">A teszt konfigurációjának listája.</span><span class="sxs-lookup"><span data-stu-id="d46de-121">List of test configuration.</span></span>

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

### <span data-ttu-id="d46de-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d46de-122">-Confirm</span></span>
<span data-ttu-id="d46de-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d46de-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d46de-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46de-124">-WhatIf</span></span>
<span data-ttu-id="d46de-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d46de-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d46de-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d46de-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d46de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46de-127">CommonParameters</span></span>
<span data-ttu-id="d46de-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d46de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46de-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d46de-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46de-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d46de-130">INPUTS</span></span>

### <span data-ttu-id="d46de-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="d46de-131">None</span></span>

## <span data-ttu-id="d46de-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d46de-132">OUTPUTS</span></span>

### <span data-ttu-id="d46de-133">Microsoft. Azure. commands. Network. models. PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="d46de-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="d46de-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d46de-134">NOTES</span></span>

## <span data-ttu-id="d46de-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d46de-135">RELATED LINKS</span></span>
