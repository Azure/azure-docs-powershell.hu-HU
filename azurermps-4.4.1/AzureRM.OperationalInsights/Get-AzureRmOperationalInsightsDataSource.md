---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 61846456cfbff2dcbdaffba8c73a9bada87f07dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501699"
---
# <span data-ttu-id="a5947-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a5947-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="a5947-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5947-102">SYNOPSIS</span></span>
<span data-ttu-id="a5947-103">Adatforrások beszerzése az Azure log Analytics-munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="a5947-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5947-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5947-104">SYNTAX</span></span>

### <span data-ttu-id="a5947-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5947-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5947-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="a5947-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5947-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="a5947-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5947-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="a5947-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5947-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="a5947-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5947-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5947-110">DESCRIPTION</span></span>
<span data-ttu-id="a5947-111">A **Get-AzureRmOperationalInsightsDataSource** parancsmag adatforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="a5947-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="a5947-112">Megadhatja, hogy milyen adatforrás legyen elérhető.</span><span class="sxs-lookup"><span data-stu-id="a5947-112">You can specify a data source to get.</span></span>
<span data-ttu-id="a5947-113">Az eredményeket az adatforrás típusa alapján szűrheti.</span><span class="sxs-lookup"><span data-stu-id="a5947-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="a5947-114">Példák</span><span class="sxs-lookup"><span data-stu-id="a5947-114">EXAMPLES</span></span>

## <span data-ttu-id="a5947-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5947-115">PARAMETERS</span></span>

### <span data-ttu-id="a5947-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="a5947-116">-Kind</span></span>
<span data-ttu-id="a5947-117">Megadja, hogy milyen típusú adatforrások legyenek.</span><span class="sxs-lookup"><span data-stu-id="a5947-117">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="a5947-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a5947-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a5947-119">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="a5947-119">AzureActivityLog</span></span> 
- <span data-ttu-id="a5947-120">Szokás</span><span class="sxs-lookup"><span data-stu-id="a5947-120">CustomLog</span></span> 
- <span data-ttu-id="a5947-121">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="a5947-121">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="a5947-122">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="a5947-122">LinuxSyslog</span></span> 
- <span data-ttu-id="a5947-123">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="a5947-123">WindowsEvent</span></span> 
- <span data-ttu-id="a5947-124">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="a5947-124">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5947-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5947-125">-Name</span></span>
<span data-ttu-id="a5947-126">A beolvasott adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5947-126">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="a5947-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5947-127">-ResourceGroupName</span></span>
<span data-ttu-id="a5947-128">A beolvasott adatforrást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5947-128">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5947-129">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="a5947-129">-Workspace</span></span>
<span data-ttu-id="a5947-130">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="a5947-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a5947-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5947-131">-WorkspaceName</span></span>
<span data-ttu-id="a5947-132">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="a5947-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5947-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5947-133">-DefaultProfile</span></span>
<span data-ttu-id="a5947-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5947-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5947-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5947-135">CommonParameters</span></span>
<span data-ttu-id="a5947-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5947-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5947-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5947-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5947-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5947-138">INPUTS</span></span>

### <span data-ttu-id="a5947-139">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5947-139">PSWorkspace</span></span>
<span data-ttu-id="a5947-140">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a5947-140">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

### <span data-ttu-id="a5947-141">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5947-141">PSWorkspace</span></span>
<span data-ttu-id="a5947-142">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a5947-142">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="a5947-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5947-143">OUTPUTS</span></span>

### <span data-ttu-id="a5947-144">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span><span class="sxs-lookup"><span data-stu-id="a5947-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span></span>

### <span data-ttu-id="a5947-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a5947-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a5947-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5947-146">NOTES</span></span>
* <span data-ttu-id="a5947-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="a5947-147">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="a5947-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5947-148">RELATED LINKS</span></span>

[<span data-ttu-id="a5947-149">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a5947-149">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="a5947-150">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a5947-150">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


