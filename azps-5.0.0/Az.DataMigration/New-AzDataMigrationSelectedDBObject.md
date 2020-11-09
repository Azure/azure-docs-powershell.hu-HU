---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297623"
---
# <span data-ttu-id="0fb16-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="0fb16-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="0fb16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fb16-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb16-103">Létrehoz egy adatbázis-beviteli objektumot, amely információt tartalmaz az áttelepítéshez szükséges forrás-és céladatbázis-adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="0fb16-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="0fb16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fb16-104">SYNTAX</span></span>

### <span data-ttu-id="0fb16-105">MigrateSqlServerSqlDb (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0fb16-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fb16-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="0fb16-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fb16-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fb16-107">DESCRIPTION</span></span>
<span data-ttu-id="0fb16-108">Az New-AzDataMigrationSelectedDB parancsmag létrehoz egy adatbázis-információt tartalmazó objektumot, amely információkat tartalmaz a forrás-és a céladatbázis, valamint a tábla megfeleltetéséről az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="0fb16-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="0fb16-109">Ezt a parancsmagot a New-AzDataMigrationTask parancsmag paraméterként használhatja.</span><span class="sxs-lookup"><span data-stu-id="0fb16-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="0fb16-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0fb16-110">EXAMPLES</span></span>

### <span data-ttu-id="0fb16-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0fb16-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="0fb16-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="0fb16-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="0fb16-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fb16-113">PARAMETERS</span></span>

### <span data-ttu-id="0fb16-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="0fb16-114">-BackupFileShare</span></span>
<span data-ttu-id="0fb16-115">A fájlmegosztás, ahová az adatbázis forrás-adatbázis-fájljait biztonsági másolatot kell készíteni.</span><span class="sxs-lookup"><span data-stu-id="0fb16-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="0fb16-116">Ezzel a beállítással felülbírálhatja az egyes adatbázisokban tárolt fájlmegosztás adatait.</span><span class="sxs-lookup"><span data-stu-id="0fb16-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="0fb16-117">A kiszolgáló teljesen minősített tartománynevét használja.</span><span class="sxs-lookup"><span data-stu-id="0fb16-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="0fb16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb16-118">-DefaultProfile</span></span>
<span data-ttu-id="0fb16-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fb16-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fb16-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="0fb16-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="0fb16-121">Az adatbázis írásvédett állapotba beállítása az áttelepítés előtt</span><span class="sxs-lookup"><span data-stu-id="0fb16-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="0fb16-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="0fb16-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="0fb16-123">Áttelepítési típus beállítása SQL Server-adatbázisba az SQL DB-áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="0fb16-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="0fb16-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="0fb16-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="0fb16-125">Áttelepítési típus beállítása SQL Server-re SQL DB MI áttelepítéssel.</span><span class="sxs-lookup"><span data-stu-id="0fb16-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="0fb16-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="0fb16-126">-SourceDatabaseName</span></span>
<span data-ttu-id="0fb16-127">A forrás-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0fb16-127">The name of the source database.</span></span>

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

### <span data-ttu-id="0fb16-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="0fb16-128">-TableMap</span></span>
<span data-ttu-id="0fb16-129">a forrás hozzárendelése a cél táblákhoz</span><span class="sxs-lookup"><span data-stu-id="0fb16-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="0fb16-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="0fb16-130">-TargetDatabaseName</span></span>
<span data-ttu-id="0fb16-131">A cél-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0fb16-131">The name of the target database.</span></span>

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

### <span data-ttu-id="0fb16-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb16-132">CommonParameters</span></span>
<span data-ttu-id="0fb16-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fb16-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb16-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fb16-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb16-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fb16-135">INPUTS</span></span>

### <span data-ttu-id="0fb16-136">Microsoft. Azure. Management. DataMigration. models. fájlmegosztásról</span><span class="sxs-lookup"><span data-stu-id="0fb16-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="0fb16-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fb16-137">OUTPUTS</span></span>

### <span data-ttu-id="0fb16-138">Microsoft. Azure. Management. DataMigration. models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="0fb16-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="0fb16-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fb16-139">NOTES</span></span>

## <span data-ttu-id="0fb16-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fb16-140">RELATED LINKS</span></span>
