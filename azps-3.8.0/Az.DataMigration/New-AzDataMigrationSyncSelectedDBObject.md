---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845314"
---
# <span data-ttu-id="fbe48-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="fbe48-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="fbe48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbe48-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe48-103">Adatbázis-információ objektum létrehozása az áttelepítési feladathoz használt szinkronizálási forgatókönyvhez</span><span class="sxs-lookup"><span data-stu-id="fbe48-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="fbe48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbe48-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbe48-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbe48-105">DESCRIPTION</span></span>

<span data-ttu-id="fbe48-106">Az New-AzDataMigrationSyncSelectedDB parancsmag egy adatbázis-információ objektumra hivatkozik, amely a forrás-és a célként megadott adatbázisokkal kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fbe48-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="fbe48-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fbe48-107">EXAMPLES</span></span>

### <span data-ttu-id="fbe48-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fbe48-108">Example 1</span></span>
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

<span data-ttu-id="fbe48-109">Ez a példa létrehoz egy adatbázis metaadat-objektumot, amely leírja az $DatabaseName áttelepítési beállításait az adatbázis $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="fbe48-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="fbe48-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbe48-110">PARAMETERS</span></span>

### <span data-ttu-id="fbe48-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe48-111">-DefaultProfile</span></span>
<span data-ttu-id="fbe48-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbe48-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbe48-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="fbe48-113">-MigrationSetting</span></span>
<span data-ttu-id="fbe48-114">Az áttelepítési viselkedést beállító áttelepítési beállítások</span><span class="sxs-lookup"><span data-stu-id="fbe48-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="fbe48-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="fbe48-115">-SchemaName</span></span>
<span data-ttu-id="fbe48-116">Áttelepítendő séma neve</span><span class="sxs-lookup"><span data-stu-id="fbe48-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="fbe48-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbe48-117">-SourceDatabaseName</span></span>
<span data-ttu-id="fbe48-118">A forrás-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fbe48-118">The name of the source database.</span></span>

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

### <span data-ttu-id="fbe48-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="fbe48-119">-SourceSetting</span></span>
<span data-ttu-id="fbe48-120">Forrás beállításai a forrás-végpont áttelepítési viselkedésének finomhangolásához</span><span class="sxs-lookup"><span data-stu-id="fbe48-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="fbe48-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="fbe48-121">-TableMap</span></span>
<span data-ttu-id="fbe48-122">A forrás hozzárendelése a cél táblákhoz</span><span class="sxs-lookup"><span data-stu-id="fbe48-122">Mapping of source to target tables</span></span>

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

### <span data-ttu-id="fbe48-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbe48-123">-TargetDatabaseName</span></span>
<span data-ttu-id="fbe48-124">A céladatbázis neve</span><span class="sxs-lookup"><span data-stu-id="fbe48-124">The name of the target database</span></span>

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

### <span data-ttu-id="fbe48-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="fbe48-125">-TargetSetting</span></span>
<span data-ttu-id="fbe48-126">Cél beállításai a végpont áttelepítési viselkedésének finomhangolásához</span><span class="sxs-lookup"><span data-stu-id="fbe48-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="fbe48-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe48-127">CommonParameters</span></span>
<span data-ttu-id="fbe48-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbe48-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe48-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe48-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe48-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbe48-130">INPUTS</span></span>

### <span data-ttu-id="fbe48-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="fbe48-131">None</span></span>

## <span data-ttu-id="fbe48-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbe48-132">OUTPUTS</span></span>

### <span data-ttu-id="fbe48-133">Microsoft. Azure. Management. DataMigration. models. MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="fbe48-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="fbe48-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbe48-134">NOTES</span></span>

## <span data-ttu-id="fbe48-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbe48-135">RELATED LINKS</span></span>
