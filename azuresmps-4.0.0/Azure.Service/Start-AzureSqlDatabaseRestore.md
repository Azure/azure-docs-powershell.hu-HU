---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015426"
---
# <span data-ttu-id="5a803-101">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="5a803-101">Start-AzureSqlDatabaseRestore</span></span>

## <span data-ttu-id="5a803-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a803-102">SYNOPSIS</span></span>
<span data-ttu-id="5a803-103">Időpontot ad vissza az adatbázis időpontjában.</span><span class="sxs-lookup"><span data-stu-id="5a803-103">Performs a point in time restore of a database.</span></span>

## <span data-ttu-id="5a803-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a803-104">SYNTAX</span></span>

### <span data-ttu-id="5a803-105">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5a803-105">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a803-106">BySourceRestorableDroppedDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5a803-106">BySourceRestorableDroppedDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a803-107">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a803-107">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a803-108">BySourceRestorableDroppedDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a803-108">BySourceRestorableDroppedDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5a803-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a803-109">DESCRIPTION</span></span>
<span data-ttu-id="5a803-110">A **Start-AzureSqlDatabaseRestore** parancsmag egy egyszerű, normál vagy prémium adatbázis időpontjának visszaállítását végzi.</span><span class="sxs-lookup"><span data-stu-id="5a803-110">The **Start-AzureSqlDatabaseRestore** cmdlet performs a point in time restore of a Basic, Standard or Premium database.</span></span>
<span data-ttu-id="5a803-111">Az Azure SQL-adatbázis az alapszintű adatbázis biztonsági másolatait 7 nappal, a 14 napra szóló standardot és a 35 napokra szóló prémium verziót őrzi meg.</span><span class="sxs-lookup"><span data-stu-id="5a803-111">Azure SQL Database retains Basic database backups 7 days, Standard for 14 days, and Premium for 35 days.</span></span>
<span data-ttu-id="5a803-112">A visszaállítási művelet új adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5a803-112">The restore operation creates a new database.</span></span>
<span data-ttu-id="5a803-113">Ha a forrásadatbázis nem törlődik, a *SourceDatabaseName* és a *TargetDatabaseName* paraméternek eltérő értékűnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5a803-113">If the source database is not deleted, the *SourceDatabaseName* and *TargetDatabaseName* parameter must have different values.</span></span>

<span data-ttu-id="5a803-114">Az Azure SQL-adatbázis jelenleg nem támogatja a Cross Server Restore-t.</span><span class="sxs-lookup"><span data-stu-id="5a803-114">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="5a803-115">A forrás-és a célkiszolgáló nevének egyeznie kell.</span><span class="sxs-lookup"><span data-stu-id="5a803-115">The source and target server names must be the same.</span></span>

## <span data-ttu-id="5a803-116">Példák</span><span class="sxs-lookup"><span data-stu-id="5a803-116">EXAMPLES</span></span>

### <span data-ttu-id="5a803-117">Példa 1: objektumként megadott adatbázis visszaállítása időpontra</span><span class="sxs-lookup"><span data-stu-id="5a803-117">Example 1: Restore a database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="5a803-118">Az első parancs a Server01 nevű kiszolgálón a Database17 nevű adatbázis adatbázis-objektumát kapja, majd a $Database változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5a803-118">The first command gets a database object for the database named Database17 on the server named Server01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="5a803-119">A második parancs visszaállítja az adatbázist egy adott időpontra.</span><span class="sxs-lookup"><span data-stu-id="5a803-119">The second command restores the database to a specific point in time.</span></span>
<span data-ttu-id="5a803-120">A parancs az új adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a803-120">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="5a803-121">2. példa: név szerint meghatározott adatbázis visszaállítása időpontra</span><span class="sxs-lookup"><span data-stu-id="5a803-121">Example 2: Restore a database specified by name to a point in time</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="5a803-122">A parancs visszaállítja a Database17 nevű adatbázist adott időpontra.</span><span class="sxs-lookup"><span data-stu-id="5a803-122">This command restores the database named Database17 to a specific point in time.</span></span>
<span data-ttu-id="5a803-123">A parancs az új adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a803-123">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="5a803-124">3. példa: az adott időpontig objektumként megadott leejtett adatbázis visszaállítása</span><span class="sxs-lookup"><span data-stu-id="5a803-124">Example 3: Restore a dropped database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

<span data-ttu-id="5a803-125">Az első parancs a Server01 nevű kiszolgálón a Database01 nevű adatbázis adatbázis-objektumát kapja.</span><span class="sxs-lookup"><span data-stu-id="5a803-125">The first command gets a database object for the database named Database01 on the server named Server01.</span></span>
<span data-ttu-id="5a803-126">A parancs a *RestorableDropped* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a803-126">The command specifies the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="5a803-127">Ezért a parancsmag a megadott visszaállítási pontra visszaállíthatja a helyreállítható adatbázisokat.</span><span class="sxs-lookup"><span data-stu-id="5a803-127">Therefore, the cmdlet gets restorable dropped database the specified restore point.</span></span>
<span data-ttu-id="5a803-128">A parancs a $Database változóban tárolja az adatbázis-objektumot.</span><span class="sxs-lookup"><span data-stu-id="5a803-128">The command stores that database object in the $Database variable.</span></span>

<span data-ttu-id="5a803-129">A második parancs visszaállítja az $Database által megadott eldobott adatbázist.</span><span class="sxs-lookup"><span data-stu-id="5a803-129">The second command restores the dropped database specified by $Database.</span></span>
<span data-ttu-id="5a803-130">A parancs az új adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a803-130">The command specifies at name for the new database.</span></span>

## <span data-ttu-id="5a803-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a803-131">PARAMETERS</span></span>

### <span data-ttu-id="5a803-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="5a803-132">-PointInTime</span></span>
<span data-ttu-id="5a803-133">Az adatbázis visszaállítási pontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a803-133">Specifies the restore point to which to restore the database.</span></span>
<span data-ttu-id="5a803-134">Amikor befejezte a visszaállítási műveletet, az adatbázis visszakerül az állapotra, amely a paraméter által megadott dátum és idő szerint van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="5a803-134">When the restore operation finishes, the database is restored to the state it was at the date and time that this parameter specifies.</span></span>
<span data-ttu-id="5a803-135">Alapértelmezés szerint ez a parancsmag az aktuális időpontra van beállítva, és egy leejtett adatbázis esetében az adatbázis elvetésének időpontját használja.</span><span class="sxs-lookup"><span data-stu-id="5a803-135">By default, for a live database this set to the current time, and for a dropped database, this cmdlet uses the time when the database was dropped.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a803-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="5a803-136">-Profile</span></span>
<span data-ttu-id="5a803-137">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5a803-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a803-138">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5a803-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a803-139">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="5a803-139">-RestorableDropped</span></span>
<span data-ttu-id="5a803-140">Jelzi, hogy ez a parancsmag visszaállíthatja a helyreállítható ledobott adatbázist.</span><span class="sxs-lookup"><span data-stu-id="5a803-140">Indicates that this cmdlet restores a restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a803-141">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="5a803-141">-SourceDatabase</span></span>
<span data-ttu-id="5a803-142">Annak az adatbázisnak a nevét adja meg, amelyre a parancsmag visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="5a803-142">Specifies the name of the database that this cmdlet restores.</span></span>

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a803-143">-SourceDatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="5a803-143">-SourceDatabaseDeletionDate</span></span>
<span data-ttu-id="5a803-144">Az adatbázis törlésének dátumát és időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a803-144">Specifies the date and time when the database was deleted.</span></span>
<span data-ttu-id="5a803-145">Ha a tényleges adatbázis-törlési időpontot adja meg, akkor az ezredmásodpercet is tartalmaznia kell.</span><span class="sxs-lookup"><span data-stu-id="5a803-145">You must include milliseconds when you specify the time to match the actual database deletion time.</span></span>

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a803-146">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a803-146">-SourceDatabaseName</span></span>
<span data-ttu-id="5a803-147">Annak az élő adatbázisnak a nevét adja meg, amelyre a parancsmag visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="5a803-147">Specifies the name of the live database that this cmdlet restores.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a803-148">-SourceRestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="5a803-148">-SourceRestorableDroppedDatabase</span></span>
<span data-ttu-id="5a803-149">Itt adhatja meg azt az objektumot, amely a parancsmag által visszaállítható visszaállító adatbázist jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5a803-149">Specifies an object that represents the restorable dropped database that this cmdlet restores.</span></span>
<span data-ttu-id="5a803-150">Ha **RestorableDroppedDatabase** objektumot szeretne beolvasni, használja az Get-AzureSqlDatabase parancsmagot, és adja meg a *RestorableDropped* paramétert.</span><span class="sxs-lookup"><span data-stu-id="5a803-150">To obtain a **RestorableDroppedDatabase** object, use the Get-AzureSqlDatabase cmdlet, and specify the *RestorableDropped* parameter.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a803-151">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="5a803-151">-SourceServerName</span></span>
<span data-ttu-id="5a803-152">Annak a kiszolgálónak a neve, amelyen a forrásadatbázis él és fut, vagy amelyen a forrásadatbázis a törlés előtt futott.</span><span class="sxs-lookup"><span data-stu-id="5a803-152">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a803-153">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a803-153">-TargetDatabaseName</span></span>
<span data-ttu-id="5a803-154">Annak az új adatbázisnak a neve, amely a visszaállítási műveletet hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5a803-154">Specifies the name of the new database that the restore operation creates.</span></span>

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

### <span data-ttu-id="5a803-155">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="5a803-155">-TargetServerName</span></span>
<span data-ttu-id="5a803-156">Annak a kiszolgálónak a nevét adja meg, amelyre a parancsmag visszaállítja az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="5a803-156">Specifies the name of the server to which this cmdlet restores the database.</span></span>

<span data-ttu-id="5a803-157">Az Azure SQL-adatbázis jelenleg nem támogatja a Cross Server Restore-t.</span><span class="sxs-lookup"><span data-stu-id="5a803-157">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="5a803-158">A forrás-és a célkiszolgáló nevének egyeznie kell.</span><span class="sxs-lookup"><span data-stu-id="5a803-158">The source and target server names must be the same.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a803-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a803-159">CommonParameters</span></span>
<span data-ttu-id="5a803-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a803-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a803-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a803-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a803-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a803-162">INPUTS</span></span>

### <span data-ttu-id="5a803-163">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="5a803-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

### <span data-ttu-id="5a803-164">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="5a803-164">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="5a803-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a803-165">OUTPUTS</span></span>

### <span data-ttu-id="5a803-166">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. RestoreDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="5a803-166">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestoreDatabaseOperation</span></span>

## <span data-ttu-id="5a803-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a803-167">NOTES</span></span>
* <span data-ttu-id="5a803-168">A parancsmag futtatásához tanúsítványon alapuló hitelesítést kell használnia.</span><span class="sxs-lookup"><span data-stu-id="5a803-168">You must use certificate based authentication to run this cmdlet.</span></span> <span data-ttu-id="5a803-169">Futtassa az alábbi parancsokat azon a számítógépen, amelyen a parancsmag futtatható:</span><span class="sxs-lookup"><span data-stu-id="5a803-169">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="5a803-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a803-170">RELATED LINKS</span></span>

[<span data-ttu-id="5a803-171">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="5a803-171">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="5a803-172">Adatbázis-visszaállítási kérés létrehozása</span><span class="sxs-lookup"><span data-stu-id="5a803-172">Create Database Restore Request</span></span>](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[<span data-ttu-id="5a803-173">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="5a803-173">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="5a803-174">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5a803-174">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)


