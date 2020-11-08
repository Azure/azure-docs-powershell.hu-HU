---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015423"
---
# <span data-ttu-id="6a604-101">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="6a604-101">Start-AzureSqlDatabaseRecovery</span></span>

## <span data-ttu-id="6a604-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a604-102">SYNOPSIS</span></span>
<span data-ttu-id="6a604-103">Egy adatbázis visszaállítási kérését kezdeményezi.</span><span class="sxs-lookup"><span data-stu-id="6a604-103">Initiates a restore request for a database.</span></span>

## <span data-ttu-id="6a604-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a604-104">SYNTAX</span></span>

### <span data-ttu-id="6a604-105">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a604-105">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6a604-106">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="6a604-106">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6a604-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a604-107">DESCRIPTION</span></span>
<span data-ttu-id="6a604-108">A **Start-AzureSqlDatabaseRecovery** parancsmag visszahívási kérést kezdeményez egy élő vagy ledobott adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="6a604-108">The **Start-AzureSqlDatabaseRecovery** cmdlet initiates a restore request for a live or dropped database.</span></span>
<span data-ttu-id="6a604-109">Ez a parancsmag támogatja az adatbázis utolsó ismert elérhető biztonsági másolatát használó alapszintű helyreállítást.</span><span class="sxs-lookup"><span data-stu-id="6a604-109">This cmdlet supports basic recovery that uses the last known available backup for the database.</span></span>
<span data-ttu-id="6a604-110">A helyreállítási művelet új adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6a604-110">The recovery operation creates a new database.</span></span>
<span data-ttu-id="6a604-111">Ha ugyanazon a kiszolgálón visszaállít egy élő adatbázist, az új adatbázisnak meg kell adnia egy másik nevet.</span><span class="sxs-lookup"><span data-stu-id="6a604-111">If you recover a live database on the same server, you must specify a different name for the new database.</span></span>

<span data-ttu-id="6a604-112">Ha egy adatbázis időpontját szeretné visszaállítani, használja inkább a **Start-AzureSqlDatabaseRestore** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6a604-112">To do a point in time restore for a database, use the **Start-AzureSqlDatabaseRestore** cmdlet instead.</span></span>

## <span data-ttu-id="6a604-113">Példák</span><span class="sxs-lookup"><span data-stu-id="6a604-113">EXAMPLES</span></span>

### <span data-ttu-id="6a604-114">Példa 1: objektumként megadott adatbázis helyreállítása</span><span class="sxs-lookup"><span data-stu-id="6a604-114">Example 1: Recover a database specified as an object</span></span>
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="6a604-115">Az első parancs az adatbázis-objektumot a **Get-AzureSqlRecoverableDatabase** parancsmag segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6a604-115">The first command gets a database object by using the **Get-AzureSqlRecoverableDatabase** cmdlet.</span></span>
<span data-ttu-id="6a604-116">A parancs az objektumot a $Database változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6a604-116">The command stores that object in the $Database variable.</span></span>

<span data-ttu-id="6a604-117">A második parancs visszanyeri az adatbázis $Database-ban tárolt adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="6a604-117">The second command recovers the database stored in $Database.</span></span>

### <span data-ttu-id="6a604-118">2. példa: név szerint megadott adatbázis helyreállítása</span><span class="sxs-lookup"><span data-stu-id="6a604-118">Example 2: Recover a database specified by name</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="6a604-119">A parancs az adatbázis nevével visszanyeri az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="6a604-119">This command recovers a database using the database name.</span></span>

## <span data-ttu-id="6a604-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a604-120">PARAMETERS</span></span>

### <span data-ttu-id="6a604-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="6a604-121">-Profile</span></span>
<span data-ttu-id="6a604-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6a604-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6a604-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6a604-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6a604-124">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="6a604-124">-SourceDatabase</span></span>
<span data-ttu-id="6a604-125">Azt az adatbázis-objektumot adja meg, amely a parancsmag által helyreállított adatbázisnak felel meg.</span><span class="sxs-lookup"><span data-stu-id="6a604-125">Specifies the database object that represents the database that this cmdlet recovers.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a604-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a604-126">-SourceDatabaseName</span></span>
<span data-ttu-id="6a604-127">Annak az adatbázisnak a nevét adja meg, amelyre a parancsmag visszanyeri.</span><span class="sxs-lookup"><span data-stu-id="6a604-127">Specifies the name of the database that this cmdlet recovers.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a604-128">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="6a604-128">-SourceServerName</span></span>
<span data-ttu-id="6a604-129">Annak a kiszolgálónak a neve, amelyen a forrásadatbázis él és fut, vagy amelyen a forrásadatbázis a törlés előtt futott.</span><span class="sxs-lookup"><span data-stu-id="6a604-129">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a604-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a604-130">-TargetDatabaseName</span></span>
<span data-ttu-id="6a604-131">A helyreállított adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a604-131">Specifies the name of the recovered database.</span></span>
<span data-ttu-id="6a604-132">Ha a forrásadatbázis továbbra is él, a forrás-adatbázis nevétől eltérő nevet kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="6a604-132">If the source database is still live, in order to recover it to the same server, you must specify a name that differs from the source database name.</span></span>

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

### <span data-ttu-id="6a604-133">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="6a604-133">-TargetServerName</span></span>
<span data-ttu-id="6a604-134">Megadja annak a kiszolgálónak a nevét, amelynek az adatbázisát vissza szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="6a604-134">Specifies the name of the server to which to restore a database.</span></span>
<span data-ttu-id="6a604-135">Egy adatbázis visszaállítható ugyanazon a kiszolgálón vagy egy másik kiszolgálón is.</span><span class="sxs-lookup"><span data-stu-id="6a604-135">You can restore a database to the same server or to a different server.</span></span>

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

### <span data-ttu-id="6a604-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a604-136">CommonParameters</span></span>
<span data-ttu-id="6a604-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a604-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a604-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a604-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a604-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a604-139">INPUTS</span></span>

### <span data-ttu-id="6a604-140">Microsoft. WindowsAzure. Management. SQL. models. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="6a604-140">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="6a604-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a604-141">OUTPUTS</span></span>

### <span data-ttu-id="6a604-142">Microsoft. WindowsAzure. Management. SQL. models. RecoverDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="6a604-142">Microsoft.WindowsAzure.Management.Sql.Models.RecoverDatabaseOperation</span></span>

## <span data-ttu-id="6a604-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a604-143">NOTES</span></span>
* <span data-ttu-id="6a604-144">A parancsmag futtatásához tanúsítványon alapuló hitelesítést kell használnia.</span><span class="sxs-lookup"><span data-stu-id="6a604-144">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="6a604-145">Futtassa az alábbi parancsokat azon a számítógépen, amelyen futtatja ezt a parancsmagot:</span><span class="sxs-lookup"><span data-stu-id="6a604-145">Run the following commands on the computer where you run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="6a604-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a604-146">RELATED LINKS</span></span>

[<span data-ttu-id="6a604-147">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="6a604-147">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="6a604-148">Adatbázis-helyreállítási kérés létrehozása</span><span class="sxs-lookup"><span data-stu-id="6a604-148">Create Database Recovery Request</span></span>](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[<span data-ttu-id="6a604-149">Geo-replikáció az Azure SQL-adatbázisban</span><span class="sxs-lookup"><span data-stu-id="6a604-149">Geo-Replication in Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[<span data-ttu-id="6a604-150">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="6a604-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="6a604-151">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="6a604-151">Get-AzureSqlRecoverableDatabase</span></span>](./Get-AzureSqlRecoverableDatabase.md)

[<span data-ttu-id="6a604-152">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="6a604-152">Start-AzureSqlDatabaseRestore</span></span>](./Start-AzureSqlDatabaseRestore.md)


