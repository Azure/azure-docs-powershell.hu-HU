---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413064"
---
# <span data-ttu-id="667cf-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="667cf-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="667cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="667cf-102">SYNOPSIS</span></span>
<span data-ttu-id="667cf-103">Egy Azure SQL-adatbázis másolási műveletének indítása.</span><span class="sxs-lookup"><span data-stu-id="667cf-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="667cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="667cf-104">SYNTAX</span></span>

### <span data-ttu-id="667cf-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="667cf-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667cf-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="667cf-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667cf-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="667cf-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667cf-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="667cf-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="667cf-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="667cf-109">DESCRIPTION</span></span>
<span data-ttu-id="667cf-110">A **Start-AzureSqlDatabaseCopy** parancsmag egy egyszeres másolási műveletet vagy egy adott Azure SQL-adatbázis folyamatos másolási műveletét indítja el.</span><span class="sxs-lookup"><span data-stu-id="667cf-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="667cf-111">Ez a parancsmag nem tranzakciós.</span><span class="sxs-lookup"><span data-stu-id="667cf-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="667cf-112">Az eredeti adatbázis a forrásadatbázis.</span><span class="sxs-lookup"><span data-stu-id="667cf-112">The original database is the source database.</span></span>
<span data-ttu-id="667cf-113">A másolat a másodlagos vagy céladatbázis.</span><span class="sxs-lookup"><span data-stu-id="667cf-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="667cf-114">Folyamatos másolat esetén a forrás- és céladatbázisok nem ugyanazon a kiszolgálón találhatók, és a forrás- és céladatbázisokat tároló kiszolgálóknak ugyanannak az előfizetésnek a részeinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="667cf-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="667cf-115">Ha nem adja meg a *ContinuousCopy* paramétert, ez a parancsmag a forrásadatbázis egy egyszer használható másolatát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="667cf-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="667cf-116">Amikor a válasz érkezik, a művelet továbbra is folyamatban lehet.</span><span class="sxs-lookup"><span data-stu-id="667cf-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="667cf-117">A műveletet figyelheti a Get-AzureSqlDatabaseCopy vagy Get-AzureSqlDatabaseOperation parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="667cf-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="667cf-118">Ha a *ContinuousCopy* értéket adja meg, ez a parancsmag a forrásadatbázis folyamatos másolatát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="667cf-118">If you specify *ContinuousCopy*, this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="667cf-119">Amikor a válasz érkezik, a művelet folyamatban lesz.</span><span class="sxs-lookup"><span data-stu-id="667cf-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="667cf-120">A műveletet a **Get-AzureSqlDatabaseCopy** vagy **a Get-AzureSqlDatabaseOperation segítségével figyelheti.**</span><span class="sxs-lookup"><span data-stu-id="667cf-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="667cf-121">Folyamatos másolatot online vagy offline adatbázisként is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="667cf-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="667cf-122">Az online folyamatos másolat az Azure SQLGeo-Replication-adatbázis aktív címtárának beállításához https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ használható.</span><span class="sxs-lookup"><span data-stu-id="667cf-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="667cf-123">Az offline folyamatos másolat az Azure SQLGeo-Replication-adatbázis standard Geo-Replication beállításához https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ használatos.</span><span class="sxs-lookup"><span data-stu-id="667cf-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="667cf-124">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="667cf-124">EXAMPLES</span></span>

### <span data-ttu-id="667cf-125">1. példa: Folyamatos adatbázis-másolat ütemezése</span><span class="sxs-lookup"><span data-stu-id="667cf-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="667cf-126">Ez a parancs az Orders (Rendelések) adatbázis folyamatos másolatát ütemezi az lpqd0zbr8y nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="667cf-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="667cf-127">A parancs létrehoz egy céladatbázist a bk0b8kf658 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="667cf-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="667cf-128">2. példa: Egyszeres példány létrehozása ugyanazon a kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="667cf-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="667cf-129">Ez a parancs létrehozza az Orders (Rendelések) adatbázis egy egyszeres másolatát az lpqd0zbr8y nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="667cf-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="667cf-130">A parancs létrehoz egy OrdersCopy nevű példányt ugyanazon a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="667cf-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="667cf-131">3. példa: Folyamatos offline adatbázis-példány ütemezése</span><span class="sxs-lookup"><span data-stu-id="667cf-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="667cf-132">Ez a parancs az Orders (Rendelések) adatbázis folyamatos másolatát ütemezi az lpqd0zbr8y nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="667cf-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="667cf-133">Ez a parancs létrehoz egy offline céladatbázist a bk0b8kf658 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="667cf-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="667cf-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="667cf-134">PARAMETERS</span></span>

### <span data-ttu-id="667cf-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="667cf-135">-ContinuousCopy</span></span>
<span data-ttu-id="667cf-136">Azt jelzi, hogy az adatbázis másolata folyamatos másolat lesz (egy replika-adatbázis).</span><span class="sxs-lookup"><span data-stu-id="667cf-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="667cf-137">A folyamatos másolás nem támogatott ugyanazon a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="667cf-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="667cf-138">Ha ez a paraméter nincs megadva, akkor a program egy egyszeres példányt hajt végre.</span><span class="sxs-lookup"><span data-stu-id="667cf-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="667cf-139">Az egyszeres példányban a forrás- és partneradatbázisnak ugyanazon a kiszolgálón kell lennie.</span><span class="sxs-lookup"><span data-stu-id="667cf-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

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

### <span data-ttu-id="667cf-140">-Database</span><span class="sxs-lookup"><span data-stu-id="667cf-140">-Database</span></span>
<span data-ttu-id="667cf-141">A forrás Azure SQL-adatbázist képviselő objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="667cf-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="667cf-142">Ez a paraméter elfogadja a folyamatbemenetet.</span><span class="sxs-lookup"><span data-stu-id="667cf-142">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="667cf-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="667cf-143">-DatabaseName</span></span>
<span data-ttu-id="667cf-144">A forrásadatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="667cf-144">Specifies the name of the source database.</span></span>

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

### <span data-ttu-id="667cf-145">-Force</span><span class="sxs-lookup"><span data-stu-id="667cf-145">-Force</span></span>
<span data-ttu-id="667cf-146">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="667cf-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="667cf-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="667cf-147">-OfflineSecondary</span></span>
<span data-ttu-id="667cf-148">Azt adja meg, hogy a folyamatos másolat aktív másolat helyett passzív másolat.</span><span class="sxs-lookup"><span data-stu-id="667cf-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="667cf-149">Ha a forrásadatbázis standard kiadású adatbázis, akkor ezt a paramétert kell megadni.</span><span class="sxs-lookup"><span data-stu-id="667cf-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="667cf-150">Ha ez a paraméter meg van adva, akkor *a ContinuousCopy* paramétert is meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="667cf-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

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

### <span data-ttu-id="667cf-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="667cf-151">-PartnerDatabase</span></span>
<span data-ttu-id="667cf-152">A céladatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="667cf-152">Specifies name of the target database.</span></span>
<span data-ttu-id="667cf-153">Ha a *ContinuousCopy* paramétert adja meg, a *PartnerDatabase* értékének meg kell egyeznie a forrásadatbázis nevével.</span><span class="sxs-lookup"><span data-stu-id="667cf-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="667cf-154">Ha nem a *ContinuousCopy* nevet adja meg, meg kell adnia a céladatbázis nevét, amely nem lehet más, mint a forrásadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="667cf-154">If you do not specify *ContinuousCopy*, you must specify a name for the target database, which can be different from the source database name.</span></span>

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

### <span data-ttu-id="667cf-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="667cf-155">-PartnerServer</span></span>
<span data-ttu-id="667cf-156">A céladatbázist tároló kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="667cf-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="667cf-157">Ennek a kiszolgálónak ugyanabban az Azure-előfizetésben kell lennie, mint a forrásadatbázis-kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="667cf-157">This server must be in the same Azure subscription as the source database server.</span></span>

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

### <span data-ttu-id="667cf-158">-Profil</span><span class="sxs-lookup"><span data-stu-id="667cf-158">-Profile</span></span>
<span data-ttu-id="667cf-159">Azt az Azure-profilt adja meg, amelyből a parancsmag olvas.</span><span class="sxs-lookup"><span data-stu-id="667cf-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="667cf-160">Ha nem ad meg profilt, ez a parancsmag a helyi alapértelmezett profilból olvassa be.</span><span class="sxs-lookup"><span data-stu-id="667cf-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="667cf-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="667cf-161">-ServerName</span></span>
<span data-ttu-id="667cf-162">Annak a kiszolgálónak a nevét adja meg, amelyen a forrásadatbázis található.</span><span class="sxs-lookup"><span data-stu-id="667cf-162">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="667cf-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="667cf-163">-Confirm</span></span>
<span data-ttu-id="667cf-164">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="667cf-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="667cf-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667cf-165">-WhatIf</span></span>
<span data-ttu-id="667cf-166">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="667cf-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="667cf-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="667cf-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="667cf-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667cf-168">CommonParameters</span></span>
<span data-ttu-id="667cf-169">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="667cf-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667cf-170">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="667cf-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667cf-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="667cf-171">INPUTS</span></span>

### <span data-ttu-id="667cf-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="667cf-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="667cf-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="667cf-173">OUTPUTS</span></span>

### <span data-ttu-id="667cf-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="667cf-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="667cf-175">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="667cf-175">NOTES</span></span>
* <span data-ttu-id="667cf-176">Hitelesítés: Ez a parancsmag tanúsítványalapú hitelesítést igényel.</span><span class="sxs-lookup"><span data-stu-id="667cf-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="667cf-177">Ha például tanúsítványalapú hitelesítéssel állíthatja be az aktuális előfizetést, tekintse meg a New-AzureSqlDatabaseServerContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="667cf-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="667cf-178">Figyelés: A kiszolgálón aktív egy vagy több folyamatos másolási kapcsolat állapotának ellenőrzéséhez használja a **Get-AzureSqlDatabaseCopy** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="667cf-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="667cf-179">Ha a folyamatos másolási kapcsolat forrásán és célértékénél is ellenőriznie kell a műveletek állapotát, használja a **Get-AzureSqlDatabaseOperation** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="667cf-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="667cf-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="667cf-180">RELATED LINKS</span></span>

[<span data-ttu-id="667cf-181">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="667cf-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="667cf-182">Műveletek az Azure SQL-adatbázisokban</span><span class="sxs-lookup"><span data-stu-id="667cf-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="667cf-183">Adatbázis-másolás létrehozása</span><span class="sxs-lookup"><span data-stu-id="667cf-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[<span data-ttu-id="667cf-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="667cf-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="667cf-185">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="667cf-185">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


