---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: ec1bba32027d3ec96aef61f3abec7d51cec5c35b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372202"
---
# <span data-ttu-id="eaf87-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="eaf87-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="eaf87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaf87-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf87-103">Kapcsolatfigyelő kimeneti célobjektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="eaf87-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="eaf87-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eaf87-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaf87-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eaf87-105">DESCRIPTION</span></span>
<span data-ttu-id="eaf87-106">A New-AzNetworkWatcherConnectionMonitorOutputObject parancsmag létrehozza a kapcsolatfigyelő kimeneti célobjektumát.</span><span class="sxs-lookup"><span data-stu-id="eaf87-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="eaf87-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eaf87-107">EXAMPLES</span></span>

### <span data-ttu-id="eaf87-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="eaf87-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="eaf87-109">Típus: "munkaterület" WorkspaceSettings: { "WorkspaceResourceId": "MyWSResourceId" }</span><span class="sxs-lookup"><span data-stu-id="eaf87-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="eaf87-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaf87-110">PARAMETERS</span></span>

### <span data-ttu-id="eaf87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf87-111">-DefaultProfile</span></span>
<span data-ttu-id="eaf87-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eaf87-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaf87-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="eaf87-113">-OutputType</span></span>
<span data-ttu-id="eaf87-114">A kapcsolatfigyelő kimeneti céltípusa.</span><span class="sxs-lookup"><span data-stu-id="eaf87-114">Connection monitor output destination type.</span></span> <span data-ttu-id="eaf87-115">Jelenleg csak \" a Munkaterület \" támogatott.</span><span class="sxs-lookup"><span data-stu-id="eaf87-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="eaf87-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="eaf87-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="eaf87-117">Log analytics workspace resource ID.</span><span class="sxs-lookup"><span data-stu-id="eaf87-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="eaf87-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaf87-118">-Confirm</span></span>
<span data-ttu-id="eaf87-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eaf87-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf87-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf87-120">-WhatIf</span></span>
<span data-ttu-id="eaf87-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eaf87-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaf87-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eaf87-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf87-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf87-123">CommonParameters</span></span>
<span data-ttu-id="eaf87-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaf87-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf87-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eaf87-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf87-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eaf87-126">INPUTS</span></span>

### <span data-ttu-id="eaf87-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="eaf87-127">None</span></span>

## <span data-ttu-id="eaf87-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eaf87-128">OUTPUTS</span></span>

### <span data-ttu-id="eaf87-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="eaf87-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="eaf87-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eaf87-130">NOTES</span></span>

## <span data-ttu-id="eaf87-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eaf87-131">RELATED LINKS</span></span>
