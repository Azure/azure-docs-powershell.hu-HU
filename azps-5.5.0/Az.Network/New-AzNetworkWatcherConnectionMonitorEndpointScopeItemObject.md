---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151667"
---
# <span data-ttu-id="b106c-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="b106c-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="b106c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b106c-102">SYNOPSIS</span></span>
<span data-ttu-id="b106c-103">Kapcsolatfigyelő végpont hatókörének elemét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b106c-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="b106c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b106c-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b106c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b106c-105">DESCRIPTION</span></span>
<span data-ttu-id="b106c-106">A New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject parancsmag létrehozza a végpont hatókörének elemét.</span><span class="sxs-lookup"><span data-stu-id="b106c-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="b106c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b106c-107">EXAMPLES</span></span>

### <span data-ttu-id="b106c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b106c-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="b106c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b106c-109">PARAMETERS</span></span>

### <span data-ttu-id="b106c-110">-Address</span><span class="sxs-lookup"><span data-stu-id="b106c-110">-Address</span></span>
<span data-ttu-id="b106c-111">A hatókörelem címe.</span><span class="sxs-lookup"><span data-stu-id="b106c-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="b106c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b106c-112">-DefaultProfile</span></span>
<span data-ttu-id="b106c-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b106c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b106c-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b106c-114">-Confirm</span></span>
<span data-ttu-id="b106c-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b106c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b106c-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b106c-116">-WhatIf</span></span>
<span data-ttu-id="b106c-117">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b106c-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b106c-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b106c-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b106c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b106c-119">CommonParameters</span></span>
<span data-ttu-id="b106c-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b106c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b106c-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b106c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b106c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b106c-122">INPUTS</span></span>

### <span data-ttu-id="b106c-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="b106c-123">None</span></span>

## <span data-ttu-id="b106c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b106c-124">OUTPUTS</span></span>

### <span data-ttu-id="b106c-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="b106c-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="b106c-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b106c-126">NOTES</span></span>

## <span data-ttu-id="b106c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b106c-127">RELATED LINKS</span></span>
