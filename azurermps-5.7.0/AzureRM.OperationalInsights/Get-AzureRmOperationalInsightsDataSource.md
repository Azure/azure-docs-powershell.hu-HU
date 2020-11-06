---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 057437e55fd7877154343bdbfc5f25d216412b8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496344"
---
# <span data-ttu-id="403da-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="403da-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="403da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="403da-102">SYNOPSIS</span></span>
<span data-ttu-id="403da-103">Adatforrások beszerzése az Azure log Analytics-munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="403da-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="403da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="403da-104">SYNTAX</span></span>

### <span data-ttu-id="403da-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="403da-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="403da-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="403da-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="403da-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="403da-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="403da-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="403da-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="403da-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="403da-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="403da-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="403da-110">DESCRIPTION</span></span>
<span data-ttu-id="403da-111">A **Get-AzureRmOperationalInsightsDataSource** parancsmag adatforrásokat kap.</span><span class="sxs-lookup"><span data-stu-id="403da-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="403da-112">Megadhatja, hogy milyen adatforrás legyen elérhető.</span><span class="sxs-lookup"><span data-stu-id="403da-112">You can specify a data source to get.</span></span>
<span data-ttu-id="403da-113">Az eredményeket az adatforrás típusa alapján szűrheti.</span><span class="sxs-lookup"><span data-stu-id="403da-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="403da-114">Példák</span><span class="sxs-lookup"><span data-stu-id="403da-114">EXAMPLES</span></span>

## <span data-ttu-id="403da-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="403da-115">PARAMETERS</span></span>

### <span data-ttu-id="403da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="403da-116">-DefaultProfile</span></span>
<span data-ttu-id="403da-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="403da-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="403da-118">-Kind</span><span class="sxs-lookup"><span data-stu-id="403da-118">-Kind</span></span>
<span data-ttu-id="403da-119">Megadja, hogy milyen típusú adatforrások legyenek.</span><span class="sxs-lookup"><span data-stu-id="403da-119">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="403da-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="403da-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="403da-121">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="403da-121">AzureActivityLog</span></span> 
- <span data-ttu-id="403da-122">Szokás</span><span class="sxs-lookup"><span data-stu-id="403da-122">CustomLog</span></span> 
- <span data-ttu-id="403da-123">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="403da-123">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="403da-124">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="403da-124">LinuxSyslog</span></span> 
- <span data-ttu-id="403da-125">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="403da-125">WindowsEvent</span></span> 
- <span data-ttu-id="403da-126">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="403da-126">WindowsPerformanceCounter</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="403da-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="403da-127">-Name</span></span>
<span data-ttu-id="403da-128">A beolvasott adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="403da-128">Specifies the name of a data source to get.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceObjectByName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="403da-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="403da-129">-ResourceGroupName</span></span>
<span data-ttu-id="403da-130">A beolvasott adatforrást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="403da-130">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="403da-131">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="403da-131">-Workspace</span></span>
<span data-ttu-id="403da-132">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="403da-132">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="403da-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="403da-133">-WorkspaceName</span></span>
<span data-ttu-id="403da-134">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="403da-134">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="403da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="403da-135">CommonParameters</span></span>
<span data-ttu-id="403da-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="403da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="403da-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="403da-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="403da-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="403da-138">INPUTS</span></span>

### <span data-ttu-id="403da-139">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="403da-139">PSWorkspace</span></span>
<span data-ttu-id="403da-140">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="403da-140">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

### <span data-ttu-id="403da-141">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="403da-141">PSWorkspace</span></span>
<span data-ttu-id="403da-142">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="403da-142">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="403da-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="403da-143">OUTPUTS</span></span>

### <span data-ttu-id="403da-144">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span><span class="sxs-lookup"><span data-stu-id="403da-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span></span>

### <span data-ttu-id="403da-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="403da-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="403da-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="403da-146">NOTES</span></span>
* <span data-ttu-id="403da-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="403da-147">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="403da-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="403da-148">RELATED LINKS</span></span>

[<span data-ttu-id="403da-149">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="403da-149">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="403da-150">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="403da-150">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


