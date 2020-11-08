---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointfilteritemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
ms.openlocfilehash: c06052ee28d849c5d07a941366efd15cbfeefe25
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024611"
---
# <span data-ttu-id="d1cba-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span><span class="sxs-lookup"><span data-stu-id="d1cba-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span></span>

## <span data-ttu-id="d1cba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1cba-102">SYNOPSIS</span></span>
<span data-ttu-id="d1cba-103">A kapcsolat monitor végpont-szűrő elemét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="d1cba-103">Creates a connection monitor endpoint filter item.</span></span>

## <span data-ttu-id="d1cba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1cba-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1cba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1cba-105">DESCRIPTION</span></span>
<span data-ttu-id="d1cba-106">Az New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject parancsmag végpont-szűrő elemet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d1cba-106">The New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet creates endpoint filter item.</span></span>

## <span data-ttu-id="d1cba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d1cba-107">EXAMPLES</span></span>

### <span data-ttu-id="d1cba-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d1cba-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "10.0.0.1"
```

<span data-ttu-id="d1cba-109">Típus: AgentAddress cím: 10.0.0.1</span><span class="sxs-lookup"><span data-stu-id="d1cba-109">Type    : AgentAddress Address : 10.0.0.1</span></span>

## <span data-ttu-id="d1cba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1cba-110">PARAMETERS</span></span>

### <span data-ttu-id="d1cba-111">-Address (cím)</span><span class="sxs-lookup"><span data-stu-id="d1cba-111">-Address</span></span>
<span data-ttu-id="d1cba-112">A szűrő elem címe.</span><span class="sxs-lookup"><span data-stu-id="d1cba-112">The address of the filter item.</span></span>

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

### <span data-ttu-id="d1cba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1cba-113">-DefaultProfile</span></span>
<span data-ttu-id="d1cba-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1cba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1cba-115">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="d1cba-115">-Type</span></span>
<span data-ttu-id="d1cba-116">A szűrőben található elem típusa.</span><span class="sxs-lookup"><span data-stu-id="d1cba-116">The type of item included in the filter.</span></span> <span data-ttu-id="d1cba-117">Jelenleg csak a "AgentAddress" támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1cba-117">Currently only 'AgentAddress' is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cba-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d1cba-118">-Confirm</span></span>
<span data-ttu-id="d1cba-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d1cba-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1cba-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1cba-120">-WhatIf</span></span>
<span data-ttu-id="d1cba-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d1cba-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1cba-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1cba-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1cba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1cba-123">CommonParameters</span></span>
<span data-ttu-id="d1cba-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1cba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1cba-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d1cba-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1cba-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1cba-126">INPUTS</span></span>

### <span data-ttu-id="d1cba-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="d1cba-127">None</span></span>

## <span data-ttu-id="d1cba-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1cba-128">OUTPUTS</span></span>

### <span data-ttu-id="d1cba-129">Microsoft. Azure. commands. Network. models. PSConnectionMonitorEndpointFilterItem</span><span class="sxs-lookup"><span data-stu-id="d1cba-129">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorEndpointFilterItem</span></span>

## <span data-ttu-id="d1cba-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1cba-130">NOTES</span></span>

## <span data-ttu-id="d1cba-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1cba-131">RELATED LINKS</span></span>
