---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302712"
---
# <span data-ttu-id="b9931-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="b9931-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="b9931-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9931-102">SYNOPSIS</span></span>
<span data-ttu-id="b9931-103">A kapcsolat figyelése cél objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="b9931-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="b9931-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9931-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9931-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9931-105">DESCRIPTION</span></span>
<span data-ttu-id="b9931-106">Az New-AzNetworkWatcherConnectionMonitorOutputObject parancsmag a kapcsolat figyelése cél objektumot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b9931-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="b9931-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b9931-107">EXAMPLES</span></span>

### <span data-ttu-id="b9931-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b9931-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="b9931-109">Írja be a következőt: "Munkaterület" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="b9931-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="b9931-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9931-110">PARAMETERS</span></span>

### <span data-ttu-id="b9931-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9931-111">-DefaultProfile</span></span>
<span data-ttu-id="b9931-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9931-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9931-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="b9931-113">-OutputType</span></span>
<span data-ttu-id="b9931-114">A kapcsolat-monitor kimeneti rendeltetési típusa.</span><span class="sxs-lookup"><span data-stu-id="b9931-114">Connection monitor output destination type.</span></span> <span data-ttu-id="b9931-115">Jelenleg csak \" a munkaterület \" támogatott.</span><span class="sxs-lookup"><span data-stu-id="b9931-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="b9931-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="b9931-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="b9931-117">Log Analytics Workspace-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="b9931-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="b9931-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9931-118">-Confirm</span></span>
<span data-ttu-id="b9931-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9931-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9931-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9931-120">-WhatIf</span></span>
<span data-ttu-id="b9931-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9931-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9931-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9931-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9931-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9931-123">CommonParameters</span></span>
<span data-ttu-id="b9931-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9931-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9931-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b9931-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9931-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9931-126">INPUTS</span></span>

### <span data-ttu-id="b9931-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="b9931-127">None</span></span>

## <span data-ttu-id="b9931-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9931-128">OUTPUTS</span></span>

### <span data-ttu-id="b9931-129">Microsoft. Azure. commands. Network. models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="b9931-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="b9931-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9931-130">NOTES</span></span>

## <span data-ttu-id="b9931-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9931-131">RELATED LINKS</span></span>
