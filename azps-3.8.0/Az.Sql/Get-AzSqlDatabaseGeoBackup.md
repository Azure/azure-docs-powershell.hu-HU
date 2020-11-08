---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011551"
---
# <span data-ttu-id="0d513-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="0d513-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="0d513-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d513-102">SYNOPSIS</span></span>
<span data-ttu-id="0d513-103">Egy adatbázis geo-redundáns biztonsági másolatát kapja.</span><span class="sxs-lookup"><span data-stu-id="0d513-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="0d513-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d513-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d513-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d513-105">DESCRIPTION</span></span>
<span data-ttu-id="0d513-106">A **Get-AzSqlDatabaseGeoBackup** PARANCSMAG egy SQL-adatbázis meghatározott geo-redundáns biztonsági másolatát kapja, vagy az összes rendelkezésre álló geo-redundáns biztonsági mentést egy adott kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="0d513-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="0d513-107">A Geo-redundáns biztonsági másolat egy helyreállítható erőforrás, amely külön földrajzi helyről származó adatfájlokat használ.</span><span class="sxs-lookup"><span data-stu-id="0d513-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="0d513-108">A Geo-Restore segítségével visszaállíthatja a Geo-redundáns biztonsági másolatot az adatbázis új területre való visszaállításához regionális leállás esetén.</span><span class="sxs-lookup"><span data-stu-id="0d513-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="0d513-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="0d513-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0d513-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0d513-110">EXAMPLES</span></span>

### <span data-ttu-id="0d513-111">Példa 1: minden geo-redundáns biztonsági másolat beolvasása a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="0d513-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="0d513-112">Ez a parancs a megadott kiszolgálón elérhető geo-redundáns biztonsági másolatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0d513-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="0d513-113">2. példa: meghatározott geo-redundáns biztonsági másolat beszerzése</span><span class="sxs-lookup"><span data-stu-id="0d513-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="0d513-114">Ez a parancs a ContosoDatabase nevű adatbázis geo-redundáns biztonsági másolatát kapja.</span><span class="sxs-lookup"><span data-stu-id="0d513-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="0d513-115">3. példa: minden geo-redundáns biztonsági másolat beolvasása a kiszolgálón szűréssel</span><span class="sxs-lookup"><span data-stu-id="0d513-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="0d513-116">Ez a parancs minden elérhető geo-redundáns biztonsági mentést kap egy olyan kiszolgálón, amely "contoso" kezdetű.</span><span class="sxs-lookup"><span data-stu-id="0d513-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="0d513-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d513-117">PARAMETERS</span></span>

### <span data-ttu-id="0d513-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0d513-118">-DatabaseName</span></span>
<span data-ttu-id="0d513-119">A beolvasott adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d513-119">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="0d513-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d513-120">-DefaultProfile</span></span>
<span data-ttu-id="0d513-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0d513-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d513-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d513-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d513-123">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-adatbázis kiszolgálója van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0d513-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="0d513-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0d513-124">-ServerName</span></span>
<span data-ttu-id="0d513-125">Itt adhatja meg annak a kiszolgálónak a nevét, amely a visszaállítani kívánt biztonsági másolatot tárolja.</span><span class="sxs-lookup"><span data-stu-id="0d513-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="0d513-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0d513-126">-Confirm</span></span>
<span data-ttu-id="0d513-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0d513-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d513-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d513-128">-WhatIf</span></span>
<span data-ttu-id="0d513-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0d513-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d513-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d513-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d513-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d513-131">CommonParameters</span></span>
<span data-ttu-id="0d513-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d513-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d513-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0d513-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d513-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d513-134">INPUTS</span></span>

### <span data-ttu-id="0d513-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0d513-135">System.String</span></span>

## <span data-ttu-id="0d513-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d513-136">OUTPUTS</span></span>

### <span data-ttu-id="0d513-137">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="0d513-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="0d513-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d513-138">NOTES</span></span>

## <span data-ttu-id="0d513-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d513-139">RELATED LINKS</span></span>

[<span data-ttu-id="0d513-140">Áttekintés: a Felhőbeli üzletmenet folytonossága és az adatbázis katasztrófa-elhárítása SQL-adatbázissal</span><span class="sxs-lookup"><span data-stu-id="0d513-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="0d513-141">Azure SQL-adatbázis helyreállítása leállás esetén</span><span class="sxs-lookup"><span data-stu-id="0d513-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="0d513-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d513-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="0d513-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0d513-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
