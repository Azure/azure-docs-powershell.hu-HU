---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 12d9ff89ea87ae24d3817cdd3ec0b706582e4849
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010632"
---
# <span data-ttu-id="0f603-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="0f603-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="0f603-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f603-102">SYNOPSIS</span></span>
<span data-ttu-id="0f603-103">Adatforrást ad hozzá a linuxos számítógépekhez.</span><span class="sxs-lookup"><span data-stu-id="0f603-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="0f603-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f603-104">SYNTAX</span></span>

### <span data-ttu-id="0f603-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f603-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f603-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0f603-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f603-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f603-107">DESCRIPTION</span></span>
<span data-ttu-id="0f603-108">A **New-AzOperationalInsightsLinuxSyslogDataSource** parancsmag a syslog-adatforrást felveszi egy munkaterületen összekapcsolt linuxos számítógépekre.</span><span class="sxs-lookup"><span data-stu-id="0f603-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="0f603-109">Az Azure hadműveleti ismeretei a syslog-adatok gyűjtésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="0f603-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="0f603-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0f603-110">EXAMPLES</span></span>

### <span data-ttu-id="0f603-111">1. példa: syslog-adatforrások létrehozása</span><span class="sxs-lookup"><span data-stu-id="0f603-111">Example 1: Create syslog data sources</span></span>
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

## <span data-ttu-id="0f603-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f603-112">PARAMETERS</span></span>

### <span data-ttu-id="0f603-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="0f603-113">-CollectAlert</span></span>
<span data-ttu-id="0f603-114">Jelzi, hogy a műveleti elemzések begyűjtik a riasztási üzeneteket.</span><span class="sxs-lookup"><span data-stu-id="0f603-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="0f603-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="0f603-115">-CollectCritical</span></span>
<span data-ttu-id="0f603-116">Jelzi, hogy a műveletek a kritikus üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="0f603-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="0f603-117">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="0f603-117">-CollectDebug</span></span>
<span data-ttu-id="0f603-118">Jelzi, hogy a műveletek a hibakeresési üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="0f603-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="0f603-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="0f603-119">-CollectEmergency</span></span>
<span data-ttu-id="0f603-120">Jelzi, hogy a tevékenységi összefüggések a vészhelyzeti üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="0f603-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="0f603-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="0f603-121">-CollectError</span></span>
<span data-ttu-id="0f603-122">Jelzi, hogy a műveleti elemzések hibaüzeneteket gyűjtenek.</span><span class="sxs-lookup"><span data-stu-id="0f603-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="0f603-123">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="0f603-123">-CollectInformational</span></span>
<span data-ttu-id="0f603-124">Jelzi, hogy a műveleti elemzések gyűjtik az információs üzeneteket.</span><span class="sxs-lookup"><span data-stu-id="0f603-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="0f603-125">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="0f603-125">-CollectNotice</span></span>
<span data-ttu-id="0f603-126">Jelzi, hogy az üzemeltetési elemzések összegyűjtik az üzeneteket.</span><span class="sxs-lookup"><span data-stu-id="0f603-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="0f603-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="0f603-127">-CollectWarning</span></span>
<span data-ttu-id="0f603-128">Jelzi, hogy a syslog figyelmeztető üzeneteket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0f603-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="0f603-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f603-129">-DefaultProfile</span></span>
<span data-ttu-id="0f603-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0f603-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f603-131">-Létesítmény</span><span class="sxs-lookup"><span data-stu-id="0f603-131">-Facility</span></span>
<span data-ttu-id="0f603-132">Egy eszköz kódját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f603-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="0f603-133">-Force</span><span class="sxs-lookup"><span data-stu-id="0f603-133">-Force</span></span>
<span data-ttu-id="0f603-134">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0f603-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f603-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f603-135">-Name</span></span>
<span data-ttu-id="0f603-136">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f603-136">Specifies a name for the data source.</span></span> <span data-ttu-id="0f603-137">A név nincs kitéve az Azure-portálon, és bármely karakterlánc használható mindaddig, amíg egyedi.</span><span class="sxs-lookup"><span data-stu-id="0f603-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="0f603-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f603-138">-ResourceGroupName</span></span>
<span data-ttu-id="0f603-139">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f603-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="0f603-140">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="0f603-140">-Workspace</span></span>
<span data-ttu-id="0f603-141">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="0f603-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0f603-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0f603-142">-WorkspaceName</span></span>
<span data-ttu-id="0f603-143">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="0f603-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0f603-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f603-144">-Confirm</span></span>
<span data-ttu-id="0f603-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f603-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f603-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f603-146">-WhatIf</span></span>
<span data-ttu-id="0f603-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f603-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f603-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f603-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f603-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f603-149">CommonParameters</span></span>
<span data-ttu-id="0f603-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f603-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f603-151">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f603-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f603-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f603-152">INPUTS</span></span>

### <span data-ttu-id="0f603-153">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0f603-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="0f603-154">System. String</span><span class="sxs-lookup"><span data-stu-id="0f603-154">System.String</span></span>

## <span data-ttu-id="0f603-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f603-155">OUTPUTS</span></span>

### <span data-ttu-id="0f603-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0f603-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0f603-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f603-157">NOTES</span></span>

## <span data-ttu-id="0f603-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f603-158">RELATED LINKS</span></span>

[<span data-ttu-id="0f603-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="0f603-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="0f603-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="0f603-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


