---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350417"
---
# <span data-ttu-id="4f698-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="4f698-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="4f698-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f698-102">SYNOPSIS</span></span>
<span data-ttu-id="4f698-103">Létrehoz egy adatbázis-bemeneti objektumot, amely az áttelepítéshez szükséges forrás- és céladatbázisokkal kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4f698-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="4f698-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4f698-104">SYNTAX</span></span>

### <span data-ttu-id="4f698-105">MigrateSqlServerSqlDb (default)</span><span class="sxs-lookup"><span data-stu-id="4f698-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f698-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="4f698-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f698-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4f698-107">DESCRIPTION</span></span>
<span data-ttu-id="4f698-108">A New-AzDataMigrationSelectedDB parancsmag létrehoz egy adatbázis-információs objektumot, amely a forrás- és céladatbázisok, valamint a táblaleképezések adatait tartalmazza az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="4f698-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="4f698-109">Ez a parancsmag paraméterként használható a New-AzDataMigrationTask parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="4f698-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="4f698-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4f698-110">EXAMPLES</span></span>

### <span data-ttu-id="4f698-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4f698-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="4f698-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="4f698-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="4f698-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f698-113">PARAMETERS</span></span>

### <span data-ttu-id="4f698-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="4f698-114">-BackupFileShare</span></span>
<span data-ttu-id="4f698-115">Fájlmegosztás, amelyről az adatbázis forráskiszolgáló-adatbázisfájlja biztonsági mentése szükséges.</span><span class="sxs-lookup"><span data-stu-id="4f698-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="4f698-116">Ezzel a beállítással felülbírálhatja az egyes adatbázisok fájlmegosztási adatait.</span><span class="sxs-lookup"><span data-stu-id="4f698-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="4f698-117">A kiszolgáló teljes tartománynevét használja.</span><span class="sxs-lookup"><span data-stu-id="4f698-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="4f698-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f698-118">-DefaultProfile</span></span>
<span data-ttu-id="4f698-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f698-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f698-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="4f698-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="4f698-121">Adatbázis beállítása csak olvashatóként az áttelepítés előtt</span><span class="sxs-lookup"><span data-stu-id="4f698-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="4f698-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="4f698-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="4f698-123">Állítsa az áttelepítés típusát SQL Serverre SQL DB-áttelepítésre.</span><span class="sxs-lookup"><span data-stu-id="4f698-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="4f698-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="4f698-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="4f698-125">Állítsa át az áttelepítés típusát SQL Serverre SQL DB MI-áttelepítésre.</span><span class="sxs-lookup"><span data-stu-id="4f698-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="4f698-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4f698-126">-SourceDatabaseName</span></span>
<span data-ttu-id="4f698-127">A forrásadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="4f698-127">The name of the source database.</span></span>

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

### <span data-ttu-id="4f698-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="4f698-128">-TableMap</span></span>
<span data-ttu-id="4f698-129">mapping of source to target tables</span><span class="sxs-lookup"><span data-stu-id="4f698-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="4f698-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4f698-130">-TargetDatabaseName</span></span>
<span data-ttu-id="4f698-131">A céladatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="4f698-131">The name of the target database.</span></span>

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

### <span data-ttu-id="4f698-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f698-132">CommonParameters</span></span>
<span data-ttu-id="4f698-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f698-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f698-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f698-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f698-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f698-135">INPUTS</span></span>

### <span data-ttu-id="4f698-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span><span class="sxs-lookup"><span data-stu-id="4f698-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="4f698-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f698-137">OUTPUTS</span></span>

### <span data-ttu-id="4f698-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="4f698-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="4f698-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4f698-139">NOTES</span></span>

## <span data-ttu-id="4f698-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f698-140">RELATED LINKS</span></span>
