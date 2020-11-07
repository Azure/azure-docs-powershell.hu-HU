---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 6372abc324601761c07ec4c69d52db188172ba0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669846"
---
# <span data-ttu-id="7a9b4-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="7a9b4-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="7a9b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a9b4-102">SYNOPSIS</span></span>
<span data-ttu-id="7a9b4-103">Teljesítményszámlálókat ad hozzá a munkaterületek minden linuxos számítógépéhez.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="7a9b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a9b4-104">SYNTAX</span></span>

### <span data-ttu-id="7a9b4-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7a9b4-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a9b4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7a9b4-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a9b4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a9b4-107">DESCRIPTION</span></span>
<span data-ttu-id="7a9b4-108">A **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** parancsmag olyan teljesítményszámlálókat ad eredményül, amelyekben az Azure-műveletek a munkaterületek összes linuxos számítógépére gyűjtik az adatokat.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="7a9b4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7a9b4-109">EXAMPLES</span></span>

## <span data-ttu-id="7a9b4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a9b4-110">PARAMETERS</span></span>

### <span data-ttu-id="7a9b4-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="7a9b4-111">-CounterNames</span></span>
<span data-ttu-id="7a9b4-112">A számlálók neveinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="7a9b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a9b4-113">-DefaultProfile</span></span>
<span data-ttu-id="7a9b4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7a9b4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a9b4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a9b4-115">-Force</span></span>
<span data-ttu-id="7a9b4-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a9b4-117">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="7a9b4-117">-InstanceName</span></span>
<span data-ttu-id="7a9b4-118">A példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="7a9b4-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="7a9b4-119">-IntervalSeconds</span></span>
<span data-ttu-id="7a9b4-120">A gyűjtemény intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="7a9b4-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7a9b4-121">-Name</span></span>
<span data-ttu-id="7a9b4-122">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="7a9b4-123">-Objektumnév</span><span class="sxs-lookup"><span data-stu-id="7a9b4-123">-ObjectName</span></span>
<span data-ttu-id="7a9b4-124">Az objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="7a9b4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a9b4-125">-ResourceGroupName</span></span>
<span data-ttu-id="7a9b4-126">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="7a9b4-127">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="7a9b4-127">-Workspace</span></span>
<span data-ttu-id="7a9b4-128">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7a9b4-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7a9b4-129">-WorkspaceName</span></span>
<span data-ttu-id="7a9b4-130">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7a9b4-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7a9b4-131">-Confirm</span></span>
<span data-ttu-id="7a9b4-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a9b4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a9b4-133">-WhatIf</span></span>
<span data-ttu-id="7a9b4-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a9b4-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a9b4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a9b4-136">CommonParameters</span></span>
<span data-ttu-id="7a9b4-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a9b4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a9b4-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a9b4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a9b4-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a9b4-139">INPUTS</span></span>

### <span data-ttu-id="7a9b4-140">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7a9b4-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7a9b4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7a9b4-141">System.String</span></span>

### <span data-ttu-id="7a9b4-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="7a9b4-142">System.String[]</span></span>

### <span data-ttu-id="7a9b4-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7a9b4-143">System.Int32</span></span>

## <span data-ttu-id="7a9b4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a9b4-144">OUTPUTS</span></span>

### <span data-ttu-id="7a9b4-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7a9b4-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7a9b4-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a9b4-146">NOTES</span></span>

## <span data-ttu-id="7a9b4-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a9b4-147">RELATED LINKS</span></span>

[<span data-ttu-id="7a9b4-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="7a9b4-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="7a9b4-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="7a9b4-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


