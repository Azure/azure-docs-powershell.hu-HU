---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016293"
---
# <span data-ttu-id="0d75d-101">Get-AzureSqlDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="0d75d-101">Get-AzureSqlDatabaseOperation</span></span>

## <span data-ttu-id="0d75d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d75d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d75d-103">Az adatbázis-műveletek állapotát egy Azure-kiszolgálón kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0d75d-103">Gets the status of database operations on an Azure server.</span></span>

## <span data-ttu-id="0d75d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d75d-104">SYNTAX</span></span>

### <span data-ttu-id="0d75d-105">ByConnectionContext (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d75d-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0d75d-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="0d75d-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0d75d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d75d-107">DESCRIPTION</span></span>
<span data-ttu-id="0d75d-108">A **Get-AzureSqlDatabaseOperation** parancsmag az adatbázis-műveletek állapotát a megadott Azure-kiszolgálón kapja.</span><span class="sxs-lookup"><span data-stu-id="0d75d-108">The **Get-AzureSqlDatabaseOperation** cmdlet gets the status of database operations on the specified Azure server.</span></span>
<span data-ttu-id="0d75d-109">Ha csak a *kiszolgálónév* vagy a *ConnectionContext* paramétert adja meg, a parancsmag minden adatbázis-műveletet megkapja a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="0d75d-109">If you specify only the *ServerName* or *ConnectionContext* parameter, the cmdlet gets all the database operations for the server.</span></span>
<span data-ttu-id="0d75d-110">Ha az *adatbázis* vagy a *databasename* paraméter használatával is megadhat egy adatbázist, ez a parancsmag a megadott adatbázis összes műveletét megkapja.</span><span class="sxs-lookup"><span data-stu-id="0d75d-110">If you also specify a database by using the *Database* or *DatabaseName* parameter, this cmdlet gets all the operations for the specified database.</span></span>
<span data-ttu-id="0d75d-111">Ha megad egy műveleti GUID azonosítót, a *kiszolgálónév* vagy a *ConnectionContext* , a parancsmag egyetlen adatbázis-műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="0d75d-111">If you specify an operation GUID, and *ServerName* or *ConnectionContext* , the cmdlet gets a single database operation.</span></span>

## <span data-ttu-id="0d75d-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0d75d-112">EXAMPLES</span></span>

### <span data-ttu-id="0d75d-113">Példa 1: adatbázis minden adatbázis-műveletének állapotának lekérése</span><span class="sxs-lookup"><span data-stu-id="0d75d-113">Example 1: Get the status of all database operations for a database</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

<span data-ttu-id="0d75d-114">Ez a parancs a kiszolgálón a Database17 nevű adatbázis minden műveletének állapotát beolvassa, és a kapcsolati környezet $Context adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d75d-114">This command gets the status of all database operations on the database named Database17 on the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="0d75d-115">2. példa: a kiszolgáló összes adatbázis-művelete állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="0d75d-115">Example 2: Get the status of all database operations for a server</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

<span data-ttu-id="0d75d-116">Ez a parancs minden olyan adatbázis-művelet állapotát megjeleníti a kiszolgálón, amelyen a kapcsolati környezet $Context meg van határozva.</span><span class="sxs-lookup"><span data-stu-id="0d75d-116">This command gets the status of all database operations on the server that the connection context $Context specifies.</span></span>

## <span data-ttu-id="0d75d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d75d-117">PARAMETERS</span></span>

### <span data-ttu-id="0d75d-118">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="0d75d-118">-ConnectionContext</span></span>
<span data-ttu-id="0d75d-119">A kiszolgáló kapcsolati környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d75d-119">Specifies the connection context of a server.</span></span>

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

### <span data-ttu-id="0d75d-120">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="0d75d-120">-Database</span></span>
<span data-ttu-id="0d75d-121">Egy Azure SQL-adatbázist jelképező objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0d75d-121">Specifies an object that represents an Azure SQL Database.</span></span>
<span data-ttu-id="0d75d-122">Ha ezt a paramétert adja meg, a *kiszolgálónév* paramétert vagy a *ConnectionContext* paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="0d75d-122">If you specify this parameter, you must specify the *ServerName* parameter or *ConnectionContext* parameter.</span></span>

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

### <span data-ttu-id="0d75d-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0d75d-123">-DatabaseName</span></span>
<span data-ttu-id="0d75d-124">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d75d-124">Specifies the name of a database.</span></span>
<span data-ttu-id="0d75d-125">Ha ezt a paramétert adja meg, a *kiszolgálónév* paramétert vagy a *ConnectionContext* paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="0d75d-125">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d75d-126">-OperationGuid</span><span class="sxs-lookup"><span data-stu-id="0d75d-126">-OperationGuid</span></span>
<span data-ttu-id="0d75d-127">Azt a műveleti azonosítót adja meg, amely egy bizonyos adatbázis-műveletnek felel meg, amelyre a parancsmag állapota bekerül.</span><span class="sxs-lookup"><span data-stu-id="0d75d-127">Specifies the operation ID that represents a specific database operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="0d75d-128">A műveleti azonosítók beolvasásához az Azure SQL-adatbázisok vagy-kiszolgálók összes adatbázis-műveletét kéri.</span><span class="sxs-lookup"><span data-stu-id="0d75d-128">You can obtain operation IDs by requesting all the database operations for a Azure SQL Database or server.</span></span>
<span data-ttu-id="0d75d-129">Ha ezt a paramétert adja meg, a *kiszolgálónév* paramétert vagy a *ConnectionContext* paramétert kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="0d75d-129">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d75d-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="0d75d-130">-Profile</span></span>
<span data-ttu-id="0d75d-131">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0d75d-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0d75d-132">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0d75d-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0d75d-133">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0d75d-133">-ServerName</span></span>
<span data-ttu-id="0d75d-134">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d75d-134">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="0d75d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d75d-135">CommonParameters</span></span>
<span data-ttu-id="0d75d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d75d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d75d-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d75d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d75d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d75d-138">INPUTS</span></span>

### <span data-ttu-id="0d75d-139">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="0d75d-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="0d75d-140">Microsoft. WindowsAzure. Command. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="0d75d-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

### <span data-ttu-id="0d75d-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0d75d-141">System.Guid</span></span>

## <span data-ttu-id="0d75d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d75d-142">OUTPUTS</span></span>

### <span data-ttu-id="0d75d-143">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. database. DatabaseOperationResponseList []</span><span class="sxs-lookup"><span data-stu-id="0d75d-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponseList[]</span></span>
<span data-ttu-id="0d75d-144">Ez a parancsmag egy **DatabaseOperationResponseList** -objektumokból álló tömböt ad eredményül, ha több műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="0d75d-144">This cmdlet returns an array of **DatabaseOperationResponseList** objects if you get multiple operations.</span></span>

### <span data-ttu-id="0d75d-145">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. database. DatabaseOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0d75d-145">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponse</span></span>

## <span data-ttu-id="0d75d-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d75d-146">NOTES</span></span>

## <span data-ttu-id="0d75d-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d75d-147">RELATED LINKS</span></span>

[<span data-ttu-id="0d75d-148">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="0d75d-148">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="0d75d-149">Adatbázis-művelet állapota</span><span class="sxs-lookup"><span data-stu-id="0d75d-149">Database Operation Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[<span data-ttu-id="0d75d-150">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="0d75d-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="0d75d-151">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d75d-151">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="0d75d-152">Új – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="0d75d-152">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


