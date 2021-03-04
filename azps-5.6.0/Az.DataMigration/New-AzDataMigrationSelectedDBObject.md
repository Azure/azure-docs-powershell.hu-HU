---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: c6e417ade1e411eaaa0b86f8f69ac6c17f228e91
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942617"
---
# <span data-ttu-id="e2382-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="e2382-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="e2382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2382-102">SYNOPSIS</span></span>
<span data-ttu-id="e2382-103">Létrehoz egy adatbázis-bemeneti objektumot, amely az áttelepítéshez szükséges forrás- és céladatbázisokkal kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e2382-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="e2382-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e2382-104">SYNTAX</span></span>

### <span data-ttu-id="e2382-105">MigrateSqlServerSqlDb (default)</span><span class="sxs-lookup"><span data-stu-id="e2382-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2382-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="e2382-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2382-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e2382-107">DESCRIPTION</span></span>
<span data-ttu-id="e2382-108">A New-AzDataMigrationSelectedDB parancsmag létrehoz egy adatbázis-információs objektumot, amely a forrás- és céladatbázisok, valamint a táblaleképezések adatait tartalmazza az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="e2382-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="e2382-109">Ez a parancsmag paraméterként használható a New-AzDataMigrationTask parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="e2382-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="e2382-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e2382-110">EXAMPLES</span></span>

### <span data-ttu-id="e2382-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e2382-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="e2382-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="e2382-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="e2382-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2382-113">PARAMETERS</span></span>

### <span data-ttu-id="e2382-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="e2382-114">-BackupFileShare</span></span>
<span data-ttu-id="e2382-115">Fájlmegosztás, amelyről az adatbázis forráskiszolgáló-adatbázisfájlja biztonsági mentése szükséges.</span><span class="sxs-lookup"><span data-stu-id="e2382-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="e2382-116">Ezzel a beállítással felülbírálhatja az egyes adatbázisok fájlmegosztási adatait.</span><span class="sxs-lookup"><span data-stu-id="e2382-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="e2382-117">A kiszolgáló teljes tartománynevét használja.</span><span class="sxs-lookup"><span data-stu-id="e2382-117">Use fully qualified domain name for the server.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.FileShare
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2382-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2382-118">-DefaultProfile</span></span>
<span data-ttu-id="e2382-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2382-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2382-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="e2382-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="e2382-121">Adatbázis beállítása csak olvashatóként az áttelepítés előtt</span><span class="sxs-lookup"><span data-stu-id="e2382-121">Set Database to readonly before migration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2382-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="e2382-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="e2382-123">Állítsa az áttelepítés típusát SQL Serverre SQL DB-áttelepítésre.</span><span class="sxs-lookup"><span data-stu-id="e2382-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2382-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="e2382-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="e2382-125">Állítsa át az áttelepítés típusát SQL Serverre SQL DB MI-áttelepítésre.</span><span class="sxs-lookup"><span data-stu-id="e2382-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2382-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2382-126">-SourceDatabaseName</span></span>
<span data-ttu-id="e2382-127">A forrásadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e2382-127">The name of the source database.</span></span>

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

### <span data-ttu-id="e2382-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="e2382-128">-TableMap</span></span>
<span data-ttu-id="e2382-129">mapping of source to target tables</span><span class="sxs-lookup"><span data-stu-id="e2382-129">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2382-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2382-130">-TargetDatabaseName</span></span>
<span data-ttu-id="e2382-131">A céladatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e2382-131">The name of the target database.</span></span>

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

### <span data-ttu-id="e2382-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2382-132">CommonParameters</span></span>
<span data-ttu-id="e2382-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2382-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2382-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2382-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2382-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2382-135">INPUTS</span></span>

### <span data-ttu-id="e2382-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span><span class="sxs-lookup"><span data-stu-id="e2382-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="e2382-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2382-137">OUTPUTS</span></span>

### <span data-ttu-id="e2382-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="e2382-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="e2382-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e2382-139">NOTES</span></span>

## <span data-ttu-id="e2382-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2382-140">RELATED LINKS</span></span>
