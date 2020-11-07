---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 89aed8cb651fc5e11f6314df0ec74f3b4f9aa29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838454"
---
# <span data-ttu-id="24d81-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="24d81-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="24d81-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24d81-102">SYNOPSIS</span></span>
<span data-ttu-id="24d81-103">Begyűjti az eseménynaplókat a Windows operációs rendszert futtató számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="24d81-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="24d81-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24d81-104">SYNTAX</span></span>

### <span data-ttu-id="24d81-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24d81-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d81-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="24d81-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24d81-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="24d81-107">DESCRIPTION</span></span>
<span data-ttu-id="24d81-108">A **New-AzOperationalInsightsWindowsEventDataSource** parancsmag olyan adatforrást ad hozzá, amely a Windows-eseménynaplókat gyűjti össze olyan csatlakoztatott számítógépekről, amelyek a Windows operációs rendszert futtatják az Azure hadműveleti vizsgálatokban.</span><span class="sxs-lookup"><span data-stu-id="24d81-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="24d81-109">Példák</span><span class="sxs-lookup"><span data-stu-id="24d81-109">EXAMPLES</span></span>

### <span data-ttu-id="24d81-110">1. példa: a Windows rendszerbeli esemény-adatforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="24d81-110">Example 1: Create system Windows event data source</span></span>
```
$EventLogNames       = @()
$EventLogNames      += 'Directory Service'
$EventLogNames      += 'Microsoft-Windows-EventCollector/Operational'
$EventLogNames      += 'System'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($EventLogName in $EventLogNames) {
    $Count++
    $null = New-AzOperationalInsightsWindowsEventDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Windows-event-$($Count)" `
    -EventLogName $EventLogName `
    -CollectErrors `
    -CollectWarnings `
    -CollectInformation
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'WindowsEvent'
```

## <span data-ttu-id="24d81-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24d81-111">PARAMETERS</span></span>

### <span data-ttu-id="24d81-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="24d81-112">-CollectErrors</span></span>
<span data-ttu-id="24d81-113">Jelzi, hogy a műveleti elemzések hibaüzeneteket gyűjtenek.</span><span class="sxs-lookup"><span data-stu-id="24d81-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="24d81-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="24d81-114">-CollectInformation</span></span>
<span data-ttu-id="24d81-115">Jelzi, hogy az üzemi elemzések az információs üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="24d81-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="24d81-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="24d81-116">-CollectWarnings</span></span>
<span data-ttu-id="24d81-117">Jelzi, hogy a műveleti elemzések a figyelmeztető üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="24d81-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="24d81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d81-118">-DefaultProfile</span></span>
<span data-ttu-id="24d81-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="24d81-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24d81-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="24d81-120">-EventLogName</span></span>
<span data-ttu-id="24d81-121">Az Eseménynapló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="24d81-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="24d81-122">-Force</span><span class="sxs-lookup"><span data-stu-id="24d81-122">-Force</span></span>
<span data-ttu-id="24d81-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="24d81-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="24d81-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24d81-124">-Name</span></span>
<span data-ttu-id="24d81-125">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="24d81-125">Specifies a name for the data source.</span></span> <span data-ttu-id="24d81-126">A név nincs kitéve az Azure-portálon, és bármely karakterlánc használható mindaddig, amíg egyedi.</span><span class="sxs-lookup"><span data-stu-id="24d81-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="24d81-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d81-127">-ResourceGroupName</span></span>
<span data-ttu-id="24d81-128">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="24d81-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="24d81-129">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="24d81-129">-Workspace</span></span>
<span data-ttu-id="24d81-130">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="24d81-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="24d81-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="24d81-131">-WorkspaceName</span></span>
<span data-ttu-id="24d81-132">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="24d81-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="24d81-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24d81-133">-Confirm</span></span>
<span data-ttu-id="24d81-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24d81-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d81-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d81-135">-WhatIf</span></span>
<span data-ttu-id="24d81-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24d81-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24d81-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24d81-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d81-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d81-138">CommonParameters</span></span>
<span data-ttu-id="24d81-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24d81-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d81-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d81-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d81-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24d81-141">INPUTS</span></span>

### <span data-ttu-id="24d81-142">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="24d81-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="24d81-143">System. String</span><span class="sxs-lookup"><span data-stu-id="24d81-143">System.String</span></span>

## <span data-ttu-id="24d81-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24d81-144">OUTPUTS</span></span>

### <span data-ttu-id="24d81-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="24d81-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="24d81-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24d81-146">NOTES</span></span>

## <span data-ttu-id="24d81-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24d81-147">RELATED LINKS</span></span>
