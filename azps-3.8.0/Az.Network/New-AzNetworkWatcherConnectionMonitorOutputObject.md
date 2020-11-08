---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011020"
---
# <span data-ttu-id="3a100-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="3a100-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="3a100-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a100-102">SYNOPSIS</span></span>
<span data-ttu-id="3a100-103">A kapcsolat figyelése cél objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="3a100-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="3a100-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a100-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a100-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a100-105">DESCRIPTION</span></span>
<span data-ttu-id="3a100-106">Az New-AzNetworkWatcherConnectionMonitorOutputObject parancsmag a kapcsolat figyelése cél objektumot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="3a100-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="3a100-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3a100-107">EXAMPLES</span></span>

### <span data-ttu-id="3a100-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3a100-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="3a100-109">Írja be a következőt: "Munkaterület" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="3a100-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="3a100-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a100-110">PARAMETERS</span></span>

### <span data-ttu-id="3a100-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a100-111">-DefaultProfile</span></span>
<span data-ttu-id="3a100-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a100-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a100-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="3a100-113">-OutputType</span></span>
<span data-ttu-id="3a100-114">A kapcsolat-monitor kimeneti rendeltetési típusa.</span><span class="sxs-lookup"><span data-stu-id="3a100-114">Connection monitor output destination type.</span></span> <span data-ttu-id="3a100-115">Jelenleg csak \" a munkaterület \" támogatott.</span><span class="sxs-lookup"><span data-stu-id="3a100-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="3a100-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="3a100-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="3a100-117">Log Analytics Workspace-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="3a100-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="3a100-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3a100-118">-Confirm</span></span>
<span data-ttu-id="3a100-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3a100-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a100-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a100-120">-WhatIf</span></span>
<span data-ttu-id="3a100-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3a100-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a100-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3a100-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a100-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a100-123">CommonParameters</span></span>
<span data-ttu-id="3a100-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a100-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a100-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3a100-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a100-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a100-126">INPUTS</span></span>

### <span data-ttu-id="3a100-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="3a100-127">None</span></span>

## <span data-ttu-id="3a100-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a100-128">OUTPUTS</span></span>

### <span data-ttu-id="3a100-129">Microsoft. Azure. commands. Network. models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="3a100-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="3a100-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a100-130">NOTES</span></span>

## <span data-ttu-id="3a100-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a100-131">RELATED LINKS</span></span>
