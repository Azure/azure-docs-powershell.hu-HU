---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 5ba899cba4c45c3d13858d8e274b333d613106dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922658"
---
# <span data-ttu-id="58f34-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="58f34-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="58f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58f34-102">SYNOPSIS</span></span>
<span data-ttu-id="58f34-103">Geodundáns biztonsági másolatot készít egy adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="58f34-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="58f34-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58f34-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58f34-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58f34-105">DESCRIPTION</span></span>
<span data-ttu-id="58f34-106">A **Get-AzSqlDatabaseGeoBackup** parancsmag meghatározott georedundáns biztonsági másolatot kap egy SQL-adatbázisról vagy az összes rendelkezésre álló geodundáns biztonsági másolatról egy adott kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="58f34-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="58f34-107">A georedundáns biztonsági másolat egy különálló földrajzi helyről származó adatfájlokat használó visszaállítható erőforrás.</span><span class="sxs-lookup"><span data-stu-id="58f34-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="58f34-108">A Geo-Restore segítségével visszaállíthatja a georedundáns biztonsági másolatot, ha egy regionális kimaradás miatt az adatbázist visszaállítja egy új régióba.</span><span class="sxs-lookup"><span data-stu-id="58f34-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="58f34-109">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="58f34-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="58f34-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58f34-110">EXAMPLES</span></span>

### <span data-ttu-id="58f34-111">1. példa: Az összes georedundáns biztonsági másolat lekérte egy kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="58f34-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="58f34-112">Ez a parancs minden geodundáns biztonsági másolatot kap egy adott kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="58f34-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="58f34-113">2. példa: Meghatározott georedundáns biztonsági másolat készítése</span><span class="sxs-lookup"><span data-stu-id="58f34-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="58f34-114">Ez a parancs a ContosoDatabase nevű geodundáns biztonsági másolatot kapja az adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="58f34-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="58f34-115">3. példa: Az összes georedundáns biztonsági másolat lekérte egy kiszolgálón szűréssel</span><span class="sxs-lookup"><span data-stu-id="58f34-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="58f34-116">Ez a parancs minden földrajzi redundáns biztonsági másolatot kap egy adott kiszolgálóról, amely a "Contoso" kezdetű.</span><span class="sxs-lookup"><span data-stu-id="58f34-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="58f34-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58f34-117">PARAMETERS</span></span>

### <span data-ttu-id="58f34-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="58f34-118">-DatabaseName</span></span>
<span data-ttu-id="58f34-119">A lekért adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="58f34-119">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58f34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f34-120">-DefaultProfile</span></span>
<span data-ttu-id="58f34-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="58f34-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58f34-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58f34-122">-ResourceGroupName</span></span>
<span data-ttu-id="58f34-123">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az SQL-adatbázis-kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="58f34-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58f34-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="58f34-124">-ServerName</span></span>
<span data-ttu-id="58f34-125">Annak a kiszolgálónak a neve, amely a visszaállítható biztonsági másolatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="58f34-125">Specifies the name of the server that hosts the backup to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58f34-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58f34-126">-Confirm</span></span>
<span data-ttu-id="58f34-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="58f34-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f34-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58f34-128">-WhatIf</span></span>
<span data-ttu-id="58f34-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="58f34-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58f34-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58f34-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f34-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f34-131">CommonParameters</span></span>
<span data-ttu-id="58f34-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58f34-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f34-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58f34-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f34-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58f34-134">INPUTS</span></span>

### <span data-ttu-id="58f34-135">System.String</span><span class="sxs-lookup"><span data-stu-id="58f34-135">System.String</span></span>

## <span data-ttu-id="58f34-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58f34-136">OUTPUTS</span></span>

### <span data-ttu-id="58f34-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="58f34-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="58f34-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58f34-138">NOTES</span></span>

## <span data-ttu-id="58f34-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58f34-139">RELATED LINKS</span></span>

[<span data-ttu-id="58f34-140">Áttekintés: Felhőbeli üzletfolytonosság és adatbázis-katasztrófa-helyreállítás az SQL-adatbázissal</span><span class="sxs-lookup"><span data-stu-id="58f34-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="58f34-141">Azure SQL-adatbázis helyreállítása kimaradásból</span><span class="sxs-lookup"><span data-stu-id="58f34-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="58f34-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58f34-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="58f34-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="58f34-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
