---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5d7c10227876c2ee5b8eeab12623457be0f64aa8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468794"
---
# <span data-ttu-id="0a49f-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="0a49f-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="0a49f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a49f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a49f-103">Eseménynaplókat gyűjt a Windows operációs rendszert futtató számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="0a49f-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="0a49f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a49f-104">SYNTAX</span></span>

### <span data-ttu-id="0a49f-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a49f-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a49f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0a49f-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a49f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a49f-107">DESCRIPTION</span></span>
<span data-ttu-id="0a49f-108">A **New-AzOperationalInsightsWindowsEventDataSource** parancsmag hozzáad egy adatforrást, amely a Windows eseménynaplóit olyan csatlakoztatott számítógépekről gyűjti, amelyek a Windows operációs rendszert futtatják az Azure Operational Insights szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="0a49f-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="0a49f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a49f-109">EXAMPLES</span></span>

### <span data-ttu-id="0a49f-110">1. példa: Rendszer Windows-esemény adatforrásának létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a49f-110">Example 1: Create system Windows event data source</span></span>
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

## <span data-ttu-id="0a49f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a49f-111">PARAMETERS</span></span>

### <span data-ttu-id="0a49f-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="0a49f-112">-CollectErrors</span></span>
<span data-ttu-id="0a49f-113">Azt jelzi, hogy a Operational Insights hibaüzeneteket gyűjt.</span><span class="sxs-lookup"><span data-stu-id="0a49f-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="0a49f-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="0a49f-114">-CollectInformation</span></span>
<span data-ttu-id="0a49f-115">Azt jelzi, hogy a Operational Insights információs üzeneteket gyűjt.</span><span class="sxs-lookup"><span data-stu-id="0a49f-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="0a49f-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="0a49f-116">-CollectWarnings</span></span>
<span data-ttu-id="0a49f-117">Azt jelzi, hogy a Operational Insights figyelmeztető üzeneteket gyűjt.</span><span class="sxs-lookup"><span data-stu-id="0a49f-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="0a49f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a49f-118">-DefaultProfile</span></span>
<span data-ttu-id="0a49f-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0a49f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a49f-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="0a49f-120">-EventLogName</span></span>
<span data-ttu-id="0a49f-121">Az eseménynapló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a49f-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="0a49f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0a49f-122">-Force</span></span>
<span data-ttu-id="0a49f-123">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="0a49f-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a49f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0a49f-124">-Name</span></span>
<span data-ttu-id="0a49f-125">Megadja az adatforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="0a49f-125">Specifies a name for the data source.</span></span> <span data-ttu-id="0a49f-126">A név nem látható az Azure Portalon, és bármilyen karakterlánc használható, ha egyedi.</span><span class="sxs-lookup"><span data-stu-id="0a49f-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="0a49f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a49f-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a49f-128">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a49f-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="0a49f-129">-Workspace</span><span class="sxs-lookup"><span data-stu-id="0a49f-129">-Workspace</span></span>
<span data-ttu-id="0a49f-130">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="0a49f-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0a49f-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a49f-131">-WorkspaceName</span></span>
<span data-ttu-id="0a49f-132">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="0a49f-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0a49f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a49f-133">-Confirm</span></span>
<span data-ttu-id="0a49f-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0a49f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a49f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a49f-135">-WhatIf</span></span>
<span data-ttu-id="0a49f-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0a49f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a49f-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a49f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a49f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a49f-138">CommonParameters</span></span>
<span data-ttu-id="0a49f-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a49f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a49f-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a49f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a49f-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a49f-141">INPUTS</span></span>

### <span data-ttu-id="0a49f-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a49f-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="0a49f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0a49f-143">System.String</span></span>

## <span data-ttu-id="0a49f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a49f-144">OUTPUTS</span></span>

### <span data-ttu-id="0a49f-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0a49f-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0a49f-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a49f-146">NOTES</span></span>

## <span data-ttu-id="0a49f-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a49f-147">RELATED LINKS</span></span>
