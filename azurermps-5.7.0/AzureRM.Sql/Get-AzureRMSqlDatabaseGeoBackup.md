---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: 79e4919278e034c97b224c17538edfebfbf51a43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678924"
---
# <span data-ttu-id="2d9d4-101">Get-AzureRmSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="2d9d4-101">Get-AzureRmSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="2d9d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d9d4-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9d4-103">Egy adatbázis geo-redundáns biztonsági másolatát kapja.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-103">Gets a geo-redundant backup of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d9d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d9d4-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d9d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d9d4-105">DESCRIPTION</span></span>
<span data-ttu-id="2d9d4-106">A **Get-AzureRMSqlDatabaseGeoBackup** PARANCSMAG egy SQL-adatbázis meghatározott geo-redundáns biztonsági másolatát kapja, vagy az összes rendelkezésre álló geo-redundáns biztonsági mentést egy adott kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-106">The **Get-AzureRMSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>

<span data-ttu-id="2d9d4-107">A Geo-redundáns biztonsági másolat egy helyreállítható erőforrás, amely külön földrajzi helyről származó adatfájlokat használ.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="2d9d4-108">A Geo-Restore segítségével visszaállíthatja a Geo-redundáns biztonsági másolatot az adatbázis új területre való visszaállításához regionális leállás esetén.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>

<span data-ttu-id="2d9d4-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2d9d4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2d9d4-110">EXAMPLES</span></span>

### <span data-ttu-id="2d9d4-111">Példa 1: minden geo-redundáns biztonsági másolat beolvasása a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="2d9d4-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="2d9d4-112">Ez a parancs a megadott kiszolgálón elérhető geo-redundáns biztonsági másolatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="2d9d4-113">2. példa: meghatározott geo-redundáns biztonsági másolat beszerzése</span><span class="sxs-lookup"><span data-stu-id="2d9d4-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="2d9d4-114">Ez a parancs a ContosoDatabase nevű adatbázis geo-redundáns biztonsági másolatát kapja.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

## <span data-ttu-id="2d9d4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d9d4-115">PARAMETERS</span></span>

### <span data-ttu-id="2d9d4-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2d9d4-116">-DatabaseName</span></span>
<span data-ttu-id="2d9d4-117">A beolvasott adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-117">Specifies the name of the database to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9d4-118">-DefaultProfile</span></span>
<span data-ttu-id="2d9d4-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2d9d4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d9d4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d9d4-120">-ResourceGroupName</span></span>
<span data-ttu-id="2d9d4-121">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-adatbázis kiszolgálója van rendelve.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-121">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9d4-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2d9d4-122">-ServerName</span></span>
<span data-ttu-id="2d9d4-123">Itt adhatja meg annak a kiszolgálónak a nevét, amely a visszaállítani kívánt biztonsági másolatot tárolja.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-123">Specifies the name of the server that hosts the backup to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9d4-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2d9d4-124">-Confirm</span></span>
<span data-ttu-id="2d9d4-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d9d4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d9d4-126">-WhatIf</span></span>
<span data-ttu-id="2d9d4-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d9d4-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d9d4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9d4-129">CommonParameters</span></span>
<span data-ttu-id="2d9d4-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d9d4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9d4-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d9d4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9d4-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d9d4-132">INPUTS</span></span>

### <span data-ttu-id="2d9d4-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="2d9d4-133">None</span></span>
<span data-ttu-id="2d9d4-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2d9d4-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d9d4-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d9d4-135">OUTPUTS</span></span>

### <span data-ttu-id="2d9d4-136">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="2d9d4-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="2d9d4-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d9d4-137">NOTES</span></span>

## <span data-ttu-id="2d9d4-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d9d4-138">RELATED LINKS</span></span>

[<span data-ttu-id="2d9d4-139">Áttekintés: a Felhőbeli üzletmenet folytonossága és az adatbázis katasztrófa-elhárítása SQL-adatbázissal</span><span class="sxs-lookup"><span data-stu-id="2d9d4-139">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="2d9d4-140">Azure SQL-adatbázis helyreállítása leállás esetén</span><span class="sxs-lookup"><span data-stu-id="2d9d4-140">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="2d9d4-141">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2d9d4-141">Restore-AzureRmSqlDatabase</span></span>](./Restore-AzureRmSqlDatabase.md)

[<span data-ttu-id="2d9d4-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="2d9d4-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
