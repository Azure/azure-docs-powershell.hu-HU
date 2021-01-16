---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344622"
---
# <span data-ttu-id="ee049-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="ee049-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="ee049-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee049-102">SYNOPSIS</span></span>
<span data-ttu-id="ee049-103">A szinkronizálási helyzetnek megfelelő adatbázis-információs objektumot hoz létre az áttelepítési feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="ee049-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="ee049-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ee049-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee049-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ee049-105">DESCRIPTION</span></span>

<span data-ttu-id="ee049-106">A New-AzDataMigrationSyncSelectedDB parancsmag létrehoz egy, a szinkronizálási helyzetre jellemző adatbázis-információs objektumot, amely a forrás- és céladatbázisokkal kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ee049-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="ee049-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ee049-107">EXAMPLES</span></span>

### <span data-ttu-id="ee049-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ee049-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="ee049-109">Ez a példa létrehoz egy adatbázis metaadat-objektumát, amely leírja az adatbázis-áttelepítési beállításokat$DatabaseName adatbázis-$DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="ee049-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="ee049-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee049-110">PARAMETERS</span></span>

### <span data-ttu-id="ee049-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee049-111">-DefaultProfile</span></span>
<span data-ttu-id="ee049-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee049-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee049-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="ee049-113">-MigrationSetting</span></span>
<span data-ttu-id="ee049-114">Az áttelepítés működését finomhangoló áttelepítési beállítások</span><span class="sxs-lookup"><span data-stu-id="ee049-114">Migration settings which tune the migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee049-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ee049-115">-SchemaName</span></span>
<span data-ttu-id="ee049-116">Áttelepítenie kell a séma nevét</span><span class="sxs-lookup"><span data-stu-id="ee049-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="ee049-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee049-117">-SourceDatabaseName</span></span>
<span data-ttu-id="ee049-118">A forrásadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ee049-118">The name of the source database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee049-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="ee049-119">-SourceSetting</span></span>
<span data-ttu-id="ee049-120">Forrásbeállítások a forrás végpont áttelepítési viselkedésének finomhangolásához</span><span class="sxs-lookup"><span data-stu-id="ee049-120">Source settings to tune source endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee049-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="ee049-121">-TableMap</span></span>
<span data-ttu-id="ee049-122">Forrás hozzárendelése céltáblákhoz</span><span class="sxs-lookup"><span data-stu-id="ee049-122">Mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee049-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee049-123">-TargetDatabaseName</span></span>
<span data-ttu-id="ee049-124">A céladatbázis neve</span><span class="sxs-lookup"><span data-stu-id="ee049-124">The name of the target database</span></span>

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

### <span data-ttu-id="ee049-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="ee049-125">-TargetSetting</span></span>
<span data-ttu-id="ee049-126">Célbeállítások a cél végpont áttelepítési viselkedésének finomhangolásához</span><span class="sxs-lookup"><span data-stu-id="ee049-126">Target settings to tune target endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee049-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee049-127">CommonParameters</span></span>
<span data-ttu-id="ee049-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee049-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee049-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee049-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee049-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee049-130">INPUTS</span></span>

### <span data-ttu-id="ee049-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="ee049-131">None</span></span>

## <span data-ttu-id="ee049-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee049-132">OUTPUTS</span></span>

### <span data-ttu-id="ee049-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="ee049-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="ee049-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ee049-134">NOTES</span></span>

## <span data-ttu-id="ee049-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee049-135">RELATED LINKS</span></span>
