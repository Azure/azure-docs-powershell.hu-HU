---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 12d9ff89ea87ae24d3817cdd3ec0b706582e4849
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481055"
---
# <span data-ttu-id="c73b0-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="c73b0-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="c73b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c73b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c73b0-103">Hozzáad egy adatforrást Linux rendszerű számítógépekhez.</span><span class="sxs-lookup"><span data-stu-id="c73b0-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="c73b0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c73b0-104">SYNTAX</span></span>

### <span data-ttu-id="c73b0-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c73b0-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c73b0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c73b0-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c73b0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c73b0-107">DESCRIPTION</span></span>
<span data-ttu-id="c73b0-108">A **New-AzOperationalInsightsLinuxSyslogDataSource** parancsmag hozzáad egy syslog adatforrást a csatlakoztatott Linux számítógépekhez egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="c73b0-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="c73b0-109">Az Azure Operational Insights képes syslog adatok gyűjtésére.</span><span class="sxs-lookup"><span data-stu-id="c73b0-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="c73b0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c73b0-110">EXAMPLES</span></span>

### <span data-ttu-id="c73b0-111">1. példa: Syslog adatforrások létrehozása</span><span class="sxs-lookup"><span data-stu-id="c73b0-111">Example 1: Create syslog data sources</span></span>
```
$FacilityNames       = @()
$FacilityNames      += 'auth'
$FacilityNames      += 'authpriv'
$FacilityNames      += 'cron'
$FacilityNames      += 'daemon'
$FacilityNames      += 'ftp'
$FacilityNames      += 'kern'
$FacilityNames      += 'mail'
$FacilityNames      += 'syslog'
$FacilityNames      += 'user'
$FacilityNames      += 'uucp'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($FacilityName in $FacilityNames) {
    $Count++
    $null = New-AzOperationalInsightsLinuxSyslogDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Linux-syslog-$($Count)" `
    -Facility $FacilityName `
    -CollectEmergency `
    -CollectAlert `
    -CollectCritical `
    -CollectError `
    -CollectWarning `
    -CollectNotice `
    -CollectDebug `
    -CollectInformational
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'LinuxSyslog'
```

## <span data-ttu-id="c73b0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c73b0-112">PARAMETERS</span></span>

### <span data-ttu-id="c73b0-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="c73b0-113">-CollectAlert</span></span>
<span data-ttu-id="c73b0-114">Azt jelzi, hogy a Operational Insights riasztási üzeneteket gyűjt.</span><span class="sxs-lookup"><span data-stu-id="c73b0-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="c73b0-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="c73b0-115">-CollectCritical</span></span>
<span data-ttu-id="c73b0-116">Azt jelzi, hogy a Operational Insights összegyűjti a kritikus üzeneteket.</span><span class="sxs-lookup"><span data-stu-id="c73b0-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="c73b0-117">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="c73b0-117">-CollectDebug</span></span>
<span data-ttu-id="c73b0-118">Azt jelzi, hogy a Operational Insights hibakeresési üzeneteket gyűjt.</span><span class="sxs-lookup"><span data-stu-id="c73b0-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="c73b0-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="c73b0-119">-CollectEmergency</span></span>
<span data-ttu-id="c73b0-120">Azt jelzi, hogy a Operational Insights segélyhívási üzeneteket gyűjt.</span><span class="sxs-lookup"><span data-stu-id="c73b0-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="c73b0-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="c73b0-121">-CollectError</span></span>
<span data-ttu-id="c73b0-122">Azt jelzi, hogy a Operational Insights hibaüzeneteket gyűjt.</span><span class="sxs-lookup"><span data-stu-id="c73b0-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="c73b0-123">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="c73b0-123">-CollectInformational</span></span>
<span data-ttu-id="c73b0-124">Azt jelzi, hogy a Operational Insights információs üzeneteket gyűjt.</span><span class="sxs-lookup"><span data-stu-id="c73b0-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="c73b0-125">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="c73b0-125">-CollectNotice</span></span>
<span data-ttu-id="c73b0-126">Azt jelzi, hogy a Operational Insights értesítéseket gyűjt.</span><span class="sxs-lookup"><span data-stu-id="c73b0-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="c73b0-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="c73b0-127">-CollectWarning</span></span>
<span data-ttu-id="c73b0-128">Azt jelzi, hogy a syslog figyelmeztető üzeneteket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="c73b0-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="c73b0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c73b0-129">-DefaultProfile</span></span>
<span data-ttu-id="c73b0-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c73b0-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c73b0-131">- Raktáron</span><span class="sxs-lookup"><span data-stu-id="c73b0-131">-Facility</span></span>
<span data-ttu-id="c73b0-132">A létesítmény kódját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c73b0-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="c73b0-133">-Force</span><span class="sxs-lookup"><span data-stu-id="c73b0-133">-Force</span></span>
<span data-ttu-id="c73b0-134">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="c73b0-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c73b0-135">-Name</span><span class="sxs-lookup"><span data-stu-id="c73b0-135">-Name</span></span>
<span data-ttu-id="c73b0-136">Megadja az adatforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="c73b0-136">Specifies a name for the data source.</span></span> <span data-ttu-id="c73b0-137">A név nem látható az Azure Portalon, és bármilyen karakterlánc használható, ha egyedi.</span><span class="sxs-lookup"><span data-stu-id="c73b0-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="c73b0-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c73b0-138">-ResourceGroupName</span></span>
<span data-ttu-id="c73b0-139">Egy Linux rendszerű számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c73b0-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="c73b0-140">-Workspace</span><span class="sxs-lookup"><span data-stu-id="c73b0-140">-Workspace</span></span>
<span data-ttu-id="c73b0-141">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="c73b0-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c73b0-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c73b0-142">-WorkspaceName</span></span>
<span data-ttu-id="c73b0-143">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="c73b0-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c73b0-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c73b0-144">-Confirm</span></span>
<span data-ttu-id="c73b0-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c73b0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c73b0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c73b0-146">-WhatIf</span></span>
<span data-ttu-id="c73b0-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c73b0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c73b0-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c73b0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c73b0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c73b0-149">CommonParameters</span></span>
<span data-ttu-id="c73b0-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c73b0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c73b0-151">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c73b0-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c73b0-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c73b0-152">INPUTS</span></span>

### <span data-ttu-id="c73b0-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c73b0-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c73b0-154">System.String</span><span class="sxs-lookup"><span data-stu-id="c73b0-154">System.String</span></span>

## <span data-ttu-id="c73b0-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c73b0-155">OUTPUTS</span></span>

### <span data-ttu-id="c73b0-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c73b0-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c73b0-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c73b0-157">NOTES</span></span>

## <span data-ttu-id="c73b0-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c73b0-158">RELATED LINKS</span></span>

[<span data-ttu-id="c73b0-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="c73b0-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="c73b0-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="c73b0-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


