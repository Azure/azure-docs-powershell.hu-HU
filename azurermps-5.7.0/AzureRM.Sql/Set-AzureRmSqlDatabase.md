---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: b0493433f7419039acacd696748b3c5f9518aef5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494291"
---
# <span data-ttu-id="a33c1-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a33c1-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="a33c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a33c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a33c1-103">Beállítja az adatbázis tulajdonságait, vagy áthelyezi egy meglévő adatbázist egy rugalmas készletbe.</span><span class="sxs-lookup"><span data-stu-id="a33c1-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a33c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a33c1-104">SYNTAX</span></span>

### <span data-ttu-id="a33c1-105">Frissítés</span><span class="sxs-lookup"><span data-stu-id="a33c1-105">Update</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a33c1-106">Átnevezése</span><span class="sxs-lookup"><span data-stu-id="a33c1-106">Rename</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a33c1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a33c1-107">DESCRIPTION</span></span>
<span data-ttu-id="a33c1-108">A **set-AzureRmSqlDatabase** parancsmag az Azure SQL-adatbázisban tárolt adatbázis tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="a33c1-108">The **Set-AzureRmSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="a33c1-109">Ez a parancsmag módosíthatja a Service Tier ( *kiadás* ), a teljesítményszint ( *RequestedServiceObjectiveName* ) és az adatbázis tárterületének maximális méretét ( *MaxSizeBytes* ).</span><span class="sxs-lookup"><span data-stu-id="a33c1-109">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="a33c1-110">Emellett megadhatja, hogy az *ElasticPoolName* paraméter az adatbázis rugalmas készletéből való áthelyezését is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="a33c1-110">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="a33c1-111">Ha egy adatbázis már egy rugalmas készletben van, akkor a *RequestedServiceObjectiveName* paraméterrel az adatbázist rugalmas készletből és egyetlen adatbázis teljesítmény szintjére helyezheti.</span><span class="sxs-lookup"><span data-stu-id="a33c1-111">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="a33c1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a33c1-112">EXAMPLES</span></span>

### <span data-ttu-id="a33c1-113">1. példa: adatbázis frissítése szabványos S2-adatbázisra</span><span class="sxs-lookup"><span data-stu-id="a33c1-113">Example 1: Update a database to a Standard S2 database</span></span>
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

<span data-ttu-id="a33c1-114">Ez a parancs frissíti a Database01 nevű adatbázist egy szabványos S2-adatbázishoz a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="a33c1-114">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="a33c1-115">2. példa: adatbázis felvétele elasztikus poolba</span><span class="sxs-lookup"><span data-stu-id="a33c1-115">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="a33c1-116">A parancs hozzáadja a Database01 nevű adatbázist a Server01 nevű ElasticPool01 nevű rugalmas készlethez.</span><span class="sxs-lookup"><span data-stu-id="a33c1-116">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="a33c1-117">3. példa: az adatbázis tárterületének maximális méretének módosítása</span><span class="sxs-lookup"><span data-stu-id="a33c1-117">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="a33c1-118">Ez a parancs frissíti a Database01 nevű adatbázist a maximális méret 1 TB értékre állításával.</span><span class="sxs-lookup"><span data-stu-id="a33c1-118">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="a33c1-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a33c1-119">PARAMETERS</span></span>

### <span data-ttu-id="a33c1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a33c1-120">-AsJob</span></span>
<span data-ttu-id="a33c1-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a33c1-121">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="a33c1-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a33c1-122">-DatabaseName</span></span>
<span data-ttu-id="a33c1-123">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a33c1-123">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33c1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33c1-124">-DefaultProfile</span></span>
<span data-ttu-id="a33c1-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a33c1-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33c1-126">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="a33c1-126">-Edition</span></span>
<span data-ttu-id="a33c1-127">Az adatbázis kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a33c1-127">Specifies the edition for the database.</span></span>
<span data-ttu-id="a33c1-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a33c1-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a33c1-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="a33c1-129">None</span></span>
- <span data-ttu-id="a33c1-130">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="a33c1-130">Premium</span></span>
- <span data-ttu-id="a33c1-131">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="a33c1-131">Basic</span></span>
- <span data-ttu-id="a33c1-132">Standard</span><span class="sxs-lookup"><span data-stu-id="a33c1-132">Standard</span></span>
- <span data-ttu-id="a33c1-133">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="a33c1-133">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: Update
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33c1-134">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a33c1-134">-ElasticPoolName</span></span>
<span data-ttu-id="a33c1-135">Annak a rugalmas készletnek a nevét adja meg, amelybe az adatbázist át szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="a33c1-135">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33c1-136">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="a33c1-136">-MaxSizeBytes</span></span>
<span data-ttu-id="a33c1-137">Az Azure SQL-adatbázis maximális mérete bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="a33c1-137">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33c1-138">-NewName</span><span class="sxs-lookup"><span data-stu-id="a33c1-138">-NewName</span></span>
<span data-ttu-id="a33c1-139">Az új név az adatbázis átnevezéséhez.</span><span class="sxs-lookup"><span data-stu-id="a33c1-139">The new name to rename the database to.</span></span>

```yaml
Type: String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33c1-140">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="a33c1-140">-ReadScale</span></span>
<span data-ttu-id="a33c1-141">Az Azure SQL-adatbázishoz rendelt olvasási méretarány beállítás. (Engedélyezve/letiltva)</span><span class="sxs-lookup"><span data-stu-id="a33c1-141">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: Update
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33c1-142">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="a33c1-142">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="a33c1-143">Az adatbázishoz hozzárendelni kívánt szolgáltatási cél nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a33c1-143">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="a33c1-144">A szolgáltatási célkitűzésekről további információt az [Azure SQL Database Service Tiers és a teljesítmény szintje](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) a Microsoft Developer Network műsortárában című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="a33c1-144">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33c1-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a33c1-145">-ResourceGroupName</span></span>
<span data-ttu-id="a33c1-146">Annak a csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="a33c1-146">Specifies the name of resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33c1-147">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a33c1-147">-ServerName</span></span>
<span data-ttu-id="a33c1-148">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a33c1-148">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33c1-149">-Címkék</span><span class="sxs-lookup"><span data-stu-id="a33c1-149">-Tags</span></span>
<span data-ttu-id="a33c1-150">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="a33c1-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a33c1-151">Példa:</span><span class="sxs-lookup"><span data-stu-id="a33c1-151">For example:</span></span>

<span data-ttu-id="a33c1-152">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="a33c1-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Update
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33c1-153">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="a33c1-153">-ZoneRedundant</span></span>
<span data-ttu-id="a33c1-154">A zóna redundancia az Azure SQL-adatbázishoz való társításhoz</span><span class="sxs-lookup"><span data-stu-id="a33c1-154">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33c1-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a33c1-155">-Confirm</span></span>
<span data-ttu-id="a33c1-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a33c1-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a33c1-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a33c1-157">-WhatIf</span></span>
<span data-ttu-id="a33c1-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a33c1-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a33c1-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a33c1-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a33c1-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33c1-160">CommonParameters</span></span>
<span data-ttu-id="a33c1-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a33c1-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33c1-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a33c1-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33c1-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a33c1-163">INPUTS</span></span>

### <span data-ttu-id="a33c1-164">Nincs</span><span class="sxs-lookup"><span data-stu-id="a33c1-164">None</span></span>
<span data-ttu-id="a33c1-165">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a33c1-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a33c1-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a33c1-166">OUTPUTS</span></span>

### <span data-ttu-id="a33c1-167">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a33c1-167">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a33c1-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a33c1-168">NOTES</span></span>

## <span data-ttu-id="a33c1-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a33c1-169">RELATED LINKS</span></span>

[<span data-ttu-id="a33c1-170">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a33c1-170">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="a33c1-171">Új – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a33c1-171">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="a33c1-172">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a33c1-172">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="a33c1-173">Önéletrajz – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a33c1-173">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="a33c1-174">Felfüggesztés – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a33c1-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="a33c1-175">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a33c1-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
