---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4fb6a38ff9c79a16d150402d3a2e2be135e0c004
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846681"
---
# <span data-ttu-id="51fd0-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="51fd0-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="51fd0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="51fd0-103">Adatforrások beszerzése az Azure log Analytics-munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="51fd0-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="51fd0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51fd0-104">SYNTAX</span></span>

### <span data-ttu-id="51fd0-105">ByWorkspaceNameByKind (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51fd0-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51fd0-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="51fd0-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51fd0-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="51fd0-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51fd0-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="51fd0-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51fd0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="51fd0-109">DESCRIPTION</span></span>
<span data-ttu-id="51fd0-110">A **Get-AzOperationalInsightsDataSource** parancsmag adatforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="51fd0-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="51fd0-111">Megadhatja, hogy milyen adatforrás legyen elérhető.</span><span class="sxs-lookup"><span data-stu-id="51fd0-111">You can specify a data source to get.</span></span>
<span data-ttu-id="51fd0-112">Az eredményeket az adatforrás típusa alapján szűrheti.</span><span class="sxs-lookup"><span data-stu-id="51fd0-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="51fd0-113">Példák</span><span class="sxs-lookup"><span data-stu-id="51fd0-113">EXAMPLES</span></span>

## <span data-ttu-id="51fd0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51fd0-114">PARAMETERS</span></span>

### <span data-ttu-id="51fd0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51fd0-115">-DefaultProfile</span></span>
<span data-ttu-id="51fd0-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="51fd0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51fd0-117">-Kind</span><span class="sxs-lookup"><span data-stu-id="51fd0-117">-Kind</span></span>
<span data-ttu-id="51fd0-118">Megadja, hogy milyen típusú adatforrások legyenek.</span><span class="sxs-lookup"><span data-stu-id="51fd0-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="51fd0-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="51fd0-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="51fd0-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="51fd0-120">AzureActivityLog</span></span> 
- <span data-ttu-id="51fd0-121">Szokás</span><span class="sxs-lookup"><span data-stu-id="51fd0-121">CustomLog</span></span> 
- <span data-ttu-id="51fd0-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="51fd0-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="51fd0-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="51fd0-123">LinuxSyslog</span></span> 
- <span data-ttu-id="51fd0-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="51fd0-124">WindowsEvent</span></span> 
- <span data-ttu-id="51fd0-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="51fd0-125">WindowsPerformanceCounter</span></span>

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

### <span data-ttu-id="51fd0-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51fd0-126">-Name</span></span>
<span data-ttu-id="51fd0-127">A beolvasott adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51fd0-127">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="51fd0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51fd0-128">-ResourceGroupName</span></span>
<span data-ttu-id="51fd0-129">A beolvasott adatforrást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51fd0-129">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="51fd0-130">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="51fd0-130">-Workspace</span></span>
<span data-ttu-id="51fd0-131">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="51fd0-131">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="51fd0-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="51fd0-132">-WorkspaceName</span></span>
<span data-ttu-id="51fd0-133">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="51fd0-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="51fd0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51fd0-134">CommonParameters</span></span>
<span data-ttu-id="51fd0-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51fd0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51fd0-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51fd0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51fd0-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51fd0-137">INPUTS</span></span>

### <span data-ttu-id="51fd0-138">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="51fd0-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="51fd0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="51fd0-139">System.String</span></span>

## <span data-ttu-id="51fd0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51fd0-140">OUTPUTS</span></span>

### <span data-ttu-id="51fd0-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="51fd0-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="51fd0-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51fd0-142">NOTES</span></span>
* <span data-ttu-id="51fd0-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="51fd0-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="51fd0-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51fd0-144">RELATED LINKS</span></span>

[<span data-ttu-id="51fd0-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="51fd0-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="51fd0-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="51fd0-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


