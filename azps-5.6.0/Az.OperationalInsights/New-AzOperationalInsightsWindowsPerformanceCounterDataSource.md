---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 2e3cd573c337d7ff13401939aaf127fa64a6c765
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937953"
---
# <span data-ttu-id="49ed7-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="49ed7-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="49ed7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="49ed7-103">Hozzáadja a Windows teljesítményszámláló adatforrását a Windows operációs rendszert futtató csatlakoztatott számítógépekhez.</span><span class="sxs-lookup"><span data-stu-id="49ed7-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="49ed7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49ed7-104">SYNTAX</span></span>

### <span data-ttu-id="49ed7-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49ed7-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ed7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="49ed7-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49ed7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49ed7-107">DESCRIPTION</span></span>
<span data-ttu-id="49ed7-108">A **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** parancsmag hozzáad egy Windows teljesítményszámláló adatforrást a Windows operációs rendszert futtató csatlakoztatott számítógépekhez.</span><span class="sxs-lookup"><span data-stu-id="49ed7-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="49ed7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49ed7-109">EXAMPLES</span></span>

## <span data-ttu-id="49ed7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49ed7-110">PARAMETERS</span></span>

### <span data-ttu-id="49ed7-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="49ed7-111">-CounterName</span></span>
<span data-ttu-id="49ed7-112">Egy számláló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49ed7-112">Specifies the name of a counter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ed7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ed7-113">-DefaultProfile</span></span>
<span data-ttu-id="49ed7-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="49ed7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49ed7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="49ed7-115">-Force</span></span>
<span data-ttu-id="49ed7-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="49ed7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="49ed7-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="49ed7-117">-InstanceName</span></span>
<span data-ttu-id="49ed7-118">Egy példánynevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="49ed7-118">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ed7-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="49ed7-119">-IntervalSeconds</span></span>
<span data-ttu-id="49ed7-120">A gyűjtemény időközét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49ed7-120">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ed7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="49ed7-121">-Name</span></span>
<span data-ttu-id="49ed7-122">Megadja az adatforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="49ed7-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="49ed7-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="49ed7-123">-ObjectName</span></span>
<span data-ttu-id="49ed7-124">Egy objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49ed7-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="49ed7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49ed7-125">-ResourceGroupName</span></span>
<span data-ttu-id="49ed7-126">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49ed7-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="49ed7-127">-UseLegacyCollevessző</span><span class="sxs-lookup"><span data-stu-id="49ed7-127">-UseLegacyCollector</span></span>
<span data-ttu-id="49ed7-128">Használja a régi és az alapértelmezett 1656-et.</span><span class="sxs-lookup"><span data-stu-id="49ed7-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="49ed7-129">-Workspace</span><span class="sxs-lookup"><span data-stu-id="49ed7-129">-Workspace</span></span>
<span data-ttu-id="49ed7-130">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="49ed7-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="49ed7-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="49ed7-131">-WorkspaceName</span></span>
<span data-ttu-id="49ed7-132">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="49ed7-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="49ed7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49ed7-133">-Confirm</span></span>
<span data-ttu-id="49ed7-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="49ed7-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ed7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ed7-135">-WhatIf</span></span>
<span data-ttu-id="49ed7-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="49ed7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49ed7-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49ed7-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ed7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ed7-138">CommonParameters</span></span>
<span data-ttu-id="49ed7-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ed7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ed7-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ed7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ed7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49ed7-141">INPUTS</span></span>

### <span data-ttu-id="49ed7-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="49ed7-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="49ed7-143">System.String</span><span class="sxs-lookup"><span data-stu-id="49ed7-143">System.String</span></span>

### <span data-ttu-id="49ed7-144">System.Int32</span><span class="sxs-lookup"><span data-stu-id="49ed7-144">System.Int32</span></span>

## <span data-ttu-id="49ed7-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49ed7-145">OUTPUTS</span></span>

### <span data-ttu-id="49ed7-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="49ed7-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="49ed7-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49ed7-147">NOTES</span></span>

## <span data-ttu-id="49ed7-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49ed7-148">RELATED LINKS</span></span>
