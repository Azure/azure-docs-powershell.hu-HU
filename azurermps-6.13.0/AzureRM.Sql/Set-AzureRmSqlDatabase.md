---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 283b12ca63f92086369f273b1f04d5e3f0cd1716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493612"
---
# <span data-ttu-id="3ce4b-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3ce4b-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="3ce4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ce4b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce4b-103">Beállítja az adatbázis tulajdonságait, vagy áthelyezi egy meglévő adatbázist egy rugalmas készletbe.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ce4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ce4b-104">SYNTAX</span></span>

### <span data-ttu-id="3ce4b-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ce4b-105">Update (Default)</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ce4b-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="3ce4b-106">VcoreBasedDatabase</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce4b-107">Átnevezése</span><span class="sxs-lookup"><span data-stu-id="3ce4b-107">Rename</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ce4b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ce4b-108">DESCRIPTION</span></span>
<span data-ttu-id="3ce4b-109">A **set-AzureRmSqlDatabase** parancsmag az Azure SQL-adatbázisban tárolt adatbázis tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-109">The **Set-AzureRmSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="3ce4b-110">Ez a parancsmag módosíthatja a Service Tier ( *kiadás* ), a teljesítményszint ( *RequestedServiceObjectiveName* ) és az adatbázis tárterületének maximális méretét ( *MaxSizeBytes* ).</span><span class="sxs-lookup"><span data-stu-id="3ce4b-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="3ce4b-111">Emellett megadhatja, hogy az *ElasticPoolName* paraméter az adatbázis rugalmas készletéből való áthelyezését is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="3ce4b-112">Ha egy adatbázis már egy rugalmas készletben van, akkor a *RequestedServiceObjectiveName* paraméterrel az adatbázist rugalmas készletből és egyetlen adatbázis teljesítmény szintjére helyezheti.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="3ce4b-113">Példák</span><span class="sxs-lookup"><span data-stu-id="3ce4b-113">EXAMPLES</span></span>

### <span data-ttu-id="3ce4b-114">1. példa: adatbázis frissítése szabványos S2-adatbázisra</span><span class="sxs-lookup"><span data-stu-id="3ce4b-114">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="3ce4b-115">Ez a parancs frissíti a Database01 nevű adatbázist egy szabványos S2-adatbázishoz a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-115">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="3ce4b-116">2. példa: adatbázis felvétele elasztikus poolba</span><span class="sxs-lookup"><span data-stu-id="3ce4b-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="3ce4b-117">A parancs hozzáadja a Database01 nevű adatbázist a Server01 nevű ElasticPool01 nevű rugalmas készlethez.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="3ce4b-118">3. példa: az adatbázis tárterületének maximális méretének módosítása</span><span class="sxs-lookup"><span data-stu-id="3ce4b-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="3ce4b-119">Ez a parancs frissíti a Database01 nevű adatbázist a maximális méret 1 TB értékre állításával.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="3ce4b-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ce4b-120">PARAMETERS</span></span>

### <span data-ttu-id="3ce4b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ce4b-121">-AsJob</span></span>
<span data-ttu-id="3ce4b-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3ce4b-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3ce4b-123">-ComputeGeneration</span></span>
<span data-ttu-id="3ce4b-124">A hozzárendelni kívánt számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-124">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3ce4b-125">-DatabaseName</span></span>
<span data-ttu-id="3ce4b-126">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-126">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce4b-127">-DefaultProfile</span></span>
<span data-ttu-id="3ce4b-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3ce4b-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-129">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="3ce4b-129">-Edition</span></span>
<span data-ttu-id="3ce4b-130">Az adatbázis kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-130">Specifies the edition for the database.</span></span>
<span data-ttu-id="3ce4b-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3ce4b-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ce4b-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="3ce4b-132">None</span></span>
- <span data-ttu-id="3ce4b-133">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="3ce4b-133">Basic</span></span>
- <span data-ttu-id="3ce4b-134">Standard</span><span class="sxs-lookup"><span data-stu-id="3ce4b-134">Standard</span></span>
- <span data-ttu-id="3ce4b-135">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="3ce4b-135">Premium</span></span>
- <span data-ttu-id="3ce4b-136">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="3ce4b-136">DataWarehouse</span></span>
- <span data-ttu-id="3ce4b-137">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="3ce4b-137">Free</span></span>
- <span data-ttu-id="3ce4b-138">Nyúlik</span><span class="sxs-lookup"><span data-stu-id="3ce4b-138">Stretch</span></span>
- <span data-ttu-id="3ce4b-139">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="3ce4b-139">GeneralPurpose</span></span>
- <span data-ttu-id="3ce4b-140">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="3ce4b-140">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-141">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3ce4b-141">-ElasticPoolName</span></span>
<span data-ttu-id="3ce4b-142">Annak a rugalmas készletnek a nevét adja meg, amelybe az adatbázist át szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-142">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3ce4b-143">-LicenseType</span></span>
<span data-ttu-id="3ce4b-144">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-144">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-145">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="3ce4b-145">-MaxSizeBytes</span></span>
<span data-ttu-id="3ce4b-146">Az Azure SQL-adatbázis maximális mérete bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="3ce4b-146">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-147">-NewName</span><span class="sxs-lookup"><span data-stu-id="3ce4b-147">-NewName</span></span>
<span data-ttu-id="3ce4b-148">Az új név az adatbázis átnevezéséhez.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-148">The new name to rename the database to.</span></span>

```yaml
Type: System.String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-149">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="3ce4b-149">-ReadScale</span></span>
<span data-ttu-id="3ce4b-150">Az Azure SQL-adatbázishoz rendelt olvasási méretarány beállítás. (Engedélyezve/letiltva)</span><span class="sxs-lookup"><span data-stu-id="3ce4b-150">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: Update, VcoreBasedDatabase
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-151">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="3ce4b-151">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="3ce4b-152">Az adatbázishoz hozzárendelni kívánt szolgáltatási cél nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-152">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="3ce4b-153">A szolgáltatási célkitűzésekről további információt az [Azure SQL Database Service Tiers és a teljesítmény szintje](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) a Microsoft Developer Network műsortárában című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-153">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce4b-154">-ResourceGroupName</span></span>
<span data-ttu-id="3ce4b-155">Annak a csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-155">Specifies the name of resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-156">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3ce4b-156">-ServerName</span></span>
<span data-ttu-id="3ce4b-157">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-157">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-158">-Címkék</span><span class="sxs-lookup"><span data-stu-id="3ce4b-158">-Tags</span></span>
<span data-ttu-id="3ce4b-159">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3ce4b-160">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3ce4b-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update, VcoreBasedDatabase
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="3ce4b-161">-VCore</span></span>
<span data-ttu-id="3ce4b-162">Az Azure SQL-adatbázis vcore száma</span><span class="sxs-lookup"><span data-stu-id="3ce4b-162">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="3ce4b-163">-ZoneRedundant</span></span>
<span data-ttu-id="3ce4b-164">A zóna redundancia az Azure SQL-adatbázishoz való társításhoz</span><span class="sxs-lookup"><span data-stu-id="3ce4b-164">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ce4b-165">-Confirm</span></span>
<span data-ttu-id="3ce4b-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ce4b-167">-WhatIf</span></span>
<span data-ttu-id="3ce4b-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ce4b-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ce4b-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce4b-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce4b-170">CommonParameters</span></span>
<span data-ttu-id="3ce4b-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ce4b-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce4b-172">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce4b-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce4b-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ce4b-173">INPUTS</span></span>

### <span data-ttu-id="3ce4b-174">System. String</span><span class="sxs-lookup"><span data-stu-id="3ce4b-174">System.String</span></span>

## <span data-ttu-id="3ce4b-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ce4b-175">OUTPUTS</span></span>

### <span data-ttu-id="3ce4b-176">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3ce4b-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="3ce4b-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ce4b-177">NOTES</span></span>

## <span data-ttu-id="3ce4b-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ce4b-178">RELATED LINKS</span></span>

[<span data-ttu-id="3ce4b-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3ce4b-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="3ce4b-180">Új – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3ce4b-180">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="3ce4b-181">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3ce4b-181">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="3ce4b-182">Önéletrajz – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3ce4b-182">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="3ce4b-183">Felfüggesztés – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3ce4b-183">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="3ce4b-184">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3ce4b-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
