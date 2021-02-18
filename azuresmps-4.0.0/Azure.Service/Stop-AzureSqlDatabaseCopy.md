---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405618"
---
# <span data-ttu-id="71e74-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="71e74-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="71e74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71e74-102">SYNOPSIS</span></span>
<span data-ttu-id="71e74-103">Folyamatos másolási kapcsolatot szüntet meg.</span><span class="sxs-lookup"><span data-stu-id="71e74-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="71e74-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71e74-104">SYNTAX</span></span>

### <span data-ttu-id="71e74-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="71e74-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71e74-106">Adatbázis-adatbázis</span><span class="sxs-lookup"><span data-stu-id="71e74-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71e74-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="71e74-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71e74-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71e74-108">DESCRIPTION</span></span>
<span data-ttu-id="71e74-109">A **Stop-AzureSqlDatabaseCopy** parancsmag megszakítja a folyamatos másolási kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="71e74-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="71e74-110">Ez a parancsmag leállítja az adatmozgást a forrásadatbázis és a másodlagos vagy céladatbázis között, majd a másodlagos adatbázis állapotát önálló online adatbázisként módosítja.</span><span class="sxs-lookup"><span data-stu-id="71e74-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="71e74-111">A folyamatos másolási kapcsolatot, a megszüntetést vagy a tervezett megszüntetést és a kényszeres megszüntetést kétféleképpen lehet megszüntetni lehetséges adatvesztéssel.</span><span class="sxs-lookup"><span data-stu-id="71e74-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="71e74-112">A forrásadatbázist tartalmazó kiszolgálón futtathatja ezt a parancsmagot megszüntetés vagy kényszerített megszüntetés módban.</span><span class="sxs-lookup"><span data-stu-id="71e74-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="71e74-113">A másodlagos adatbázist tartalmazó kiszolgálón kényszerített megszüntetést kell használnia.</span><span class="sxs-lookup"><span data-stu-id="71e74-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="71e74-114">A tervezett megszüntetés addig vár, amíg a forrásadatbázisban lekötött tranzakciók a parancsmag futtatásakor a másodlagos adatbázisba replikálódnak.</span><span class="sxs-lookup"><span data-stu-id="71e74-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="71e74-115">A kényszerített megszüntetés nem várja meg a lekötött tranzakciók replikációját, és a másodlagos adatbázisban adatvesztést okozhat.</span><span class="sxs-lookup"><span data-stu-id="71e74-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="71e74-116">A replikáció állapota függőben van, de csak a kényszerített megszüntetés képes megszüntetni a folyamatos másolási kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="71e74-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="71e74-117">Ha a replikáció állapota FÜGGŐBEN van, a nem kényszerített megszüntetés nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="71e74-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="71e74-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71e74-118">EXAMPLES</span></span>

### <span data-ttu-id="71e74-119">1. példa: Folyamatos másolási kapcsolat megszüntetése</span><span class="sxs-lookup"><span data-stu-id="71e74-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="71e74-120">Ez a parancs megszünteti az Orders (Rendelések) nevű adatbázis folyamatos másolási kapcsolatát az lpqd0zbr8y nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="71e74-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="71e74-121">A bk0b8kf658 nevű kiszolgáló tárolja a másodlagos adatbázist.</span><span class="sxs-lookup"><span data-stu-id="71e74-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="71e74-122">2. példa: Folytonos másolási kapcsolat megszüntetése</span><span class="sxs-lookup"><span data-stu-id="71e74-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="71e74-123">Az első parancs az Orders (Rendelések) nevű adatbázis adatbázis-másolási kapcsolatát kapja meg az lpqd0zbr8y nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="71e74-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="71e74-124">A második parancs a másodlagos adatbázist tartalmazó kiszolgáló folyamatos másolási kapcsolatát szünteti meg.</span><span class="sxs-lookup"><span data-stu-id="71e74-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="71e74-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71e74-125">PARAMETERS</span></span>

### <span data-ttu-id="71e74-126">-Database</span><span class="sxs-lookup"><span data-stu-id="71e74-126">-Database</span></span>
<span data-ttu-id="71e74-127">A forrás Azure SQL-adatbázist képviselő objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="71e74-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="71e74-128">Ez a parancsmag megszakítja a paraméterként megadott adatbázis folyamatos másolási kapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="71e74-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71e74-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="71e74-129">-DatabaseCopy</span></span>
<span data-ttu-id="71e74-130">Egy adatbázist képviselő objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="71e74-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="71e74-131">Ez a parancsmag megszakítja a paraméterként megadott adatbázis folyamatos másolási kapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="71e74-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="71e74-132">Ez a paraméter elfogadja a folyamatbemenetet.</span><span class="sxs-lookup"><span data-stu-id="71e74-132">This parameter accepts pipeline input.</span></span>

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71e74-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="71e74-133">-DatabaseName</span></span>
<span data-ttu-id="71e74-134">Egy adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71e74-134">Specifies the name of a database.</span></span>
<span data-ttu-id="71e74-135">Ez a parancsmag megszakítja a paraméterként megadott adatbázis folyamatos másolási kapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="71e74-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e74-136">-Force</span><span class="sxs-lookup"><span data-stu-id="71e74-136">-Force</span></span>
<span data-ttu-id="71e74-137">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="71e74-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71e74-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="71e74-138">-ForcedTermination</span></span>
<span data-ttu-id="71e74-139">Azt jelzi, hogy ez a parancsmag a folyamatos másolási kapcsolat kényszerített megszűnését okozza.</span><span class="sxs-lookup"><span data-stu-id="71e74-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="71e74-140">A kényszerített megszüntetés adatvesztést okozhat.</span><span class="sxs-lookup"><span data-stu-id="71e74-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="71e74-141">Ha a parancsmagot a céladatbázist tároló kiszolgálón futtatni, meg kell adnia ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="71e74-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="71e74-142">Ha ezt a parancsmagot a forrásadatbázist tartalmazó kiszolgálón futtatni, ha a másodlagos adatbázis nem érhető el, meg kell adnia ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="71e74-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="71e74-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="71e74-143">-PartnerDatabase</span></span>
<span data-ttu-id="71e74-144">A másodlagos adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71e74-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="71e74-145">Ha megad egy nevet, annak meg kell egyeznie a forrásadatbázis nevével.</span><span class="sxs-lookup"><span data-stu-id="71e74-145">If you specify a name, it must match the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e74-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="71e74-146">-PartnerServer</span></span>
<span data-ttu-id="71e74-147">A céladatbázist tároló kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="71e74-147">Specifies the name of the server that hosts the target database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e74-148">-Profil</span><span class="sxs-lookup"><span data-stu-id="71e74-148">-Profile</span></span>
<span data-ttu-id="71e74-149">Azt az Azure-profilt adja meg, amelyből a parancsmag olvas.</span><span class="sxs-lookup"><span data-stu-id="71e74-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="71e74-150">Ha nem ad meg profilt, ez a parancsmag a helyi alapértelmezett profilból olvassa be.</span><span class="sxs-lookup"><span data-stu-id="71e74-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71e74-151">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71e74-151">-ServerName</span></span>
<span data-ttu-id="71e74-152">Annak a kiszolgálónak a nevét adja meg, amelyen a forrásadatbázis található.</span><span class="sxs-lookup"><span data-stu-id="71e74-152">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71e74-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71e74-153">-Confirm</span></span>
<span data-ttu-id="71e74-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="71e74-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e74-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e74-155">-WhatIf</span></span>
<span data-ttu-id="71e74-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="71e74-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71e74-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71e74-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e74-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e74-158">CommonParameters</span></span>
<span data-ttu-id="71e74-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e74-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e74-160">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e74-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e74-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71e74-161">INPUTS</span></span>

### <span data-ttu-id="71e74-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="71e74-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="71e74-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="71e74-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="71e74-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71e74-164">OUTPUTS</span></span>

### <span data-ttu-id="71e74-165">Nincs</span><span class="sxs-lookup"><span data-stu-id="71e74-165">None</span></span>

## <span data-ttu-id="71e74-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71e74-166">NOTES</span></span>
* <span data-ttu-id="71e74-167">Hitelesítés: Ez a parancsmag tanúsítványalapú hitelesítést igényel.</span><span class="sxs-lookup"><span data-stu-id="71e74-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="71e74-168">Ha például tanúsítványalapú hitelesítéssel állíthatja be az aktuális előfizetést, tekintse meg a **New-AzureSqlDatabaseServerContext** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="71e74-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="71e74-169">Korlátozások: A másodlagos adatbázist tartalmazó kiszolgálón csak a kényszerített megszüntetés támogatott.</span><span class="sxs-lookup"><span data-stu-id="71e74-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="71e74-170">A megszűnés hatása a korábbi másodlagos adatbázisra: A megszüntetés után a másodlagos adatbázis független adatbázissá válik.</span><span class="sxs-lookup"><span data-stu-id="71e74-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="71e74-171">Ha már befejeződött a másodlagos adatbázis létrehozása, az adatbázis megszüntetése után az adatbázis teljes hozzáférésre van megnyitva.</span><span class="sxs-lookup"><span data-stu-id="71e74-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="71e74-172">Ha a forrásadatbázis írási és írási adatbázis, a korábbi másodlagos adatbázis is írási és írási adatbázissá válik.</span><span class="sxs-lookup"><span data-stu-id="71e74-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="71e74-173">Ha a bevetés folyamatban van, a rendszer megszakítja a bevetést, és a korábbi másodlagos adatbázis soha nem lesz látható a másodlagos adatbázist tartalmazó kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="71e74-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="71e74-174">A forrásadatbázist írási módra állíthatja.</span><span class="sxs-lookup"><span data-stu-id="71e74-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="71e74-175">Ez garantálja, hogy a rendszer a megszűnés után szinkronizálja a forrás- és a másodlagos adatbázisokat, és biztosítja, hogy a megszüntetés során ne legyen tranzakciók lekötöttek.</span><span class="sxs-lookup"><span data-stu-id="71e74-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="71e74-176">A megszüntetés befejeződése után állítsa vissza a forrást írási és olvasási módba.</span><span class="sxs-lookup"><span data-stu-id="71e74-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="71e74-177">Ha szükséges, a korábbi másodlagos adatbázist írási-olvasási módra is beállíthatja.</span><span class="sxs-lookup"><span data-stu-id="71e74-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="71e74-178">Figyelés: Ha a folyamatos másolási kapcsolat forrásán és célszámán is ellenőriznie kell a műveletek állapotát, használja a **Get-AzureSqlDatabaseOperation** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="71e74-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="71e74-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71e74-179">RELATED LINKS</span></span>

[<span data-ttu-id="71e74-180">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="71e74-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="71e74-181">Műveletek az Azure SQL-adatbázisokban</span><span class="sxs-lookup"><span data-stu-id="71e74-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="71e74-182">Adatbázis-másolás vége</span><span class="sxs-lookup"><span data-stu-id="71e74-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[<span data-ttu-id="71e74-183">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="71e74-183">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="71e74-184">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="71e74-184">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


