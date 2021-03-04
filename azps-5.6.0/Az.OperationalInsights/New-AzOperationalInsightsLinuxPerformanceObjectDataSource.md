---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 7a6914d6259cafaedff68b28e8691311245ef6f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937977"
---
# <span data-ttu-id="66c14-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="66c14-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="66c14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66c14-102">SYNOPSIS</span></span>
<span data-ttu-id="66c14-103">Teljesítményszámlálókat ad a munkaterületen lévő linuxos számítógépekhez.</span><span class="sxs-lookup"><span data-stu-id="66c14-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="66c14-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="66c14-104">SYNTAX</span></span>

### <span data-ttu-id="66c14-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66c14-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66c14-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="66c14-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66c14-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="66c14-107">DESCRIPTION</span></span>
<span data-ttu-id="66c14-108">A **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** parancsmag teljesítmény-számlálókat ad hozzá, amelyekből az Azure Operational Insights adatokat gyűjt egy munkaterület összes Linux rendszerű számítógépére.</span><span class="sxs-lookup"><span data-stu-id="66c14-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="66c14-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="66c14-109">EXAMPLES</span></span>

## <span data-ttu-id="66c14-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66c14-110">PARAMETERS</span></span>

### <span data-ttu-id="66c14-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="66c14-111">-CounterNames</span></span>
<span data-ttu-id="66c14-112">A számlálók nevének tömbje.</span><span class="sxs-lookup"><span data-stu-id="66c14-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66c14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c14-113">-DefaultProfile</span></span>
<span data-ttu-id="66c14-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="66c14-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66c14-115">-Force</span><span class="sxs-lookup"><span data-stu-id="66c14-115">-Force</span></span>
<span data-ttu-id="66c14-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="66c14-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66c14-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="66c14-117">-InstanceName</span></span>
<span data-ttu-id="66c14-118">Egy példánynevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="66c14-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="66c14-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="66c14-119">-IntervalSeconds</span></span>
<span data-ttu-id="66c14-120">A gyűjtemény időközét adja meg.</span><span class="sxs-lookup"><span data-stu-id="66c14-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="66c14-121">-Name</span><span class="sxs-lookup"><span data-stu-id="66c14-121">-Name</span></span>
<span data-ttu-id="66c14-122">Megadja az adatforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="66c14-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="66c14-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="66c14-123">-ObjectName</span></span>
<span data-ttu-id="66c14-124">Egy objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="66c14-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="66c14-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c14-125">-ResourceGroupName</span></span>
<span data-ttu-id="66c14-126">Egy Linux rendszerű számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="66c14-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="66c14-127">-Workspace</span><span class="sxs-lookup"><span data-stu-id="66c14-127">-Workspace</span></span>
<span data-ttu-id="66c14-128">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="66c14-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="66c14-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="66c14-129">-WorkspaceName</span></span>
<span data-ttu-id="66c14-130">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="66c14-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="66c14-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66c14-131">-Confirm</span></span>
<span data-ttu-id="66c14-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="66c14-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66c14-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66c14-133">-WhatIf</span></span>
<span data-ttu-id="66c14-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="66c14-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66c14-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66c14-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66c14-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c14-136">CommonParameters</span></span>
<span data-ttu-id="66c14-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66c14-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c14-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66c14-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c14-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66c14-139">INPUTS</span></span>

### <span data-ttu-id="66c14-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="66c14-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="66c14-141">System.String</span><span class="sxs-lookup"><span data-stu-id="66c14-141">System.String</span></span>

### <span data-ttu-id="66c14-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="66c14-142">System.String[]</span></span>

### <span data-ttu-id="66c14-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="66c14-143">System.Int32</span></span>

## <span data-ttu-id="66c14-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66c14-144">OUTPUTS</span></span>

### <span data-ttu-id="66c14-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="66c14-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="66c14-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="66c14-146">NOTES</span></span>

## <span data-ttu-id="66c14-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66c14-147">RELATED LINKS</span></span>

[<span data-ttu-id="66c14-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="66c14-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="66c14-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="66c14-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


