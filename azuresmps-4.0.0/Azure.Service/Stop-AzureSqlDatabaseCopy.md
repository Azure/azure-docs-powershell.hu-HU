---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016403"
---
# <span data-ttu-id="4c9ea-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4c9ea-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="4c9ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9ea-103">Folytonos másolási kapcsolat megszüntetése</span><span class="sxs-lookup"><span data-stu-id="4c9ea-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="4c9ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c9ea-104">SYNTAX</span></span>

### <span data-ttu-id="4c9ea-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4c9ea-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c9ea-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="4c9ea-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c9ea-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4c9ea-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c9ea-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c9ea-108">DESCRIPTION</span></span>
<span data-ttu-id="4c9ea-109">A **stop-AzureSqlDatabaseCopy** parancsmag folytonos másolási kapcsolatot szüntet meg.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="4c9ea-110">Ez a parancsmag leállítja a forrásadatbázis és a másodlagos vagy a cél adatbázis közötti adatmozgást, majd a másodlagos adatbázis állapotát különálló online adatbázisként módosítja.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="4c9ea-111">A folyamatos másolási viszonyok, a megszüntetési vagy a tervezett megszűnések, valamint a kényszer megszűnése két módon végezhető el a lehetséges adatvesztéssel.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="4c9ea-112">A forrás adatbázist tároló kiszolgálón futtathatja ezt a parancsmagot a megszüntetés vagy a kényszeres lemondási mód használatával.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="4c9ea-113">A másodlagos adatbázist tároló kiszolgálón kényszerített befejezési módot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="4c9ea-114">A tervezett megszüntetés csak akkor várja a másodlagos adatbázisba, ha a forrástartományban futtatott összes tranzakciót futtatta a forrás adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="4c9ea-115">A kényszeres megszűnés nem várja meg az esetleges függőben lévő lekötött tranzakciók replikálását, és a másodlagos adatbázis esetleges adatvesztését is okozhatja.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="4c9ea-116">Amíg a replikációs állapot FÜGGŐben van, csak a kényszer megszűnése lehet sikeres a folyamatos másolási kapcsolat befejezése.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="4c9ea-117">Ha a replikációs állapot FÜGGŐben van, a záró érték nem használható.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="4c9ea-118">Példák</span><span class="sxs-lookup"><span data-stu-id="4c9ea-118">EXAMPLES</span></span>

### <span data-ttu-id="4c9ea-119">1. példa: folyamatos másolati kapcsolat megszüntetése</span><span class="sxs-lookup"><span data-stu-id="4c9ea-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="4c9ea-120">Ez a parancs a lpqd0zbr8y nevű kiszolgálón a rendelések nevű adatbázis folyamatos másolati kapcsolatát zárja le.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="4c9ea-121">A bk0b8kf658 nevű kiszolgáló a másodlagos adatbázist tárolja.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="4c9ea-122">2. példa: folyamatos másolati kapcsolat megszüntetése</span><span class="sxs-lookup"><span data-stu-id="4c9ea-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="4c9ea-123">Az első parancs a lpqd0zbr8y nevű kiszolgálón a rendelések nevű adatbázis adatbázis-másolási kapcsolatát kapja.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="4c9ea-124">A második parancs a másodlagos adatbázist tároló kiszolgálóról folyamatosan megszünteti a folyamatos másolási viszonyt.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="4c9ea-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c9ea-125">PARAMETERS</span></span>

### <span data-ttu-id="4c9ea-126">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="4c9ea-126">-Database</span></span>
<span data-ttu-id="4c9ea-127">Egy olyan objektumot ad meg, amely a Source Azure SQL-adatbázist jelöli.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="4c9ea-128">Ez a parancsmag lezárja az adatbázis folytonos másolati kapcsolatát, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="4c9ea-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4c9ea-129">-DatabaseCopy</span></span>
<span data-ttu-id="4c9ea-130">Egy adatbázist jelképező objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="4c9ea-131">Ez a parancsmag lezárja az adatbázis folytonos másolati kapcsolatát, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="4c9ea-132">Ez a paraméter elfogadja a csővezeték-bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-132">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="4c9ea-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4c9ea-133">-DatabaseName</span></span>
<span data-ttu-id="4c9ea-134">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-134">Specifies the name of a database.</span></span>
<span data-ttu-id="4c9ea-135">Ez a parancsmag lezárja az adatbázis folytonos másolati kapcsolatát, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="4c9ea-136">-Force</span><span class="sxs-lookup"><span data-stu-id="4c9ea-136">-Force</span></span>
<span data-ttu-id="4c9ea-137">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4c9ea-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="4c9ea-138">-ForcedTermination</span></span>
<span data-ttu-id="4c9ea-139">Jelzi, hogy ez a parancsmag a folyamatos másolási viszony kényszeres megszüntetését okozta.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="4c9ea-140">A kényszeres megszűnés az adatvesztéssel járhat.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="4c9ea-141">Ha a parancsmagot egy olyan kiszolgálón szeretné futtatni, amelyen a céladatbázis található, ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="4c9ea-142">Ha a parancsmagot a forrás adatbázist tároló kiszolgálón szeretné futtatni, ha a másodlagos adatbázis nem érhető el, akkor ezt a paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="4c9ea-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="4c9ea-143">-PartnerDatabase</span></span>
<span data-ttu-id="4c9ea-144">A másodlagos adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="4c9ea-145">Ha megad egy nevet, a forrás-adatbázis nevének egyeznie kell.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-145">If you specify a name, it must match the name of the source database.</span></span>

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

### <span data-ttu-id="4c9ea-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="4c9ea-146">-PartnerServer</span></span>
<span data-ttu-id="4c9ea-147">A célként megadott adatbázist tároló kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-147">Specifies the name of the server that hosts the target database.</span></span>

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

### <span data-ttu-id="4c9ea-148">-Profil</span><span class="sxs-lookup"><span data-stu-id="4c9ea-148">-Profile</span></span>
<span data-ttu-id="4c9ea-149">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c9ea-150">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4c9ea-151">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="4c9ea-151">-ServerName</span></span>
<span data-ttu-id="4c9ea-152">Annak a kiszolgálónak a nevét adja meg, amelyen a forrás adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-152">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="4c9ea-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4c9ea-153">-Confirm</span></span>
<span data-ttu-id="4c9ea-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c9ea-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c9ea-155">-WhatIf</span></span>
<span data-ttu-id="4c9ea-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c9ea-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c9ea-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9ea-158">CommonParameters</span></span>
<span data-ttu-id="4c9ea-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c9ea-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9ea-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c9ea-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9ea-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c9ea-161">INPUTS</span></span>

### <span data-ttu-id="4c9ea-162">Microsoft. WindowsAzure. Command. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4c9ea-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="4c9ea-163">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="4c9ea-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="4c9ea-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c9ea-164">OUTPUTS</span></span>

### <span data-ttu-id="4c9ea-165">Nincs</span><span class="sxs-lookup"><span data-stu-id="4c9ea-165">None</span></span>

## <span data-ttu-id="4c9ea-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c9ea-166">NOTES</span></span>
* <span data-ttu-id="4c9ea-167">Hitelesítés: Ez a parancsmag tanúsítvány-alapú hitelesítést követel meg.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="4c9ea-168">Példa arra, hogy hogyan állíthatja be a jelenlegi előfizetést a tanúsítványalapú hitelesítéssel, ha a **New-AzureSqlDatabaseServerContext** parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="4c9ea-169">Korlátozások: a másodlagos adatbázist tároló kiszolgálón csak a kényszeres megszüntetés támogatott.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="4c9ea-170">A megszüntetés hatása a volt másodlagos adatbázisra: a megszüntetést követően a másodlagos adatbázis független adatbázis lesz.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="4c9ea-171">Ha a másodlagos adatbázison már elkészült a kivetés, az adatbázis befejezését követően teljes hozzáférésre nyitva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="4c9ea-172">Ha a forrásadatbázis egy írható-olvasható adatbázis, a volt másodlagos adatbázis is írható-olvasható adatbázis lesz.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="4c9ea-173">Ha a kivetés jelenleg folyamatban van, a vetés megszakad, és a volt másodlagos adatbázis nem lesz látható a másodlagos adatbázist tároló kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="4c9ea-174">A forrásadatok csak olvasható módra állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="4c9ea-175">Ez biztosítja, hogy a forrás-és másodlagos adatbázisokat a befejezés után szinkronizálja a program, és gondoskodjon arról, hogy a lemondáskor ne történjen semmilyen tranzakció véglegesítése.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="4c9ea-176">A Befejezés befejezése után állítsa vissza a forrást olvasási és írási módra.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="4c9ea-177">A korábbi másodlagos adatbázist tetszés szerint is megadhatja olvasási és írási módra.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="4c9ea-178">Monitoring: Ha ellenőrizni szeretné a műveletek állapotát a folyamatos másolási kapcsolat forrásában és céljában, használja a **Get-AzureSqlDatabaseOperation** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4c9ea-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="4c9ea-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c9ea-179">RELATED LINKS</span></span>

[<span data-ttu-id="4c9ea-180">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="4c9ea-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="4c9ea-181">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="4c9ea-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="4c9ea-182">Adatbázis-példány leállítása</span><span class="sxs-lookup"><span data-stu-id="4c9ea-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[<span data-ttu-id="4c9ea-183">Azure SQL-adatbázis-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4c9ea-183">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="4c9ea-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4c9ea-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="4c9ea-185">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4c9ea-185">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


