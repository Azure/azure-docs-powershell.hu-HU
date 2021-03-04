---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 895659481999ab5801538bec3b88765e1d48aeca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921865"
---
# <span data-ttu-id="1f331-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="1f331-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="1f331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f331-102">SYNOPSIS</span></span>
<span data-ttu-id="1f331-103">Kapcsolatfigyelő kimeneti célobjektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="1f331-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="1f331-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1f331-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f331-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1f331-105">DESCRIPTION</span></span>
<span data-ttu-id="1f331-106">A New-AzNetworkWatcherConnectionMonitorOutputObject parancsmag létrehozza a kapcsolatfigyelő kimeneti célobjektumát.</span><span class="sxs-lookup"><span data-stu-id="1f331-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="1f331-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1f331-107">EXAMPLES</span></span>

### <span data-ttu-id="1f331-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1f331-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="1f331-109">Típus: "munkaterület" WorkspaceSettings: { "WorkspaceResourceId": "MyWSResourceId" }</span><span class="sxs-lookup"><span data-stu-id="1f331-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="1f331-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f331-110">PARAMETERS</span></span>

### <span data-ttu-id="1f331-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f331-111">-DefaultProfile</span></span>
<span data-ttu-id="1f331-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f331-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f331-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="1f331-113">-OutputType</span></span>
<span data-ttu-id="1f331-114">A kapcsolatfigyelő kimeneti céltípusa.</span><span class="sxs-lookup"><span data-stu-id="1f331-114">Connection monitor output destination type.</span></span> <span data-ttu-id="1f331-115">Jelenleg csak \" a Munkaterület \" támogatott.</span><span class="sxs-lookup"><span data-stu-id="1f331-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="1f331-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="1f331-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="1f331-117">Log analytics workspace resource ID.</span><span class="sxs-lookup"><span data-stu-id="1f331-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="1f331-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f331-118">-Confirm</span></span>
<span data-ttu-id="1f331-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1f331-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f331-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f331-120">-WhatIf</span></span>
<span data-ttu-id="1f331-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1f331-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f331-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f331-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f331-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f331-123">CommonParameters</span></span>
<span data-ttu-id="1f331-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f331-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f331-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f331-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f331-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f331-126">INPUTS</span></span>

### <span data-ttu-id="1f331-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="1f331-127">None</span></span>

## <span data-ttu-id="1f331-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f331-128">OUTPUTS</span></span>

### <span data-ttu-id="1f331-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="1f331-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="1f331-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1f331-130">NOTES</span></span>

## <span data-ttu-id="1f331-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f331-131">RELATED LINKS</span></span>
