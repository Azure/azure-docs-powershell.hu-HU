---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015845"
---
# <span data-ttu-id="96f79-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="96f79-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="96f79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96f79-102">SYNOPSIS</span></span>
<span data-ttu-id="96f79-103">Egy Azure SQL-adatbázis másolási műveletét indítja el.</span><span class="sxs-lookup"><span data-stu-id="96f79-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="96f79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96f79-104">SYNTAX</span></span>

### <span data-ttu-id="96f79-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="96f79-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f79-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="96f79-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f79-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="96f79-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f79-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="96f79-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96f79-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="96f79-109">DESCRIPTION</span></span>
<span data-ttu-id="96f79-110">A **Start-AzureSqlDatabaseCopy** parancsmag egyszeres másolási műveletet vagy egy bizonyos Azure SQL-adatbázis folyamatos másolási műveletét indítja el.</span><span class="sxs-lookup"><span data-stu-id="96f79-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="96f79-111">Ez a parancsmag nem tranzakciós.</span><span class="sxs-lookup"><span data-stu-id="96f79-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="96f79-112">Az eredeti adatbázis a forrás adatbázis.</span><span class="sxs-lookup"><span data-stu-id="96f79-112">The original database is the source database.</span></span>
<span data-ttu-id="96f79-113">A másolat a másodlagos vagy a cél adatbázis.</span><span class="sxs-lookup"><span data-stu-id="96f79-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="96f79-114">Folyamatos másolás esetén a forrás-és a célként megadott adatbázis nem használható ugyanazon a kiszolgálón, és a forrás-és a célként megadott adatbázisokat tároló kiszolgálók ugyanahhoz az előfizetéshez tartoznak.</span><span class="sxs-lookup"><span data-stu-id="96f79-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="96f79-115">Ha nem adja meg a *ContinuousCopy* paramétert, ez a parancsmag a forrásadatbázis egyszer használatos példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="96f79-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="96f79-116">A válasz fogadásakor a művelet továbbra is folyamatban van.</span><span class="sxs-lookup"><span data-stu-id="96f79-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="96f79-117">A műveletet a Get-AzureSqlDatabaseCopy vagy Get-AzureSqlDatabaseOperation parancsmag használatával figyelheti.</span><span class="sxs-lookup"><span data-stu-id="96f79-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="96f79-118">Ha megad egy *ContinuousCopy* , ez a parancsmag létrehoz egy folytonos másolatot a forrás adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="96f79-118">If you specify *ContinuousCopy* , this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="96f79-119">Ha a válasz érkezik, a művelet folyamatban lesz.</span><span class="sxs-lookup"><span data-stu-id="96f79-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="96f79-120">A műveletet a **Get-AzureSqlDatabaseCopy** vagy a **Get-AzureSqlDatabaseOperation** segítségével is figyelheti.</span><span class="sxs-lookup"><span data-stu-id="96f79-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="96f79-121">Folyamatos másolatot hozhat létre online vagy offline adatbázisként.</span><span class="sxs-lookup"><span data-stu-id="96f79-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="96f79-122">Az online folytonos másolat az aktív Geo-Replication Azure SQL-adatbázis konfigurálására szolgál https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .</span><span class="sxs-lookup"><span data-stu-id="96f79-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="96f79-123">A kapcsolat nélküli folyamatos másolat az Azure SQL-adatbázis normál Geo-Replicationének konfigurálására szolgál https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .</span><span class="sxs-lookup"><span data-stu-id="96f79-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="96f79-124">Példák</span><span class="sxs-lookup"><span data-stu-id="96f79-124">EXAMPLES</span></span>

### <span data-ttu-id="96f79-125">Példa 1: folytonos adatbázis-példány ütemezése</span><span class="sxs-lookup"><span data-stu-id="96f79-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="96f79-126">Ez a parancs a lpqd0zbr8y nevű kiszolgálón a rendelések nevű adatbázis folyamatos másolatát ütemezi.</span><span class="sxs-lookup"><span data-stu-id="96f79-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="96f79-127">A parancs létrehoz egy céladatbáziset a bk0b8kf658 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="96f79-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="96f79-128">2. példa: egyidejű másolat létrehozása ugyanazon a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="96f79-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="96f79-129">Ezzel a paranccsal létrehozhatja a lpqd0zbr8y nevű kiszolgálón a rendelések nevű adatbázis egyszeres másolatát.</span><span class="sxs-lookup"><span data-stu-id="96f79-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="96f79-130">A parancs létrehoz egy OrdersCopy nevű példányt ugyanazon a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="96f79-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="96f79-131">3. példa: folyamatos Offline adatbázis-példány ütemezése</span><span class="sxs-lookup"><span data-stu-id="96f79-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="96f79-132">Ez a parancs a lpqd0zbr8y nevű kiszolgálón a rendelések nevű adatbázis folyamatos másolatát ütemezi.</span><span class="sxs-lookup"><span data-stu-id="96f79-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="96f79-133">Ez a parancs létrehoz egy offline céladatbázis-adatbázist a bk0b8kf658 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="96f79-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="96f79-134">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96f79-134">PARAMETERS</span></span>

### <span data-ttu-id="96f79-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="96f79-135">-ContinuousCopy</span></span>
<span data-ttu-id="96f79-136">Azt jelzi, hogy az adatbázis másolása folyamatos másolatként (replika-adatbázis) fog szerepelni.</span><span class="sxs-lookup"><span data-stu-id="96f79-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="96f79-137">A folyamatos másolás nem támogatott ugyanazon a kiszolgálón belül.</span><span class="sxs-lookup"><span data-stu-id="96f79-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="96f79-138">Ha ez a paraméter nincs megadva, az alkalmazás egyszeres másolatot hajt végre.</span><span class="sxs-lookup"><span data-stu-id="96f79-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="96f79-139">Egyszeres másolat esetén a forrás-és a partner adatbázisnak ugyanazon a kiszolgálón kell lennie.</span><span class="sxs-lookup"><span data-stu-id="96f79-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f79-140">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="96f79-140">-Database</span></span>
<span data-ttu-id="96f79-141">Egy olyan objektumot ad meg, amely a Source Azure SQL-adatbázist jelöli.</span><span class="sxs-lookup"><span data-stu-id="96f79-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="96f79-142">Ez a paraméter elfogadja a csővezeték-bevitelt.</span><span class="sxs-lookup"><span data-stu-id="96f79-142">This parameter accepts pipeline input.</span></span>

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96f79-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="96f79-143">-DatabaseName</span></span>
<span data-ttu-id="96f79-144">A forrás adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96f79-144">Specifies the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f79-145">-Force</span><span class="sxs-lookup"><span data-stu-id="96f79-145">-Force</span></span>
<span data-ttu-id="96f79-146">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="96f79-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96f79-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="96f79-147">-OfflineSecondary</span></span>
<span data-ttu-id="96f79-148">Azt adja meg, hogy egy folytonos másolat nem aktív másolat, hanem passzív másolat.</span><span class="sxs-lookup"><span data-stu-id="96f79-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="96f79-149">Ha a forrásadatbázis normál kiadású adatbázis, akkor ez a paraméter szükséges.</span><span class="sxs-lookup"><span data-stu-id="96f79-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="96f79-150">Ha ezt a paramétert adja meg, akkor a *ContinuousCopy* is meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="96f79-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f79-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="96f79-151">-PartnerDatabase</span></span>
<span data-ttu-id="96f79-152">A céladatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96f79-152">Specifies name of the target database.</span></span>
<span data-ttu-id="96f79-153">Ha a *ContinuousCopy* paramétert adja meg, a *PartnerDatabase* értékének egyeznie kell a forrás adatbázis nevével.</span><span class="sxs-lookup"><span data-stu-id="96f79-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="96f79-154">Ha nem adja meg a *ContinuousCopy* , meg kell adnia a céladatbázis nevét, amely a forrás adatbázis nevétől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="96f79-154">If you do not specify *ContinuousCopy* , you must specify a name for the target database, which can be different from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f79-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="96f79-155">-PartnerServer</span></span>
<span data-ttu-id="96f79-156">A célként megadott adatbázist tároló kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="96f79-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="96f79-157">A kiszolgálónak ugyanazon az Azure-előfizetésben kell lennie, mint a forrás adatbázis-kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="96f79-157">This server must be in the same Azure subscription as the source database server.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f79-158">-Profil</span><span class="sxs-lookup"><span data-stu-id="96f79-158">-Profile</span></span>
<span data-ttu-id="96f79-159">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="96f79-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="96f79-160">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="96f79-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="96f79-161">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="96f79-161">-ServerName</span></span>
<span data-ttu-id="96f79-162">Annak a kiszolgálónak a nevét adja meg, amelyen a forrás adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="96f79-162">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="96f79-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96f79-163">-Confirm</span></span>
<span data-ttu-id="96f79-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96f79-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96f79-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96f79-165">-WhatIf</span></span>
<span data-ttu-id="96f79-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96f79-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96f79-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96f79-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96f79-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f79-168">CommonParameters</span></span>
<span data-ttu-id="96f79-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96f79-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f79-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96f79-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f79-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96f79-171">INPUTS</span></span>

### <span data-ttu-id="96f79-172">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="96f79-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="96f79-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96f79-173">OUTPUTS</span></span>

### <span data-ttu-id="96f79-174">Microsoft. WindowsAzure. Command. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="96f79-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="96f79-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96f79-175">NOTES</span></span>
* <span data-ttu-id="96f79-176">Hitelesítés: Ez a parancsmag tanúsítvány-alapú hitelesítést követel meg.</span><span class="sxs-lookup"><span data-stu-id="96f79-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="96f79-177">Ha egy példa arra, hogy hogyan állíthatja be az aktuális előfizetést tanúsítványalapú hitelesítéssel, olvassa el New-AzureSqlDatabaseServerContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="96f79-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="96f79-178">Figyelés: Ha a kiszolgálón aktív egy vagy több folyamatos másolási kapcsolat állapotát szeretné ellenőrizni, használja a **Get-AzureSqlDatabaseCopy** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="96f79-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="96f79-179">Ha ellenőrizni szeretné a műveletek állapotát a folyamatos másolási kapcsolat forrása és célja között, használja a **Get-AzureSqlDatabaseOperation** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="96f79-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="96f79-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96f79-180">RELATED LINKS</span></span>

[<span data-ttu-id="96f79-181">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="96f79-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="96f79-182">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="96f79-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="96f79-183">Adatbázis-másolat indítása</span><span class="sxs-lookup"><span data-stu-id="96f79-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[<span data-ttu-id="96f79-184">Azure SQL-adatbázis-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="96f79-184">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="96f79-185">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="96f79-185">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="96f79-186">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="96f79-186">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


