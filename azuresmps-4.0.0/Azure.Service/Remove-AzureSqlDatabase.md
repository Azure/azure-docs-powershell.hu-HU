---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016108"
---
# <span data-ttu-id="d7bfe-101">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d7bfe-101">Remove-AzureSqlDatabase</span></span>

## <span data-ttu-id="d7bfe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bfe-103">Azure SQL-adatbázis törlése</span><span class="sxs-lookup"><span data-stu-id="d7bfe-103">Deletes an Azure SQL Database.</span></span>

## <span data-ttu-id="d7bfe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7bfe-104">SYNTAX</span></span>

### <span data-ttu-id="d7bfe-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="d7bfe-105">ByNameWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7bfe-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="d7bfe-106">ByObjectWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7bfe-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="d7bfe-107">ByNameWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7bfe-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="d7bfe-108">ByObjectWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7bfe-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7bfe-109">DESCRIPTION</span></span>
<span data-ttu-id="d7bfe-110">A **Remove-AzureSqlDatabase** parancsmag a kiszolgáló kapcsolati környezete vagy a kiszolgálónév alapján törli az Azure SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-110">The **Remove-AzureSqlDatabase** cmdlet deletes an Azure SQL Database by server connection context or server name.</span></span>
<span data-ttu-id="d7bfe-111">Az Azure SQL Database Server kapcsolati környezetét a **New-AzureSqlDatabaseServerContext** parancsmaggal hozhatja létre, és ezt a parancsmagot használva használhatja.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-111">You can create an Azure SQL Database server connection context using the **New-AzureSqlDatabaseServerContext** cmdlet, and then use it with this cmdlet.</span></span>

<span data-ttu-id="d7bfe-112">Ha egy adatbázist egy Azure SQL-adatbázis kiszolgálójának megadásával törlünk, a **Remove-AzureSqlDatabase** parancsmag a nevet és az aktuális Azure-előfizetési adatokat használja a művelet végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-112">When you delete a database by specifying an Azure SQL Database server name, the **Remove-AzureSqlDatabase** cmdlet uses the name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="d7bfe-113">Példák</span><span class="sxs-lookup"><span data-stu-id="d7bfe-113">EXAMPLES</span></span>

### <span data-ttu-id="d7bfe-114">1. példa: adatbázis eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d7bfe-114">Example 1: Remove a database</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="d7bfe-115">Ez a parancs eltávolítja az Database01 nevű adatbázist az Azure SQL Database Server kapcsolati környezetből $Contextból.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-115">This command removes the database named Database01 from the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="d7bfe-116">2. példa: adatbázis eltávolítása kiszolgálónév használatával</span><span class="sxs-lookup"><span data-stu-id="d7bfe-116">Example 2: Remove a database by using a server name</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="d7bfe-117">Ez a parancs eltávolítja a Database01 nevű adatbázist az lpqd0zbr8y nevű Azure SQL adatbázis-kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-117">This command removes the database named Database01 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="d7bfe-118">3. példa: adatbázis eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="d7bfe-118">Example 3: Remove a database by using the pipeline</span></span>
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="d7bfe-119">Ez a példa bemutatja az adatbázis-objektum csővezetéken keresztüli továbbításának alternatív módszerét.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-119">This example demonstrates the alternative method of passing the database object through the pipeline.</span></span>

## <span data-ttu-id="d7bfe-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7bfe-120">PARAMETERS</span></span>

### <span data-ttu-id="d7bfe-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="d7bfe-121">-ConnectionContext</span></span>
<span data-ttu-id="d7bfe-122">Annak a kiszolgálónak a kapcsolati környezetét adja meg, amelyből a parancsmag eltávolítja az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-122">Specifies the connection context of a server from which this cmdlet removes a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7bfe-123">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="d7bfe-123">-Database</span></span>
<span data-ttu-id="d7bfe-124">Egy olyan objektumot ad meg, amely a parancsmag által eltávolított adatbázisnak felel meg.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-124">Specifies an object that represents the database that this cmdlet removes.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7bfe-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7bfe-125">-DatabaseName</span></span>
<span data-ttu-id="d7bfe-126">Annak az adatbázisnak a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-126">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bfe-127">-Force</span><span class="sxs-lookup"><span data-stu-id="d7bfe-127">-Force</span></span>
<span data-ttu-id="d7bfe-128">Lehetővé teszi, hogy a művelet a felhasználó megerősítésének megkérdezése nélkül legyen elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-128">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="d7bfe-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="d7bfe-129">-Profile</span></span>
<span data-ttu-id="d7bfe-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d7bfe-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d7bfe-132">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d7bfe-132">-ServerName</span></span>
<span data-ttu-id="d7bfe-133">Annak a kiszolgálónak a nevét adja meg, amelyen a parancsmag törli az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-133">Specifies the name of the server on which this cmdlet deletes the database.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7bfe-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7bfe-134">-Confirm</span></span>
<span data-ttu-id="d7bfe-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7bfe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7bfe-136">-WhatIf</span></span>
<span data-ttu-id="d7bfe-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7bfe-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7bfe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bfe-139">CommonParameters</span></span>
<span data-ttu-id="d7bfe-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7bfe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bfe-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7bfe-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bfe-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7bfe-142">INPUTS</span></span>

### <span data-ttu-id="d7bfe-143">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="d7bfe-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="d7bfe-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7bfe-144">OUTPUTS</span></span>

## <span data-ttu-id="d7bfe-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7bfe-145">NOTES</span></span>
* <span data-ttu-id="d7bfe-146">A művelet súlyossága miatt alapértelmezés szerint ez a parancsmag kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-146">Because of the severity of the operation, by default, this cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="d7bfe-147">A megerősítés kihagyásához adja meg az *erő* paramétert.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-147">To skip confirmation, specify the *Force* parameter.</span></span>

## <span data-ttu-id="d7bfe-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7bfe-148">RELATED LINKS</span></span>

[<span data-ttu-id="d7bfe-149">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="d7bfe-149">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="d7bfe-150">Adatbázis törlése</span><span class="sxs-lookup"><span data-stu-id="d7bfe-150">Delete Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[<span data-ttu-id="d7bfe-151">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="d7bfe-151">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="d7bfe-152">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d7bfe-152">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="d7bfe-153">Új – AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d7bfe-153">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="d7bfe-154">Új – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="d7bfe-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="d7bfe-155">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d7bfe-155">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


