---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016298"
---
# <span data-ttu-id="66f42-101">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="66f42-101">Get-AzureSqlDatabase</span></span>

## <span data-ttu-id="66f42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66f42-102">SYNOPSIS</span></span>
<span data-ttu-id="66f42-103">Egy vagy több adatbázis beolvasása</span><span class="sxs-lookup"><span data-stu-id="66f42-103">Retrieves one or more databases.</span></span>

## <span data-ttu-id="66f42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66f42-104">SYNTAX</span></span>

### <span data-ttu-id="66f42-105">ByConnectionContext (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66f42-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="66f42-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="66f42-106">ByServerName</span></span>
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="66f42-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="66f42-107">DESCRIPTION</span></span>
<span data-ttu-id="66f42-108">A **Get-AzureSqlDatabase** parancsmag egy Azure SQL-adatbázis egy vagy több példányát kéri egy Azure SQL adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="66f42-108">The **Get-AzureSqlDatabase** cmdlet retrieves one or more instances of an Azure SQL Database from an Azure SQL Database server.</span></span>
<span data-ttu-id="66f42-109">Megadhatja azt a kiszolgálót, amely a **New-AzureSqlDatabaseServerContext** parancsmaggal létrehozott Azure SQL adatbázis-kiszolgáló kapcsolati környezettel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="66f42-109">You can specify the server with an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="66f42-110">Ha az Azure SQL-adatbázis kiszolgálójának nevét adja meg, a parancsmag az aktuális Azure-előfizetési adatokkal hitelesíti a kiszolgáló elérésére vonatkozó kérést.</span><span class="sxs-lookup"><span data-stu-id="66f42-110">Or, if you specify the Azure SQL Database server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="66f42-111">Ha nem ad meg adatbázist, a **Get-AzureSqlDatabase** parancsmag a megadott kiszolgáló összes adatbázisát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="66f42-111">If you do not specify a database, the **Get-AzureSqlDatabase** cmdlet returns all databases from the specified server.</span></span>

<span data-ttu-id="66f42-112">Helyreállítható ledobott adatbázisok beolvasása:</span><span class="sxs-lookup"><span data-stu-id="66f42-112">Retrieving restorable dropped databases:</span></span>

<span data-ttu-id="66f42-113">Helyreállítható ledobott adatbázisok beolvasása a *RestorableDropped* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="66f42-113">Retrieve restorable dropped databases by using the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="66f42-114">Az összes helyreállítható ledobott adatbázis visszaadásához használja a *RestorableDropped* paramétert a *databasename* és a *DatabaseDeletionDate* nélkül.</span><span class="sxs-lookup"><span data-stu-id="66f42-114">To return all restorable dropped databases use the *RestorableDropped* parameter without *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="66f42-115">Egy bizonyos helyreállítható ledobott adatbázis visszaadásához használja a *RestorableDropped* paramétert a *databasename* és a *DatabaseDeletionDate* paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="66f42-115">To return a specific restorable dropped database use the *RestorableDropped* parameter with the *DatabaseName* and *DatabaseDeletionDate* parameters.</span></span>
<span data-ttu-id="66f42-116">Ha a *databasename* paraméterrel egy bizonyos helyreállítható ledobott adatbázist keres, akkor a *DatabaseDeletionDate* paramétert is tartalmaznia kell, és a megadott *DatabaseDeletionDate* értéknek tartalmaznia kell egy ezredmásodpercet, hogy megfeleljen a kívánt adatbázisnak.</span><span class="sxs-lookup"><span data-stu-id="66f42-116">When retrieving a specific restorable dropped database by using the *DatabaseName* parameter you must also include the *DatabaseDeletionDate* parameter and the specified *DatabaseDeletionDate* value must include milliseconds to match the desired database.</span></span>

<span data-ttu-id="66f42-117">A **Get-AzureSqlDatabase** parancsmag a kiszolgálón található összes helyreállítható, illetve a *databasename* és a *DatabaseDeletionDate* -ban egyaránt megfelelő adatbázis esetén visszaadott adatbázist ad vissza.</span><span class="sxs-lookup"><span data-stu-id="66f42-117">The **Get-AzureSqlDatabase** cmdlet returns either all restorable dropped databases on a server, or one specific database that matches both *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="66f42-118">Ha olyan helyreállítható, visszavezethető adatbázisokat szeretne visszaadni, amelyek eltérő feltételekkel (például az összes helyreállítható ledobott adatbázissal) felelnek meg</span><span class="sxs-lookup"><span data-stu-id="66f42-118">To return restorable dropped databases that satisfy different criteria, such as all restorable dropped databases of a specific name, you must return all restorable dropped databases, and then filter the results on the client.</span></span>

## <span data-ttu-id="66f42-119">Példák</span><span class="sxs-lookup"><span data-stu-id="66f42-119">EXAMPLES</span></span>

### <span data-ttu-id="66f42-120">Példa 1: az összes adatbázis lekérése a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="66f42-120">Example 1: Retrieve all databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="66f42-121">Ez a parancs a lpqd0zbr8y nevű kiszolgálón lekérdezi az összes adatbázist.</span><span class="sxs-lookup"><span data-stu-id="66f42-121">This command retrieves all databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="66f42-122">2. példa: az összes helyreállítható ledobott adatbázis lekérése a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="66f42-122">Example 2: Retrieve all restorable dropped databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

<span data-ttu-id="66f42-123">Ez a parancs a lpqd0zbr8y nevű kiszolgálón lekéri az összes helyreállítható ledobott adatbázist.</span><span class="sxs-lookup"><span data-stu-id="66f42-123">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="66f42-124">3. példa: adatbázis lekérése a kapcsolati környezet által meghatározott kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="66f42-124">Example 3: Retrieve a database from a server specified by a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="66f42-125">Ez a parancs a Database01 nevű adatbázist a kapcsolati környezet $Context által megadott kiszolgálóról kéri le.</span><span class="sxs-lookup"><span data-stu-id="66f42-125">This command retrieves database named Database01 from the server specified by the connection context $Context.</span></span>

### <span data-ttu-id="66f42-126">4. példa: adatbázis-objektum tárolása egy változóban</span><span class="sxs-lookup"><span data-stu-id="66f42-126">Example 4: Store a database object in a variable</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="66f42-127">Ez a parancs a Database01 nevű adatbázist a lpqd0zbr8y nevű kiszolgálóról lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="66f42-127">This command retrieves database named Database01 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="66f42-128">A parancs a $Database 01 változóban tárolja az adatbázis-objektumot.</span><span class="sxs-lookup"><span data-stu-id="66f42-128">The command stores the database object in the $Database01 variable.</span></span>

### <span data-ttu-id="66f42-129">Példa 5: helyreállítható ledobott adatbázis beolvasása</span><span class="sxs-lookup"><span data-stu-id="66f42-129">Example 5: Retrieve a restorable dropped database</span></span>
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

<span data-ttu-id="66f42-130">Ez a parancs beolvassa a Database01 nevű, 11/9/2012 nevű, a lpqd0zbr8y nevű kiszolgálóról törölt visszaállító adatbázist.</span><span class="sxs-lookup"><span data-stu-id="66f42-130">This command retrieves the restorable dropped database named Database01 that was deleted on 11/9/2012 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="66f42-131">Ez a parancs az eredményt a $DroppedDB változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="66f42-131">This command stores the results in the $DroppedDB variable.</span></span>

### <span data-ttu-id="66f42-132">6. példa: az összes helyreállítható ledobott adatbázis lekérése a kiszolgálón és a találatok szűrése</span><span class="sxs-lookup"><span data-stu-id="66f42-132">Example 6: Retrieve all restorable dropped databases on a server and filter the results</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

<span data-ttu-id="66f42-133">Ez a parancs beolvassa az összes helyreállítható ledobott adatbázist a lpqd0zbr8y nevű kiszolgálón, majd az eredményeket csak a ContactDB nevű adatbázisokra szűri.</span><span class="sxs-lookup"><span data-stu-id="66f42-133">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y, and then filters the results to only the databases named ContactDB.</span></span>

## <span data-ttu-id="66f42-134">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66f42-134">PARAMETERS</span></span>

### <span data-ttu-id="66f42-135">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="66f42-135">-ConnectionContext</span></span>
<span data-ttu-id="66f42-136">Annak a kiszolgálónak a kapcsolati környezetét adja meg, amelyből adatbázist szeretne beolvasni.</span><span class="sxs-lookup"><span data-stu-id="66f42-136">Specifies the connection context of a server from which to retrieve a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-137">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="66f42-137">-Database</span></span>
<span data-ttu-id="66f42-138">Itt adhatja meg azt az adatbázist, amely a parancsmag által lekérdezett adatbázist jelöli.</span><span class="sxs-lookup"><span data-stu-id="66f42-138">Specifies an object that represents the database that this cmdlet retrieves.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-139">-DatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="66f42-139">-DatabaseDeletionDate</span></span>
<span data-ttu-id="66f42-140">A törlés dátumát és időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="66f42-140">Specifies the date and time of a deletion.</span></span>
<span data-ttu-id="66f42-141">Ha a *RestorableDropped* paramétert adja meg, ezt a paramétert akkor adja meg, ha a törlés dátuma és időpontja alapján visszaállíthatja a helyreállítható ledobott adatbázist.</span><span class="sxs-lookup"><span data-stu-id="66f42-141">If you specify the *RestorableDropped* parameter, specify this parameter to retrieve a restorable dropped database based on the deletion date and time.</span></span>

<span data-ttu-id="66f42-142">A *DatabaseDeletionDate* paraméternek tartalmaznia kell egy ezredmásodpercet a kívánt adatbázis időpontjának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="66f42-142">The *DatabaseDeletionDate* parameter must include milliseconds to match the time of the desired database.</span></span>
<span data-ttu-id="66f42-143">Az érték megadásával milliszekundum nélkül az adatbázis nem található.</span><span class="sxs-lookup"><span data-stu-id="66f42-143">Specifying a value without milliseconds results in the database not being found.</span></span>

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

### <span data-ttu-id="66f42-144">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66f42-144">-DatabaseName</span></span>
<span data-ttu-id="66f42-145">Itt adhatja meg annak az adatbázisnak a nevét, amely a parancsmagot kéri.</span><span class="sxs-lookup"><span data-stu-id="66f42-145">Specifies the name of the database that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="66f42-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="66f42-146">-Profile</span></span>
<span data-ttu-id="66f42-147">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="66f42-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66f42-148">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="66f42-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66f42-149">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="66f42-149">-RestorableDropped</span></span>
<span data-ttu-id="66f42-150">Azt jelzi, hogy ez a parancsmag az *adatbázis* -objektumok helyett az *RestorableDroppedDatabase* -objektumokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="66f42-150">Indicates that this cmdlet returns *RestorableDroppedDatabase* objects instead of *Database* objects.</span></span>
<span data-ttu-id="66f42-151">A *DatabaseDeletionDate* paraméterrel kiválaszthat egy bizonyos helyreállítható ledobott adatbázist.</span><span class="sxs-lookup"><span data-stu-id="66f42-151">You can use the *DatabaseDeletionDate* parameter to select a specific restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-152">-RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="66f42-152">-RestorableDroppedDatabase</span></span>
<span data-ttu-id="66f42-153">Itt adhatja meg azt az objektumot, amely a parancsmag által beolvasott helyreállítható adatbázisnak a megfelelője.</span><span class="sxs-lookup"><span data-stu-id="66f42-153">Specifies an object that represents the restorable dropped database that this cmdlet retrieves.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-154">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="66f42-154">-ServerName</span></span>
<span data-ttu-id="66f42-155">Megadja annak a kiszolgálónak a nevét, amely a parancsmag által lekérdezett adatbázist tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="66f42-155">Specifies the name of the server that contains the database that this cmdlet retrieves.</span></span>
<span data-ttu-id="66f42-156">A parancsmag az aktuális Azure-előfizetést használja a kiszolgáló eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="66f42-156">The cmdlet uses the current Azure subscription to access the server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f42-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f42-157">CommonParameters</span></span>
<span data-ttu-id="66f42-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66f42-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f42-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66f42-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f42-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66f42-160">INPUTS</span></span>

### <span data-ttu-id="66f42-161">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="66f42-161">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="66f42-162">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="66f42-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

## <span data-ttu-id="66f42-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66f42-163">OUTPUTS</span></span>

### <span data-ttu-id="66f42-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span><span class="sxs-lookup"><span data-stu-id="66f42-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span></span>
<span data-ttu-id="66f42-165">Ez a parancsmag egy *adatbázis* -objektumot ad eredményül, ha nem adja meg a *RestorableDropped* paramétert.</span><span class="sxs-lookup"><span data-stu-id="66f42-165">This cmdlet returns a *Database* object if you do not specify the *RestorableDropped* parameter.</span></span>

### <span data-ttu-id="66f42-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span><span class="sxs-lookup"><span data-stu-id="66f42-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span></span>
<span data-ttu-id="66f42-167">Ez a parancsmag *RestorableDroppedDatabase* -objektumot ad eredményül, ha a *RestorableDropped* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="66f42-167">This cmdlet returns a *RestorableDroppedDatabase* object if you specify the *RestorableDropped* parameter.</span></span>

## <span data-ttu-id="66f42-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66f42-168">NOTES</span></span>

## <span data-ttu-id="66f42-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66f42-169">RELATED LINKS</span></span>

[<span data-ttu-id="66f42-170">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="66f42-170">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="66f42-171">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="66f42-171">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="66f42-172">Új – AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="66f42-172">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="66f42-173">Új – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="66f42-173">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="66f42-174">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="66f42-174">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="66f42-175">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="66f42-175">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


