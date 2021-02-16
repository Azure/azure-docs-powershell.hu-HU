---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402422"
---
# <span data-ttu-id="4556d-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4556d-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="4556d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4556d-102">SYNOPSIS</span></span>
<span data-ttu-id="4556d-103">A másolási kapcsolatok állapotát ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="4556d-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="4556d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4556d-104">SYNTAX</span></span>

### <span data-ttu-id="4556d-105">ByServerNameOnly (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4556d-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4556d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4556d-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="4556d-107">Adatbázis-adatbázis</span><span class="sxs-lookup"><span data-stu-id="4556d-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4556d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4556d-108">DESCRIPTION</span></span>
<span data-ttu-id="4556d-109">A **Get-AzureSqlDatabaseCopy** parancsmag egy vagy több aktív másolási kapcsolat állapotát ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="4556d-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="4556d-110">Futtassa ezt a parancsmagot a Start-AzureSqlDatabaseCopy vagy Stop-AzureSqlDatabaseCopy futtatása után.</span><span class="sxs-lookup"><span data-stu-id="4556d-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="4556d-111">Ellenőrizheti egy adott másolási kapcsolatot, az összes másolási kapcsolatot vagy a másolási kapcsolatok szűrt listáját, például egy adott célkiszolgáló összes példányát.</span><span class="sxs-lookup"><span data-stu-id="4556d-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="4556d-112">Ezt a parancsmagot a forrás- vagy céladatbázist tároló kiszolgálón futtathatja.</span><span class="sxs-lookup"><span data-stu-id="4556d-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="4556d-113">Ez a parancsmag szinkron.</span><span class="sxs-lookup"><span data-stu-id="4556d-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="4556d-114">A parancsmag letiltja az Azure PowerShell-konzolt, amíg egy állapotobjektumot nem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="4556d-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="4556d-115">A *PartnerServer* és *a PartnerDatabase* paraméter megadása nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4556d-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="4556d-116">Ha egyik paramétert sem adja meg, ez a parancsmag eredménytáblát ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="4556d-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="4556d-117">Ha csak egy adott adatbázis állapotát látni, adja meg mindkét paramétert.</span><span class="sxs-lookup"><span data-stu-id="4556d-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="4556d-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4556d-118">EXAMPLES</span></span>

### <span data-ttu-id="4556d-119">1. példa: Adatbázis másolási állapotának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="4556d-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="4556d-120">Ez a parancs az Orders (Rendelések) nevű adatbázis állapotát kapja meg az lpqd0zbr8y nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="4556d-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="4556d-121">A *PartnerServer* paraméter a parancsot a bk0b8kf658-kiszolgálóra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="4556d-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="4556d-122">2. példa: A kiszolgálón található összes példány állapotának ellenőrzéseA kiszolgálón található összes példány állapotának megtekintése</span><span class="sxs-lookup"><span data-stu-id="4556d-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="4556d-123">Ez a parancs az lpqd0zbr8y nevű kiszolgálón lévő összes aktív példány állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4556d-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="4556d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4556d-124">PARAMETERS</span></span>

### <span data-ttu-id="4556d-125">-Database</span><span class="sxs-lookup"><span data-stu-id="4556d-125">-Database</span></span>
<span data-ttu-id="4556d-126">A forrás Azure SQL-adatbázist képviselő objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4556d-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="4556d-127">Ez a parancsmag a paraméter által megadott adatbázis másolási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4556d-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="4556d-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4556d-128">-DatabaseCopy</span></span>
<span data-ttu-id="4556d-129">Egy adatbázist képviselő objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4556d-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="4556d-130">Ez a parancsmag a paraméter által megadott adatbázis másolási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4556d-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="4556d-131">Ez a paraméter elfogadja a folyamatbemenetet.</span><span class="sxs-lookup"><span data-stu-id="4556d-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="4556d-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4556d-132">-DatabaseName</span></span>
<span data-ttu-id="4556d-133">A forrásadatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4556d-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="4556d-134">Ez a parancsmag a paraméter által megadott adatbázis másolási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4556d-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="4556d-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="4556d-135">-PartnerDatabase</span></span>
<span data-ttu-id="4556d-136">A másodlagos adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4556d-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="4556d-137">Ha ez az adatbázis nem található meg a sys.dm_database_copies dinamikus kezelési nézetben, ez a parancsmag üres állapotobjektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="4556d-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="4556d-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="4556d-138">-PartnerServer</span></span>
<span data-ttu-id="4556d-139">A céladatbázist tároló kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="4556d-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="4556d-140">Ha ez a kiszolgáló nem található meg a sys.dm_database_copies dinamikus kezelési nézetben, ez a parancsmag üres állapotobjektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="4556d-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="4556d-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="4556d-141">-Profile</span></span>
<span data-ttu-id="4556d-142">Azt az Azure-profilt adja meg, amelyből a parancsmag olvas.</span><span class="sxs-lookup"><span data-stu-id="4556d-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4556d-143">Ha nem ad meg profilt, ez a parancsmag a helyi alapértelmezett profilból olvassa be.</span><span class="sxs-lookup"><span data-stu-id="4556d-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4556d-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4556d-144">-ServerName</span></span>
<span data-ttu-id="4556d-145">Annak a kiszolgálónak a nevét adja meg, amelyen az adatbázis másolata található.</span><span class="sxs-lookup"><span data-stu-id="4556d-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="4556d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4556d-146">CommonParameters</span></span>
<span data-ttu-id="4556d-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4556d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4556d-148">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4556d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4556d-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4556d-149">INPUTS</span></span>

### <span data-ttu-id="4556d-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4556d-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="4556d-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="4556d-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="4556d-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4556d-152">OUTPUTS</span></span>

### <span data-ttu-id="4556d-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4556d-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="4556d-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4556d-154">NOTES</span></span>
* <span data-ttu-id="4556d-155">Hitelesítés: Ez a parancsmag tanúsítványalapú hitelesítést igényel.</span><span class="sxs-lookup"><span data-stu-id="4556d-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="4556d-156">Ha például tanúsítványalapú hitelesítéssel állíthatja be az aktuális előfizetést, tekintse meg a New-AzureSqlDatabaseServerContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4556d-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="4556d-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4556d-157">RELATED LINKS</span></span>

[<span data-ttu-id="4556d-158">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="4556d-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="4556d-159">Műveletek az Azure SQL-adatbázisokban</span><span class="sxs-lookup"><span data-stu-id="4556d-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[<span data-ttu-id="4556d-160">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4556d-160">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="4556d-161">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4556d-161">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


