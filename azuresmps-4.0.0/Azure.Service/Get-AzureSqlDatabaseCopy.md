---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016295"
---
# <span data-ttu-id="9bfd4-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="9bfd4-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="9bfd4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9bfd4-102">SYNOPSIS</span></span>
<span data-ttu-id="9bfd4-103">A kapcsolatok másolási állapotának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="9bfd4-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="9bfd4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9bfd4-104">SYNTAX</span></span>

### <span data-ttu-id="9bfd4-105">ByServerNameOnly (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9bfd4-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9bfd4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9bfd4-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9bfd4-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="9bfd4-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9bfd4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9bfd4-108">DESCRIPTION</span></span>
<span data-ttu-id="9bfd4-109">A **Get-AzureSqlDatabaseCopy** parancsmag egy vagy több aktív másolási kapcsolat állapotát ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="9bfd4-110">Futtassa ezt a parancsmagot a Start-AzureSqlDatabaseCopy vagy Stop-AzureSqlDatabaseCopy parancsmag futtatása után.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="9bfd4-111">Ellenőrizheti a másolati viszonyokat, az összes másolt kapcsolatot, illetve a másolt kapcsolatok szűrt listáját, például egy adott célkiszolgáló összes példányát.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="9bfd4-112">Ezt a parancsmagot a forrás-vagy céladatbázis-kiszolgálót futtató kiszolgálón futtathatja.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="9bfd4-113">Ez a parancsmag szinkronban van.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="9bfd4-114">A parancsmag megakadályozza az Azure PowerShell-konzolt, amíg az nem egy állapotsort ad.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="9bfd4-115">A *PartnerServer* és a *PartnerDatabase* paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="9bfd4-116">Ha nem ad meg paramétert, ez a parancsmag a találatok táblázatát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="9bfd4-117">Ha csak egy adott adatbázis állapotát szeretné látni, adja meg mindkét paramétert.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="9bfd4-118">Példák</span><span class="sxs-lookup"><span data-stu-id="9bfd4-118">EXAMPLES</span></span>

### <span data-ttu-id="9bfd4-119">Példa 1: adatbázis másolati állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="9bfd4-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="9bfd4-120">Ez a parancs megkapja a lpqd0zbr8y nevű kiszolgálón a rendelések nevű adatbázis állapotát.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="9bfd4-121">A *PartnerServer* paraméter korlátozza ezt a parancsot az bk0b8kf658-kiszolgálóra.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="9bfd4-122">2. példa: a serverGet lévő összes példány állapotának lekérése</span><span class="sxs-lookup"><span data-stu-id="9bfd4-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="9bfd4-123">Ez a parancs a lpqd0zbr8y nevű kiszolgálón minden aktív másolat állapotát megkapja.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="9bfd4-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9bfd4-124">PARAMETERS</span></span>

### <span data-ttu-id="9bfd4-125">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="9bfd4-125">-Database</span></span>
<span data-ttu-id="9bfd4-126">Egy olyan objektumot ad meg, amely a Source Azure SQL-adatbázist jelöli.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="9bfd4-127">Ez a parancsmag a paraméter által megadott adatbázis másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="9bfd4-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="9bfd4-128">-DatabaseCopy</span></span>
<span data-ttu-id="9bfd4-129">Egy adatbázist jelképező objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="9bfd4-130">Ez a parancsmag a paraméter által megadott adatbázis másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="9bfd4-131">Ez a paraméter elfogadja a csővezeték-bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="9bfd4-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9bfd4-132">-DatabaseName</span></span>
<span data-ttu-id="9bfd4-133">A forrás adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="9bfd4-134">Ez a parancsmag a paraméter által megadott adatbázis másolati állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bfd4-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="9bfd4-135">-PartnerDatabase</span></span>
<span data-ttu-id="9bfd4-136">A másodlagos adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="9bfd4-137">Ha az adatbázis nem található meg a sys.dm_database_copies dinamikus kezelés nézetében, ez a parancsmag üres állapot-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bfd4-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="9bfd4-138">-PartnerServer</span></span>
<span data-ttu-id="9bfd4-139">A célként megadott adatbázist tároló kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="9bfd4-140">Ha a kiszolgáló nem található meg a sys.dm_database_copies dinamikus kezelés nézetében, ez a parancsmag üres állapot-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bfd4-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="9bfd4-141">-Profile</span></span>
<span data-ttu-id="9bfd4-142">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9bfd4-143">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9bfd4-144">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="9bfd4-144">-ServerName</span></span>
<span data-ttu-id="9bfd4-145">Annak a kiszolgálónak a nevét adja meg, amelyen az adatbázis-másolat található.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="9bfd4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bfd4-146">CommonParameters</span></span>
<span data-ttu-id="9bfd4-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9bfd4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bfd4-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bfd4-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bfd4-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bfd4-149">INPUTS</span></span>

### <span data-ttu-id="9bfd4-150">Microsoft. WindowsAzure. Command. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="9bfd4-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="9bfd4-151">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="9bfd4-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="9bfd4-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bfd4-152">OUTPUTS</span></span>

### <span data-ttu-id="9bfd4-153">Microsoft. WindowsAzure. Command. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="9bfd4-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="9bfd4-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9bfd4-154">NOTES</span></span>
* <span data-ttu-id="9bfd4-155">Hitelesítés: Ez a parancsmag tanúsítvány-alapú hitelesítést követel meg.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="9bfd4-156">Példa arra, hogy hogyan állíthatja be a jelenlegi előfizetést tanúsítványalapú hitelesítéssel, ha az New-AzureSqlDatabaseServerContext parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="9bfd4-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="9bfd4-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bfd4-157">RELATED LINKS</span></span>

[<span data-ttu-id="9bfd4-158">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="9bfd4-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="9bfd4-159">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="9bfd4-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="9bfd4-160">Azure SQL-adatbázis-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9bfd4-160">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="9bfd4-161">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="9bfd4-161">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="9bfd4-162">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="9bfd4-162">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


