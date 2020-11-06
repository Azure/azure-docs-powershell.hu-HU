---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 9abb97e5006f6572c7a0b08d8d25bcc55906a765
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496223"
---
# <span data-ttu-id="9b5b1-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="9b5b1-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="9b5b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b5b1-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5b1-103">Új Azure adatbázis-áttelepítési szolgáltatás projekt létrehozása</span><span class="sxs-lookup"><span data-stu-id="9b5b1-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b5b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b5b1-104">SYNTAX</span></span>

### <span data-ttu-id="9b5b1-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b5b1-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b5b1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b5b1-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b5b1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b5b1-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b5b1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b5b1-108">DESCRIPTION</span></span>
<span data-ttu-id="9b5b1-109">A New-AzureRmDataMigrationProject parancsmag új Azure adatbázis-áttelepítési szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="9b5b1-110">Ez a parancsmag minden szükséges paraméterben (például az Azure-erőforráscsoport nevében, az Azure adatáttelepítés-szolgáltatás nevében) található, amelyben létrejön az új projekt, a projekt létrehozásának helye, az új projekt egyedi neve, a forrás-és a cél kapcsolati objektuma, valamint a cél típusa objektum, az áttelepítendő adatbázisok listájának bemenete.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="9b5b1-111">A New-AzureRmDataMigrationConnectionInfo parancsmaggal új ConnectionInfo-objektumot hozhat létre a forrás-és a cél kapcsolatokhoz egyaránt.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="9b5b1-112">A Microsoft. Azure. Management. DataMigration. DatabaseInfo. models. a kijelölt adatbázisokra várható. ezt az objektumot New-AzureRmDataMigrationDatabaseInfo parancsmag használatával hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="9b5b1-113">Példák</span><span class="sxs-lookup"><span data-stu-id="9b5b1-113">EXAMPLES</span></span>

### <span data-ttu-id="9b5b1-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9b5b1-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="9b5b1-115">A fenti példa azt szemlélteti, hogy miként hozhat létre a MyDMSProject nevű új projektet a közép-amerikai régióban az Azure Database Migration Service instance nevű TestService nevű projektben.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="9b5b1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b5b1-116">PARAMETERS</span></span>

### <span data-ttu-id="9b5b1-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="9b5b1-117">-DatabaseInfo</span></span>
<span data-ttu-id="9b5b1-118">Adatbázis-infók.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5b1-119">-DefaultProfile</span></span>
<span data-ttu-id="9b5b1-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b5b1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b5b1-121">-InputObject</span></span>
<span data-ttu-id="9b5b1-122">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="9b5b1-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="9b5b1-123">-Location</span></span>
<span data-ttu-id="9b5b1-124">Az Azure adatbázis-áttelepítési szolgáltatás példányának helye.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9b5b1-125">-Name</span></span>
<span data-ttu-id="9b5b1-126">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b5b1-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b5b1-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b5b1-129">-ResourceId</span></span>
<span data-ttu-id="9b5b1-130">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-131">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="9b5b1-131">-ServiceName</span></span>
<span data-ttu-id="9b5b1-132">Az Azure adatbázis-áttelepítési szolgáltatás példányának neve.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-132">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="9b5b1-133">-SourceConnection</span></span>
<span data-ttu-id="9b5b1-134">Forrás-kapcsolódási adatok.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="9b5b1-135">-SourceType</span></span>
<span data-ttu-id="9b5b1-136">Source platform típusa projekthez.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-136">Source platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="9b5b1-137">-TargetConnection</span></span>
<span data-ttu-id="9b5b1-138">A cél kapcsolati adatai.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="9b5b1-139">-TargetType</span></span>
<span data-ttu-id="9b5b1-140">A projekt cél platformjának típusa.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-140">Target platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9b5b1-141">-Confirm</span></span>
<span data-ttu-id="9b5b1-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b5b1-143">-WhatIf</span></span>
<span data-ttu-id="9b5b1-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b5b1-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9b5b1-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5b1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5b1-146">CommonParameters</span></span>
<span data-ttu-id="9b5b1-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b5b1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5b1-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b5b1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5b1-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b5b1-149">INPUTS</span></span>

### <span data-ttu-id="9b5b1-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9b5b1-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="9b5b1-151">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b5b1-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9b5b1-152">System. String</span><span class="sxs-lookup"><span data-stu-id="9b5b1-152">System.String</span></span>

## <span data-ttu-id="9b5b1-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b5b1-153">OUTPUTS</span></span>

### <span data-ttu-id="9b5b1-154">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="9b5b1-154">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="9b5b1-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b5b1-155">NOTES</span></span>

## <span data-ttu-id="9b5b1-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b5b1-156">RELATED LINKS</span></span>
