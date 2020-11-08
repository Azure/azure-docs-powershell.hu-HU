---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 656d25e69e2739df7e196ba9e584c3890bf4028f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186040"
---
# <span data-ttu-id="e70a5-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="e70a5-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="e70a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e70a5-102">SYNOPSIS</span></span>
<span data-ttu-id="e70a5-103">Teljesítményszámlálókat ad hozzá a munkaterületek minden linuxos számítógépéhez.</span><span class="sxs-lookup"><span data-stu-id="e70a5-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="e70a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e70a5-104">SYNTAX</span></span>

### <span data-ttu-id="e70a5-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e70a5-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e70a5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e70a5-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e70a5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e70a5-107">DESCRIPTION</span></span>
<span data-ttu-id="e70a5-108">A **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** parancsmag olyan teljesítményszámlálókat ad eredményül, amelyekben az Azure-műveletek a munkaterületek összes linuxos számítógépére gyűjtik az adatokat.</span><span class="sxs-lookup"><span data-stu-id="e70a5-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="e70a5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e70a5-109">EXAMPLES</span></span>

## <span data-ttu-id="e70a5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e70a5-110">PARAMETERS</span></span>

### <span data-ttu-id="e70a5-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="e70a5-111">-CounterNames</span></span>
<span data-ttu-id="e70a5-112">A számlálók neveinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e70a5-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="e70a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70a5-113">-DefaultProfile</span></span>
<span data-ttu-id="e70a5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e70a5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e70a5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e70a5-115">-Force</span></span>
<span data-ttu-id="e70a5-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e70a5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e70a5-117">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="e70a5-117">-InstanceName</span></span>
<span data-ttu-id="e70a5-118">A példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e70a5-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="e70a5-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="e70a5-119">-IntervalSeconds</span></span>
<span data-ttu-id="e70a5-120">A gyűjtemény intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e70a5-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="e70a5-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e70a5-121">-Name</span></span>
<span data-ttu-id="e70a5-122">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e70a5-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="e70a5-123">-Objektumnév</span><span class="sxs-lookup"><span data-stu-id="e70a5-123">-ObjectName</span></span>
<span data-ttu-id="e70a5-124">Az objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e70a5-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="e70a5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e70a5-125">-ResourceGroupName</span></span>
<span data-ttu-id="e70a5-126">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e70a5-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="e70a5-127">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="e70a5-127">-Workspace</span></span>
<span data-ttu-id="e70a5-128">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="e70a5-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e70a5-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e70a5-129">-WorkspaceName</span></span>
<span data-ttu-id="e70a5-130">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="e70a5-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e70a5-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e70a5-131">-Confirm</span></span>
<span data-ttu-id="e70a5-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e70a5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e70a5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e70a5-133">-WhatIf</span></span>
<span data-ttu-id="e70a5-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e70a5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e70a5-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e70a5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e70a5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70a5-136">CommonParameters</span></span>
<span data-ttu-id="e70a5-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e70a5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70a5-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e70a5-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70a5-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e70a5-139">INPUTS</span></span>

### <span data-ttu-id="e70a5-140">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e70a5-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e70a5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e70a5-141">System.String</span></span>

### <span data-ttu-id="e70a5-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="e70a5-142">System.String[]</span></span>

### <span data-ttu-id="e70a5-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e70a5-143">System.Int32</span></span>

## <span data-ttu-id="e70a5-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e70a5-144">OUTPUTS</span></span>

### <span data-ttu-id="e70a5-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e70a5-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e70a5-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e70a5-146">NOTES</span></span>

## <span data-ttu-id="e70a5-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e70a5-147">RELATED LINKS</span></span>

[<span data-ttu-id="e70a5-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e70a5-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="e70a5-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e70a5-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


