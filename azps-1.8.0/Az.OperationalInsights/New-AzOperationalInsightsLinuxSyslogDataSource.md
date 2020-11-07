---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: a0268931d276c74560acd5cb04cac1d1e5778b81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669844"
---
# <span data-ttu-id="d4e36-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="d4e36-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="d4e36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4e36-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e36-103">Adatforrást ad hozzá a linuxos számítógépekhez.</span><span class="sxs-lookup"><span data-stu-id="d4e36-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="d4e36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4e36-104">SYNTAX</span></span>

### <span data-ttu-id="d4e36-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4e36-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e36-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d4e36-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e36-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4e36-107">DESCRIPTION</span></span>
<span data-ttu-id="d4e36-108">A **New-AzOperationalInsightsLinuxSyslogDataSource** parancsmag a syslog-adatforrást felveszi egy munkaterületen összekapcsolt linuxos számítógépekre.</span><span class="sxs-lookup"><span data-stu-id="d4e36-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="d4e36-109">Az Azure hadműveleti ismeretei a syslog-adatok gyűjtésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="d4e36-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="d4e36-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d4e36-110">EXAMPLES</span></span>

## <span data-ttu-id="d4e36-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4e36-111">PARAMETERS</span></span>

### <span data-ttu-id="d4e36-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="d4e36-112">-CollectAlert</span></span>
<span data-ttu-id="d4e36-113">Jelzi, hogy a műveleti elemzések begyűjtik a riasztási üzeneteket.</span><span class="sxs-lookup"><span data-stu-id="d4e36-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="d4e36-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="d4e36-114">-CollectCritical</span></span>
<span data-ttu-id="d4e36-115">Jelzi, hogy a műveletek a kritikus üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="d4e36-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="d4e36-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="d4e36-116">-CollectDebug</span></span>
<span data-ttu-id="d4e36-117">Jelzi, hogy a műveletek a hibakeresési üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="d4e36-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="d4e36-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="d4e36-118">-CollectEmergency</span></span>
<span data-ttu-id="d4e36-119">Jelzi, hogy a tevékenységi összefüggések a vészhelyzeti üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="d4e36-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="d4e36-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="d4e36-120">-CollectError</span></span>
<span data-ttu-id="d4e36-121">Jelzi, hogy a műveleti elemzések hibaüzeneteket gyűjtenek.</span><span class="sxs-lookup"><span data-stu-id="d4e36-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="d4e36-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="d4e36-122">-CollectInformational</span></span>
<span data-ttu-id="d4e36-123">Jelzi, hogy a műveleti elemzések gyűjtik az információs üzeneteket.</span><span class="sxs-lookup"><span data-stu-id="d4e36-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="d4e36-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="d4e36-124">-CollectNotice</span></span>
<span data-ttu-id="d4e36-125">Jelzi, hogy az üzemeltetési elemzések összegyűjtik az üzeneteket.</span><span class="sxs-lookup"><span data-stu-id="d4e36-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="d4e36-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="d4e36-126">-CollectWarning</span></span>
<span data-ttu-id="d4e36-127">Jelzi, hogy a syslog figyelmeztető üzeneteket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d4e36-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="d4e36-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e36-128">-DefaultProfile</span></span>
<span data-ttu-id="d4e36-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d4e36-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4e36-130">-Létesítmény</span><span class="sxs-lookup"><span data-stu-id="d4e36-130">-Facility</span></span>
<span data-ttu-id="d4e36-131">Egy eszköz kódját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4e36-131">Specifies a facility code.</span></span>

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

### <span data-ttu-id="d4e36-132">-Force</span><span class="sxs-lookup"><span data-stu-id="d4e36-132">-Force</span></span>
<span data-ttu-id="d4e36-133">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d4e36-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d4e36-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4e36-134">-Name</span></span>
<span data-ttu-id="d4e36-135">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4e36-135">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="d4e36-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e36-136">-ResourceGroupName</span></span>
<span data-ttu-id="d4e36-137">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4e36-137">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="d4e36-138">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="d4e36-138">-Workspace</span></span>
<span data-ttu-id="d4e36-139">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="d4e36-139">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d4e36-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d4e36-140">-WorkspaceName</span></span>
<span data-ttu-id="d4e36-141">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="d4e36-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d4e36-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4e36-142">-Confirm</span></span>
<span data-ttu-id="d4e36-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4e36-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e36-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e36-144">-WhatIf</span></span>
<span data-ttu-id="d4e36-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4e36-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e36-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4e36-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e36-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e36-147">CommonParameters</span></span>
<span data-ttu-id="d4e36-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4e36-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e36-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e36-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e36-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4e36-150">INPUTS</span></span>

### <span data-ttu-id="d4e36-151">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d4e36-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d4e36-152">System. String</span><span class="sxs-lookup"><span data-stu-id="d4e36-152">System.String</span></span>

## <span data-ttu-id="d4e36-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4e36-153">OUTPUTS</span></span>

### <span data-ttu-id="d4e36-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d4e36-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d4e36-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4e36-155">NOTES</span></span>

## <span data-ttu-id="d4e36-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4e36-156">RELATED LINKS</span></span>

[<span data-ttu-id="d4e36-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="d4e36-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="d4e36-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="d4e36-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


