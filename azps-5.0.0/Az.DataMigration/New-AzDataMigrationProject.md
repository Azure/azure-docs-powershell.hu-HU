---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: beed4ef06d567250fefa8cef86da133447a9f20c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297641"
---
# <span data-ttu-id="3ecda-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="3ecda-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="3ecda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ecda-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecda-103">Új Azure adatbázis-áttelepítési szolgáltatás projekt létrehozása</span><span class="sxs-lookup"><span data-stu-id="3ecda-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="3ecda-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ecda-104">SYNTAX</span></span>

### <span data-ttu-id="3ecda-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ecda-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ecda-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ecda-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ecda-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ecda-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ecda-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ecda-108">DESCRIPTION</span></span>
<span data-ttu-id="3ecda-109">A New-AzDataMigrationProject parancsmag új Azure adatbázis-áttelepítési szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3ecda-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="3ecda-110">Ez a parancsmag minden szükséges paraméterben (például az Azure-erőforráscsoport nevében, az Azure adatáttelepítés-szolgáltatás nevében) található, amelyben létrejön az új projekt, a projekt létrehozásának helye, az új projekt egyedi neve, a forrás-és a cél kapcsolati objektuma, valamint a cél típusa objektum, az áttelepítendő adatbázisok listájának bemenete.</span><span class="sxs-lookup"><span data-stu-id="3ecda-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="3ecda-111">A New-AzDataMigrationConnectionInfo parancsmaggal új ConnectionInfo-objektumot hozhat létre a forrás-és a cél kapcsolatokhoz egyaránt.</span><span class="sxs-lookup"><span data-stu-id="3ecda-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="3ecda-112">A Microsoft. Azure. Management. DataMigration. DatabaseInfo. models. a kijelölt adatbázisokra várható. ezt az objektumot New-AzDataMigrationDatabaseInfo parancsmag használatával hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="3ecda-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="3ecda-113">Példák</span><span class="sxs-lookup"><span data-stu-id="3ecda-113">EXAMPLES</span></span>

### <span data-ttu-id="3ecda-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3ecda-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="3ecda-115">A fenti példa azt szemlélteti, hogy miként hozhat létre a MyDMSProject nevű új projektet a közép-amerikai régióban az Azure Database Migration Service instance nevű TestService nevű projektben.</span><span class="sxs-lookup"><span data-stu-id="3ecda-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="3ecda-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ecda-116">PARAMETERS</span></span>

### <span data-ttu-id="3ecda-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="3ecda-117">-DatabaseInfo</span></span>
<span data-ttu-id="3ecda-118">Adatbázis-infók.</span><span class="sxs-lookup"><span data-stu-id="3ecda-118">Database Infos.</span></span>

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

### <span data-ttu-id="3ecda-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ecda-119">-DefaultProfile</span></span>
<span data-ttu-id="3ecda-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ecda-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ecda-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ecda-121">-InputObject</span></span>
<span data-ttu-id="3ecda-122">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="3ecda-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="3ecda-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="3ecda-123">-Location</span></span>
<span data-ttu-id="3ecda-124">Az Azure adatbázis-áttelepítési szolgáltatás példányának helye.</span><span class="sxs-lookup"><span data-stu-id="3ecda-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="3ecda-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ecda-125">-Name</span></span>
<span data-ttu-id="3ecda-126">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="3ecda-126">The name of the project.</span></span>

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

### <span data-ttu-id="3ecda-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ecda-127">-ResourceGroupName</span></span>
<span data-ttu-id="3ecda-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3ecda-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="3ecda-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ecda-129">-ResourceId</span></span>
<span data-ttu-id="3ecda-130">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3ecda-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="3ecda-131">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="3ecda-131">-ServiceName</span></span>
<span data-ttu-id="3ecda-132">Az Azure adatbázis-áttelepítési szolgáltatás példányának neve.</span><span class="sxs-lookup"><span data-stu-id="3ecda-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="3ecda-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="3ecda-133">-SourceConnection</span></span>
<span data-ttu-id="3ecda-134">Forrás-kapcsolódási adatok.</span><span class="sxs-lookup"><span data-stu-id="3ecda-134">Source Connection Info.</span></span>

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

### <span data-ttu-id="3ecda-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="3ecda-135">-SourceType</span></span>
<span data-ttu-id="3ecda-136">Source platform típusa projekthez.</span><span class="sxs-lookup"><span data-stu-id="3ecda-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="3ecda-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="3ecda-137">-TargetConnection</span></span>
<span data-ttu-id="3ecda-138">A cél kapcsolati adatai.</span><span class="sxs-lookup"><span data-stu-id="3ecda-138">Target connection information.</span></span>

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

### <span data-ttu-id="3ecda-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="3ecda-139">-TargetType</span></span>
<span data-ttu-id="3ecda-140">A projekt cél platformjának típusa.</span><span class="sxs-lookup"><span data-stu-id="3ecda-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="3ecda-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ecda-141">-Confirm</span></span>
<span data-ttu-id="3ecda-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ecda-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ecda-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ecda-143">-WhatIf</span></span>
<span data-ttu-id="3ecda-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ecda-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ecda-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ecda-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ecda-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecda-146">CommonParameters</span></span>
<span data-ttu-id="3ecda-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ecda-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecda-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ecda-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecda-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ecda-149">INPUTS</span></span>

### <span data-ttu-id="3ecda-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3ecda-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="3ecda-151">System. String</span><span class="sxs-lookup"><span data-stu-id="3ecda-151">System.String</span></span>

## <span data-ttu-id="3ecda-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ecda-152">OUTPUTS</span></span>

### <span data-ttu-id="3ecda-153">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="3ecda-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="3ecda-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ecda-154">NOTES</span></span>

## <span data-ttu-id="3ecda-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ecda-155">RELATED LINKS</span></span>
