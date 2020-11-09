---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301460"
---
# <span data-ttu-id="95a35-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="95a35-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="95a35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95a35-102">SYNOPSIS</span></span>
<span data-ttu-id="95a35-103">Létrehozza a kapcsolat monitor végpont-hatóköri elemét.</span><span class="sxs-lookup"><span data-stu-id="95a35-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="95a35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95a35-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95a35-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="95a35-105">DESCRIPTION</span></span>
<span data-ttu-id="95a35-106">A New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject parancsmag végpont-hatóköri elemet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="95a35-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="95a35-107">Példák</span><span class="sxs-lookup"><span data-stu-id="95a35-107">EXAMPLES</span></span>

### <span data-ttu-id="95a35-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="95a35-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="95a35-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95a35-109">PARAMETERS</span></span>

### <span data-ttu-id="95a35-110">-Address (cím)</span><span class="sxs-lookup"><span data-stu-id="95a35-110">-Address</span></span>
<span data-ttu-id="95a35-111">A hatóköri elem címe.</span><span class="sxs-lookup"><span data-stu-id="95a35-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="95a35-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95a35-112">-DefaultProfile</span></span>
<span data-ttu-id="95a35-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95a35-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95a35-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="95a35-114">-Confirm</span></span>
<span data-ttu-id="95a35-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="95a35-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95a35-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95a35-116">-WhatIf</span></span>
<span data-ttu-id="95a35-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="95a35-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95a35-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95a35-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95a35-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a35-119">CommonParameters</span></span>
<span data-ttu-id="95a35-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95a35-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a35-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="95a35-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a35-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95a35-122">INPUTS</span></span>

### <span data-ttu-id="95a35-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="95a35-123">None</span></span>

## <span data-ttu-id="95a35-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95a35-124">OUTPUTS</span></span>

### <span data-ttu-id="95a35-125">Microsoft. Azure. commands. Network. models. PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="95a35-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="95a35-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95a35-126">NOTES</span></span>

## <span data-ttu-id="95a35-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95a35-127">RELATED LINKS</span></span>
