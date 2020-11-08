---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015865"
---
# <span data-ttu-id="3d372-101">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d372-101">Set-AzureSqlDatabase</span></span>

## <span data-ttu-id="3d372-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d372-102">SYNOPSIS</span></span>
<span data-ttu-id="3d372-103">Az Azure SQL-adatbázisok tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="3d372-103">Sets properties for an Azure SQL Database.</span></span>

## <span data-ttu-id="3d372-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d372-104">SYNTAX</span></span>

### <span data-ttu-id="3d372-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="3d372-105">ByNameWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d372-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="3d372-106">ByObjectWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d372-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="3d372-107">ByNameWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d372-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="3d372-108">ByObjectWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d372-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d372-109">DESCRIPTION</span></span>
<span data-ttu-id="3d372-110">A **set-AzureSqlDatabase** parancsmag az Azure SQL-adatbázisok tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="3d372-110">The **Set-AzureSqlDatabase** cmdlet sets properties for an Azure SQL Database.</span></span>
<span data-ttu-id="3d372-111">Megadhatja az adatbázist név szerint, vagy átadhat egy Azure SQL adatbázis-objektumot a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="3d372-111">You can specify the database by name, or pass an Azure SQL Database object through the pipeline.</span></span>
<span data-ttu-id="3d372-112">Megadhatja a kiszolgálót név szerint, vagy átadhatja az Azure SQL-adatbázis kiszolgálójának kapcsolati környezetét.</span><span class="sxs-lookup"><span data-stu-id="3d372-112">You can specify the server by name, or pass an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="3d372-113">A **New-AzureSqlDatabaseServerContext** parancsmag futtatásával kapcsolati környezetet hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="3d372-113">Create a connection context by running the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="3d372-114">Ha a kiszolgálót név szerint adja meg, a parancsmag az aktuális Azure-előfizetés adatait használja a kérés hitelesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="3d372-114">If you specify the server by name, the cmdlet uses the current Azure subscription information to authenticate the request.</span></span>

## <span data-ttu-id="3d372-115">Példák</span><span class="sxs-lookup"><span data-stu-id="3d372-115">EXAMPLES</span></span>

### <span data-ttu-id="3d372-116">Példa 1: adatbázis méretének módosítása kapcsolati környezet használatával</span><span class="sxs-lookup"><span data-stu-id="3d372-116">Example 1: Change the size of a database by using a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="3d372-117">Ebben a példában a Database01 nevű adatbázis méretét módosítja az Azure SQL Database Server kapcsolati környezetének $Context.</span><span class="sxs-lookup"><span data-stu-id="3d372-117">This example changes the size of the database named Database01 to 20 GB, in the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="3d372-118">2. példa: az adatbázis méretének módosítása kiszolgálónév használatával</span><span class="sxs-lookup"><span data-stu-id="3d372-118">Example 2: Change the size of a database by using a server name</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="3d372-119">Ebben a példában a lpqd0zbr8y nevű kiszolgálón a Database01 nevű adatbázis méretének 20 GB-ra változik.</span><span class="sxs-lookup"><span data-stu-id="3d372-119">This example changes the size of the database named Database01 to 20 GB in the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="3d372-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d372-120">PARAMETERS</span></span>

### <span data-ttu-id="3d372-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="3d372-121">-ConnectionContext</span></span>
<span data-ttu-id="3d372-122">A kiszolgáló kapcsolati környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d372-122">Specifies the connection context of a server.</span></span>

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

### <span data-ttu-id="3d372-123">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="3d372-123">-Database</span></span>
<span data-ttu-id="3d372-124">Egy olyan objektumot ad meg, amely a parancsmag által módosított Azure SQL-adatbázist jelöli.</span><span class="sxs-lookup"><span data-stu-id="3d372-124">Specifies an object that represents the Azure SQL Database that this cmdlet modifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d372-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d372-125">-DatabaseName</span></span>
<span data-ttu-id="3d372-126">Annak az adatbázisnak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="3d372-126">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3d372-127">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="3d372-127">-Edition</span></span>
<span data-ttu-id="3d372-128">Az Azure SQL-adatbázis új kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d372-128">Specifies the new edition for the Azure SQL Database.</span></span>
<span data-ttu-id="3d372-129">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="3d372-129">Valid values are:</span></span> 

- <span data-ttu-id="3d372-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="3d372-130">None</span></span>
- <span data-ttu-id="3d372-131">Web</span><span class="sxs-lookup"><span data-stu-id="3d372-131">Web</span></span>
- <span data-ttu-id="3d372-132">Vállalati verzió</span><span class="sxs-lookup"><span data-stu-id="3d372-132">Business</span></span>
- <span data-ttu-id="3d372-133">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="3d372-133">Basic</span></span>
- <span data-ttu-id="3d372-134">Standard</span><span class="sxs-lookup"><span data-stu-id="3d372-134">Standard</span></span>
-  <span data-ttu-id="3d372-135">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="3d372-135">Premium</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d372-136">-Force</span><span class="sxs-lookup"><span data-stu-id="3d372-136">-Force</span></span>
<span data-ttu-id="3d372-137">Lehetővé teszi a művelet befejezését a megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="3d372-137">Allows the action to complete without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3d372-138">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="3d372-138">-MaxSizeBytes</span></span>
<span data-ttu-id="3d372-139">Az adatbázis új maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="3d372-139">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="3d372-140">Ezt a paramétert vagy a *MaxSizeGB* paramétert is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="3d372-140">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="3d372-141">A *MaxSizeGB* paramétert az elfogadható értékekről a kiadás alapján című témakörben tekintheti meg.</span><span class="sxs-lookup"><span data-stu-id="3d372-141">See the *MaxSizeGB* parameter for acceptable values based on edition.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d372-142">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="3d372-142">-MaxSizeGB</span></span>
<span data-ttu-id="3d372-143">Az adatbázis új maximális méretét adja meg gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="3d372-143">Specifies the new maximum size for the database in gigabytes.</span></span>
<span data-ttu-id="3d372-144">Ezt a paramétert vagy a *MaxSizeBytes* paramétert is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="3d372-144">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="3d372-145">Az elfogadható értékek kiadás alapján eltérőek.</span><span class="sxs-lookup"><span data-stu-id="3d372-145">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="3d372-146">Alapvető kiadási értékek: 1 vagy 2</span><span class="sxs-lookup"><span data-stu-id="3d372-146">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="3d372-147">Szokásos kiadási értékek: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 vagy 250</span><span class="sxs-lookup"><span data-stu-id="3d372-147">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="3d372-148">Prémium kiadású értékek: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 vagy 500</span><span class="sxs-lookup"><span data-stu-id="3d372-148">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="3d372-149">Web Edition-értékek: 1 vagy 5</span><span class="sxs-lookup"><span data-stu-id="3d372-149">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="3d372-150">Üzleti kiadás értékei: 10, 20, 30, 40, 50, 100 vagy 150</span><span class="sxs-lookup"><span data-stu-id="3d372-150">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d372-151">-NewDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d372-151">-NewDatabaseName</span></span>
<span data-ttu-id="3d372-152">Az adatbázis új nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d372-152">Specifies the new name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d372-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d372-153">-PassThru</span></span>
<span data-ttu-id="3d372-154">A frissített Azure SQL-adatbázis értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3d372-154">Returns the updated Azure SQL Database.</span></span>

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

### <span data-ttu-id="3d372-155">-Profil</span><span class="sxs-lookup"><span data-stu-id="3d372-155">-Profile</span></span>
<span data-ttu-id="3d372-156">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3d372-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d372-157">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3d372-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d372-158">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3d372-158">-ServerName</span></span>
<span data-ttu-id="3d372-159">Annak a kiszolgálónak a neve, amely a parancsmag által módosított adatbázist tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3d372-159">Specifies the name of the server that contains the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3d372-160">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="3d372-160">-ServiceObjective</span></span>
<span data-ttu-id="3d372-161">Egy olyan objektumot ad meg, amely az adatbázis új szolgáltatás célját (teljesítményi szintjét) jelképezi.</span><span class="sxs-lookup"><span data-stu-id="3d372-161">Specifies an object representing the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="3d372-162">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="3d372-162">Valid values are:</span></span> 

- <span data-ttu-id="3d372-163">Alap: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="3d372-163">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="3d372-164">Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="3d372-164">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="3d372-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="3d372-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="3d372-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="3d372-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="3d372-167">\* Standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="3d372-167">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="3d372-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="3d372-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="3d372-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="3d372-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="3d372-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="3d372-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="3d372-171">\* Standard (S3) a legújabb SQL-adatbázis-frissítés V12 (előzetes verzió) része.</span><span class="sxs-lookup"><span data-stu-id="3d372-171">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="3d372-172">További információ: az Azure SQL Database V12 előzetes verzió újdonságai https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="3d372-172">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d372-173">– Szinkronizálás</span><span class="sxs-lookup"><span data-stu-id="3d372-173">-Sync</span></span>
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

### <span data-ttu-id="3d372-174">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d372-174">-Confirm</span></span>
<span data-ttu-id="3d372-175">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d372-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d372-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d372-176">-WhatIf</span></span>
<span data-ttu-id="3d372-177">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d372-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d372-178">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d372-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d372-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d372-179">CommonParameters</span></span>
<span data-ttu-id="3d372-180">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d372-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d372-181">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d372-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d372-182">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d372-182">INPUTS</span></span>

### <span data-ttu-id="3d372-183">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="3d372-183">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="3d372-184">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d372-184">OUTPUTS</span></span>

### <span data-ttu-id="3d372-185">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="3d372-185">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="3d372-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d372-186">NOTES</span></span>

## <span data-ttu-id="3d372-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d372-187">RELATED LINKS</span></span>

[<span data-ttu-id="3d372-188">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="3d372-188">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="3d372-189">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="3d372-189">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="3d372-190">Adatbázis frissítése</span><span class="sxs-lookup"><span data-stu-id="3d372-190">Update Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[<span data-ttu-id="3d372-191">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d372-191">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="3d372-192">Új – AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d372-192">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="3d372-193">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d372-193">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="3d372-194">Új – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="3d372-194">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


