---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4fb6a38ff9c79a16d150402d3a2e2be135e0c004
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351030"
---
# <span data-ttu-id="e4f63-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="e4f63-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="e4f63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4f63-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f63-103">Az Azure Log Analytics munkaterületén lekért adatforrások.</span><span class="sxs-lookup"><span data-stu-id="e4f63-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="e4f63-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4f63-104">SYNTAX</span></span>

### <span data-ttu-id="e4f63-105">ByWorkspaceNameByKind (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4f63-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4f63-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="e4f63-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4f63-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="e4f63-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4f63-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="e4f63-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4f63-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4f63-109">DESCRIPTION</span></span>
<span data-ttu-id="e4f63-110">A **Get-AzOperationalInsightsDataSource** parancsmag adatforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="e4f63-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="e4f63-111">Megadhatja a behozni kívánt adatforrást.</span><span class="sxs-lookup"><span data-stu-id="e4f63-111">You can specify a data source to get.</span></span>
<span data-ttu-id="e4f63-112">Az eredményeket az adatforrás fajtája alapján szűrheti.</span><span class="sxs-lookup"><span data-stu-id="e4f63-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="e4f63-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4f63-113">EXAMPLES</span></span>

## <span data-ttu-id="e4f63-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4f63-114">PARAMETERS</span></span>

### <span data-ttu-id="e4f63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f63-115">-DefaultProfile</span></span>
<span data-ttu-id="e4f63-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e4f63-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4f63-117">-Kind</span><span class="sxs-lookup"><span data-stu-id="e4f63-117">-Kind</span></span>
<span data-ttu-id="e4f63-118">A lekért adatforrások fajtáját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e4f63-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="e4f63-119">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="e4f63-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e4f63-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="e4f63-120">AzureActivityLog</span></span> 
- <span data-ttu-id="e4f63-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="e4f63-121">CustomLog</span></span> 
- <span data-ttu-id="e4f63-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="e4f63-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="e4f63-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="e4f63-123">LinuxSyslog</span></span> 
- <span data-ttu-id="e4f63-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="e4f63-124">WindowsEvent</span></span> 
- <span data-ttu-id="e4f63-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="e4f63-125">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f63-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e4f63-126">-Name</span></span>
<span data-ttu-id="e4f63-127">A lekért adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4f63-127">Specifies the name of a data source to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f63-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f63-128">-ResourceGroupName</span></span>
<span data-ttu-id="e4f63-129">Annak az erőforráscsoportnak a nevét adja meg, amely a behozni kívánt adatforrásokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e4f63-129">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f63-130">-Workspace</span><span class="sxs-lookup"><span data-stu-id="e4f63-130">-Workspace</span></span>
<span data-ttu-id="e4f63-131">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="e4f63-131">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f63-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e4f63-132">-WorkspaceName</span></span>
<span data-ttu-id="e4f63-133">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="e4f63-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f63-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f63-134">CommonParameters</span></span>
<span data-ttu-id="e4f63-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4f63-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f63-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4f63-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f63-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4f63-137">INPUTS</span></span>

### <span data-ttu-id="e4f63-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e4f63-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e4f63-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e4f63-139">System.String</span></span>

## <span data-ttu-id="e4f63-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4f63-140">OUTPUTS</span></span>

### <span data-ttu-id="e4f63-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e4f63-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e4f63-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4f63-142">NOTES</span></span>
* <span data-ttu-id="e4f63-143">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, műveleti, betekintések</span><span class="sxs-lookup"><span data-stu-id="e4f63-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="e4f63-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4f63-144">RELATED LINKS</span></span>

[<span data-ttu-id="e4f63-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="e4f63-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="e4f63-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="e4f63-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


