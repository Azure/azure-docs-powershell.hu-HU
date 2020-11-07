---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 0a7bbc6832c5a0c6c871d2a5c35ac9ee86042fd0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669849"
---
# <span data-ttu-id="34c1b-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="34c1b-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="34c1b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="34c1b-103">Az Azure-tevékenység naplójának gyűjtése az adott előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="34c1b-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="34c1b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34c1b-104">SYNTAX</span></span>

### <span data-ttu-id="34c1b-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="34c1b-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34c1b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="34c1b-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34c1b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="34c1b-107">DESCRIPTION</span></span>
<span data-ttu-id="34c1b-108">A New-AzOperationalInsightsAzureActivityLogDataSource a log Analytics segítségével begyűjtheti az Azure Activity naplót az adott előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="34c1b-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="34c1b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="34c1b-109">EXAMPLES</span></span>

### <span data-ttu-id="34c1b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="34c1b-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="34c1b-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="34c1b-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="34c1b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34c1b-112">PARAMETERS</span></span>

### <span data-ttu-id="34c1b-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="34c1b-113">-BackfillStartTime</span></span>
<span data-ttu-id="34c1b-114">Választhat, hogy egy héttel ezelőtt backfill a naplókat.</span><span class="sxs-lookup"><span data-stu-id="34c1b-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c1b-115">-DefaultProfile</span></span>
<span data-ttu-id="34c1b-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="34c1b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34c1b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="34c1b-117">-Force</span></span>
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

### <span data-ttu-id="34c1b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="34c1b-118">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c1b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34c1b-119">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c1b-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34c1b-120">-SubscriptionId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c1b-121">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="34c1b-121">-Workspace</span></span>
```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34c1b-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="34c1b-122">-WorkspaceName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c1b-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="34c1b-123">-Confirm</span></span>
<span data-ttu-id="34c1b-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="34c1b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34c1b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34c1b-125">-WhatIf</span></span>
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

### <span data-ttu-id="34c1b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c1b-126">CommonParameters</span></span>
<span data-ttu-id="34c1b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34c1b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c1b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c1b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c1b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34c1b-129">INPUTS</span></span>

### <span data-ttu-id="34c1b-130">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="34c1b-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="34c1b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="34c1b-131">System.String</span></span>

### <span data-ttu-id="34c1b-132">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="34c1b-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="34c1b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34c1b-133">OUTPUTS</span></span>

### <span data-ttu-id="34c1b-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="34c1b-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="34c1b-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34c1b-135">NOTES</span></span>

## <span data-ttu-id="34c1b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34c1b-136">RELATED LINKS</span></span>
