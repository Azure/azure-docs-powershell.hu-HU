---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 99884c23ff99287deb721e3cb76871766cdfa7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503772"
---
# <span data-ttu-id="fbd93-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="fbd93-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="fbd93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbd93-102">SYNOPSIS</span></span>
<span data-ttu-id="fbd93-103">Új Azure adatbázis-áttelepítési szolgáltatás projekt létrehozása</span><span class="sxs-lookup"><span data-stu-id="fbd93-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbd93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbd93-104">SYNTAX</span></span>

### <span data-ttu-id="fbd93-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fbd93-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform>
 [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fbd93-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbd93-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fbd93-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbd93-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="fbd93-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbd93-108">DESCRIPTION</span></span>
<span data-ttu-id="fbd93-109">A New-AzureRmDataMigrationProject parancsmag új Azure adatbázis-áttelepítési szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fbd93-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="fbd93-110">Ez a parancsmag minden szükséges paraméterben (például az Azure-erőforráscsoport nevében, az Azure adatáttelepítés-szolgáltatás nevében) található, amelyben létrejön az új projekt, a projekt létrehozásának helye, az új projekt egyedi neve, a forrás-és a cél kapcsolati objektuma, valamint a cél típusa objektum, az áttelepítendő adatbázisok listájának bemenete.</span><span class="sxs-lookup"><span data-stu-id="fbd93-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="fbd93-111">A New-AzureRmDataMigrationConnectionInfo parancsmaggal új ConnectionInfo-objektumot hozhat létre a forrás-és a cél kapcsolatokhoz egyaránt.</span><span class="sxs-lookup"><span data-stu-id="fbd93-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="fbd93-112">A Microsoft. Azure. Management. DataMigration. DatabaseInfo. models. a kijelölt adatbázisokra várható. ezt az objektumot New-AzureRmDataMigrationDatabaseInfo parancsmag használatával hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="fbd93-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="fbd93-113">Példák</span><span class="sxs-lookup"><span data-stu-id="fbd93-113">EXAMPLES</span></span>

### <span data-ttu-id="fbd93-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fbd93-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="fbd93-115">A fenti példa azt szemlélteti, hogy miként hozhat létre a MyDMSProject nevű új projektet a közép-amerikai régióban az Azure Database Migration Service instance nevű TestService nevű projektben.</span><span class="sxs-lookup"><span data-stu-id="fbd93-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>



## <span data-ttu-id="fbd93-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbd93-116">PARAMETERS</span></span>

### <span data-ttu-id="fbd93-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fbd93-117">-Confirm</span></span>
<span data-ttu-id="fbd93-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fbd93-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd93-119">-DatabaseInfo[]</span><span class="sxs-lookup"><span data-stu-id="fbd93-119">-DatabaseInfo[]</span></span>
<span data-ttu-id="fbd93-120">Adatbázis adatai</span><span class="sxs-lookup"><span data-stu-id="fbd93-120">Database information</span></span>

```yaml
Type: DatabaseInfo[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd93-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbd93-121">-DefaultProfile</span></span>
<span data-ttu-id="fbd93-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbd93-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbd93-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="fbd93-123">-Location</span></span>
<span data-ttu-id="fbd93-124">Az Azure adatbázis-áttelepítési szolgáltatás példányának helye.</span><span class="sxs-lookup"><span data-stu-id="fbd93-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd93-125">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="fbd93-125">-ProjectName</span></span>
<span data-ttu-id="fbd93-126">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="fbd93-126">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd93-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbd93-127">-ResourceGroupName</span></span>
<span data-ttu-id="fbd93-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fbd93-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd93-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="fbd93-129">-ServiceName</span></span>
<span data-ttu-id="fbd93-130">Az Azure adatbázis-áttelepítési szolgáltatás példányának neve.</span><span class="sxs-lookup"><span data-stu-id="fbd93-130">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd93-131">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="fbd93-131">-SourceConnection</span></span>
<span data-ttu-id="fbd93-132">Forrás-kapcsolódási adatok.</span><span class="sxs-lookup"><span data-stu-id="fbd93-132">Source Connection Info.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd93-133">-SourceType</span><span class="sxs-lookup"><span data-stu-id="fbd93-133">-SourceType</span></span>
<span data-ttu-id="fbd93-134">Source platform típusa projekthez.</span><span class="sxs-lookup"><span data-stu-id="fbd93-134">Source platform type for project.</span></span>

```yaml
Type: ProjectSourcePlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd93-135">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="fbd93-135">-TargetConnection</span></span>
<span data-ttu-id="fbd93-136">A cél kapcsolati adatai.</span><span class="sxs-lookup"><span data-stu-id="fbd93-136">Target connection information.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd93-137">-TargetType</span><span class="sxs-lookup"><span data-stu-id="fbd93-137">-TargetType</span></span>
<span data-ttu-id="fbd93-138">A projekt cél platformjának típusa.</span><span class="sxs-lookup"><span data-stu-id="fbd93-138">Target platform type for project.</span></span>

```yaml
Type: ProjectTargetPlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="fbd93-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbd93-139">OUTPUTS</span></span>

### <span data-ttu-id="fbd93-140">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="fbd93-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>


## <span data-ttu-id="fbd93-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbd93-141">NOTES</span></span>

## <span data-ttu-id="fbd93-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbd93-142">RELATED LINKS</span></span>

