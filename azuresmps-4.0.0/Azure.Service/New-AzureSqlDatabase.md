---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015973"
---
# <span data-ttu-id="ff34b-101">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff34b-101">New-AzureSqlDatabase</span></span>

## <span data-ttu-id="ff34b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff34b-102">SYNOPSIS</span></span>
<span data-ttu-id="ff34b-103">Azure SQL-adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ff34b-103">Creates an Azure SQL Database.</span></span>

## <span data-ttu-id="ff34b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff34b-104">SYNTAX</span></span>

### <span data-ttu-id="ff34b-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="ff34b-105">ByConnectionContext</span></span>
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff34b-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="ff34b-106">ByServerName</span></span>
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff34b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff34b-107">DESCRIPTION</span></span>
<span data-ttu-id="ff34b-108">A **New-AzureSqlDatabase** PARANCSMAG Azure SQL-adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ff34b-108">The **New-AzureSqlDatabase** cmdlet creates an Azure SQL Database.</span></span>
<span data-ttu-id="ff34b-109">A kiszolgálót a **New-AzureSqlDatabaseServerContext** parancsmaggal létrehozott Azure SQL adatbázis-kiszolgáló kapcsolati környezete segítségével adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="ff34b-109">You can specify the server by using an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="ff34b-110">Ha a kiszolgáló nevét adja meg, a parancsmag az aktuális Azure-előfizetési adatokkal hitelesíti a kiszolgáló elérésére vonatkozó kérést.</span><span class="sxs-lookup"><span data-stu-id="ff34b-110">Or, if you specify the server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="ff34b-111">Amikor új adatbázist hoz létre az Azure SQL-adatbázis kiszolgálójának megadásával, a **New-AzureSqlDatabase** parancsmag ideiglenes kapcsolati környezetet hoz létre a megadott kiszolgálónév és az Azure aktuális előfizetési adatai alapján a művelet végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="ff34b-111">When you create a new database by specifying an Azure SQL Database server, the **New-AzureSqlDatabase** cmdlet creates a temporary connection context using the specified server name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="ff34b-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ff34b-112">EXAMPLES</span></span>

### <span data-ttu-id="ff34b-113">Példa 1: adatbázis létrehozása</span><span class="sxs-lookup"><span data-stu-id="ff34b-113">Example 1: Create a database</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="ff34b-114">Ez a parancs létrehoz egy Adatbázis1 nevű Azure SQL-adatbázist az Azure SQL-adatbázis kiszolgálójának kapcsolati környezetéhez $Context.</span><span class="sxs-lookup"><span data-stu-id="ff34b-114">This command creates an Azure SQL Database named Database1, for the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="ff34b-115">2. példa: adatbázis létrehozása az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="ff34b-115">Example 2: Create a database in the current subscription</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="ff34b-116">Ez a példa létrehoz egy Adatbázis1 nevű adatbázist a lpqd0zbr8y nevű Azure SQL adatbázis-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="ff34b-116">This example creates a database named Database1, in the specified Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="ff34b-117">A parancsmag az aktuális Azure-előfizetési adatok alapján hitelesíti a kiszolgáló elérésére vonatkozó kérést.</span><span class="sxs-lookup"><span data-stu-id="ff34b-117">The cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

## <span data-ttu-id="ff34b-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff34b-118">PARAMETERS</span></span>

### <span data-ttu-id="ff34b-119">-Szétválogatás</span><span class="sxs-lookup"><span data-stu-id="ff34b-119">-Collation</span></span>
<span data-ttu-id="ff34b-120">Az új adatbázis egybevetését adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff34b-120">Specifies a collation for the new database.</span></span>

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

### <span data-ttu-id="ff34b-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="ff34b-121">-ConnectionContext</span></span>
<span data-ttu-id="ff34b-122">Annak a kiszolgálónak a kapcsolati környezetét adja meg, ahol ez a parancsmag létrehoz egy adatbázist.</span><span class="sxs-lookup"><span data-stu-id="ff34b-122">Specifies the connection context of a server where this cmdlet creates a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff34b-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ff34b-123">-DatabaseName</span></span>
<span data-ttu-id="ff34b-124">Az új adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff34b-124">Specifies the name of the new database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff34b-125">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="ff34b-125">-Edition</span></span>
<span data-ttu-id="ff34b-126">Az új Azure SQL-adatbázis kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff34b-126">Specifies the edition for the new Azure SQL Database.</span></span>
<span data-ttu-id="ff34b-127">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="ff34b-127">Valid values are:</span></span> 

- <span data-ttu-id="ff34b-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="ff34b-128">None</span></span>
- <span data-ttu-id="ff34b-129">Web</span><span class="sxs-lookup"><span data-stu-id="ff34b-129">Web</span></span>
- <span data-ttu-id="ff34b-130">Vállalati verzió</span><span class="sxs-lookup"><span data-stu-id="ff34b-130">Business</span></span>
- <span data-ttu-id="ff34b-131">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="ff34b-131">Basic</span></span>
- <span data-ttu-id="ff34b-132">Standard</span><span class="sxs-lookup"><span data-stu-id="ff34b-132">Standard</span></span>
-  <span data-ttu-id="ff34b-133">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="ff34b-133">Premium</span></span>

<span data-ttu-id="ff34b-134">Az alapértelmezett érték a web.</span><span class="sxs-lookup"><span data-stu-id="ff34b-134">The default value is Web.</span></span>

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

### <span data-ttu-id="ff34b-135">-Force</span><span class="sxs-lookup"><span data-stu-id="ff34b-135">-Force</span></span>
<span data-ttu-id="ff34b-136">Lehetővé teszi, hogy a művelet a felhasználó megerősítésének megkérdezése nélkül legyen elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="ff34b-136">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="ff34b-137">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="ff34b-137">-MaxSizeBytes</span></span>
<span data-ttu-id="ff34b-138">Az adatbázis maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="ff34b-138">Specifies the maximum size of the database in bytes.</span></span>
<span data-ttu-id="ff34b-139">Ezt a paramétert vagy a *MaxSizeGB* paramétert is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="ff34b-139">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="ff34b-140">A *MaxSizeGB* paraméter leírása az elfogadható értékekről a kiadás alapján című témakörben olvasható.</span><span class="sxs-lookup"><span data-stu-id="ff34b-140">See the *MaxSizeGB* parameter description for acceptable values based on edition.</span></span>

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

### <span data-ttu-id="ff34b-141">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="ff34b-141">-MaxSizeGB</span></span>
<span data-ttu-id="ff34b-142">Az adatbázis maximális méretét adja meg gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="ff34b-142">Specifies the maximum size of the database in gigabytes.</span></span>
<span data-ttu-id="ff34b-143">Ezt a paramétert vagy a *MaxSizeBytes* paramétert is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="ff34b-143">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="ff34b-144">Az elfogadható értékek kiadás alapján eltérőek.</span><span class="sxs-lookup"><span data-stu-id="ff34b-144">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="ff34b-145">Alapvető kiadási értékek: 1 vagy 2</span><span class="sxs-lookup"><span data-stu-id="ff34b-145">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="ff34b-146">Szokásos kiadási értékek: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 vagy 250</span><span class="sxs-lookup"><span data-stu-id="ff34b-146">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="ff34b-147">Prémium kiadású értékek: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 vagy 500</span><span class="sxs-lookup"><span data-stu-id="ff34b-147">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="ff34b-148">Web Edition-értékek: 1 vagy 5</span><span class="sxs-lookup"><span data-stu-id="ff34b-148">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="ff34b-149">Üzleti kiadás értékei: 10, 20, 30, 40, 50, 100 vagy 150</span><span class="sxs-lookup"><span data-stu-id="ff34b-149">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

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

### <span data-ttu-id="ff34b-150">-Profil</span><span class="sxs-lookup"><span data-stu-id="ff34b-150">-Profile</span></span>
<span data-ttu-id="ff34b-151">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ff34b-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff34b-152">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ff34b-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff34b-153">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ff34b-153">-ServerName</span></span>
<span data-ttu-id="ff34b-154">Annak az Azure SQL adatbázis-kiszolgálónak a nevét adja meg, amely az új adatbázist tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ff34b-154">Specifies the name of the Azure SQL Database server to contain the new database.</span></span>

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

### <span data-ttu-id="ff34b-155">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="ff34b-155">-ServiceObjective</span></span>
<span data-ttu-id="ff34b-156">Egy olyan objektumot ad meg, amely az új szolgáltatás célját (teljesítményszint) képviseli az adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="ff34b-156">Specifies an object that represent the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="ff34b-157">Ez az érték az adatbázishoz rendelt erőforrások szintjét jelöli.</span><span class="sxs-lookup"><span data-stu-id="ff34b-157">This value represents the level of resources assigned to this database.</span></span>
<span data-ttu-id="ff34b-158">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="ff34b-158">Valid values are:</span></span> 

<span data-ttu-id="ff34b-159">Alap: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \* standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="ff34b-159">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="ff34b-160">\* Standard (S3) a legújabb SQL-adatbázis-frissítés V12 (előzetes verzió) része.</span><span class="sxs-lookup"><span data-stu-id="ff34b-160">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="ff34b-161">További információ: az Azure SQL Database V12 előzetes verzió újdonságai https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="ff34b-161">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

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

### <span data-ttu-id="ff34b-162">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff34b-162">-Confirm</span></span>
<span data-ttu-id="ff34b-163">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff34b-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff34b-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff34b-164">-WhatIf</span></span>
<span data-ttu-id="ff34b-165">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff34b-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff34b-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff34b-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff34b-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff34b-167">CommonParameters</span></span>
<span data-ttu-id="ff34b-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff34b-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff34b-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff34b-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff34b-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff34b-170">INPUTS</span></span>

## <span data-ttu-id="ff34b-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff34b-171">OUTPUTS</span></span>

### <span data-ttu-id="ff34b-172">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="ff34b-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="ff34b-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff34b-173">NOTES</span></span>
* <span data-ttu-id="ff34b-174">Ha törölni szeretne egy **új AzureSqlDatabase** létrehozott adatbázist, használja az Remove-AzureSqlDatabase parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ff34b-174">To delete a database that was created by **New-AzureSqlDatabase** , use the Remove-AzureSqlDatabase cmdlet.</span></span>

## <span data-ttu-id="ff34b-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff34b-175">RELATED LINKS</span></span>

[<span data-ttu-id="ff34b-176">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="ff34b-176">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="ff34b-177">Adatbázis létrehozása</span><span class="sxs-lookup"><span data-stu-id="ff34b-177">Create Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[<span data-ttu-id="ff34b-178">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="ff34b-178">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="ff34b-179">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff34b-179">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="ff34b-180">Új – AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="ff34b-180">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="ff34b-181">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff34b-181">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="ff34b-182">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff34b-182">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


