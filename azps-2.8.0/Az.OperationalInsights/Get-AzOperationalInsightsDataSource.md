---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: f291eedade1a1a243f22dc618ffcc538a9158de6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838474"
---
# <span data-ttu-id="0c379-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0c379-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="0c379-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c379-102">SYNOPSIS</span></span>
<span data-ttu-id="0c379-103">Adatforrások beszerzése az Azure log Analytics-munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="0c379-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="0c379-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c379-104">SYNTAX</span></span>

### <span data-ttu-id="0c379-105">ByWorkspaceNameByKind (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c379-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c379-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="0c379-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c379-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="0c379-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c379-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="0c379-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c379-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c379-109">DESCRIPTION</span></span>
<span data-ttu-id="0c379-110">A **Get-AzOperationalInsightsDataSource** parancsmag adatforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="0c379-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="0c379-111">Megadhatja, hogy milyen adatforrás legyen elérhető.</span><span class="sxs-lookup"><span data-stu-id="0c379-111">You can specify a data source to get.</span></span>
<span data-ttu-id="0c379-112">Az eredményeket az adatforrás típusa alapján szűrheti.</span><span class="sxs-lookup"><span data-stu-id="0c379-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="0c379-113">Példák</span><span class="sxs-lookup"><span data-stu-id="0c379-113">EXAMPLES</span></span>

## <span data-ttu-id="0c379-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c379-114">PARAMETERS</span></span>

### <span data-ttu-id="0c379-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c379-115">-DefaultProfile</span></span>
<span data-ttu-id="0c379-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0c379-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c379-117">-Kind</span><span class="sxs-lookup"><span data-stu-id="0c379-117">-Kind</span></span>
<span data-ttu-id="0c379-118">Megadja, hogy milyen típusú adatforrások legyenek.</span><span class="sxs-lookup"><span data-stu-id="0c379-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="0c379-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0c379-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c379-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="0c379-120">AzureActivityLog</span></span> 
- <span data-ttu-id="0c379-121">Szokás</span><span class="sxs-lookup"><span data-stu-id="0c379-121">CustomLog</span></span> 
- <span data-ttu-id="0c379-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="0c379-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="0c379-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="0c379-123">LinuxSyslog</span></span> 
- <span data-ttu-id="0c379-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="0c379-124">WindowsEvent</span></span> 
- <span data-ttu-id="0c379-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="0c379-125">WindowsPerformanceCounter</span></span>

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

### <span data-ttu-id="0c379-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c379-126">-Name</span></span>
<span data-ttu-id="0c379-127">A beolvasott adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c379-127">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="0c379-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c379-128">-ResourceGroupName</span></span>
<span data-ttu-id="0c379-129">A beolvasott adatforrást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c379-129">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="0c379-130">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="0c379-130">-Workspace</span></span>
<span data-ttu-id="0c379-131">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="0c379-131">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0c379-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0c379-132">-WorkspaceName</span></span>
<span data-ttu-id="0c379-133">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="0c379-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0c379-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c379-134">CommonParameters</span></span>
<span data-ttu-id="0c379-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c379-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c379-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c379-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c379-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c379-137">INPUTS</span></span>

### <span data-ttu-id="0c379-138">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0c379-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="0c379-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0c379-139">System.String</span></span>

## <span data-ttu-id="0c379-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c379-140">OUTPUTS</span></span>

### <span data-ttu-id="0c379-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0c379-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0c379-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c379-142">NOTES</span></span>
* <span data-ttu-id="0c379-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="0c379-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="0c379-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c379-144">RELATED LINKS</span></span>

[<span data-ttu-id="0c379-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0c379-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="0c379-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0c379-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


