---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: f5fc78f3e06150f3283e35c23bf80edce4f47650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500368"
---
# <span data-ttu-id="55f42-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55f42-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="55f42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55f42-102">SYNOPSIS</span></span>
<span data-ttu-id="55f42-103">Adatbázis vagy rugalmas adatbázis létrehozása</span><span class="sxs-lookup"><span data-stu-id="55f42-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55f42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55f42-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55f42-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55f42-105">DESCRIPTION</span></span>
<span data-ttu-id="55f42-106">A **New-AzureRmSqlDatabase** PARANCSMAG Azure SQL-adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="55f42-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="55f42-107">Rugalmas adatbázist úgy is létrehozhat, hogy a *ElasticPoolName* paramétert egy meglévő rugalmas készletre állítja.</span><span class="sxs-lookup"><span data-stu-id="55f42-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="55f42-108">Példák</span><span class="sxs-lookup"><span data-stu-id="55f42-108">EXAMPLES</span></span>

### <span data-ttu-id="55f42-109">Példa 1: adatbázis létrehozása egy megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="55f42-109">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="55f42-110">A parancs létrehoz egy Database01 nevű adatbázist a kiszolgálók Server01.</span><span class="sxs-lookup"><span data-stu-id="55f42-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="55f42-111">2. példa: rugalmas adatbázis létrehozása egy megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="55f42-111">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="55f42-112">A parancs létrehoz egy Database01 nevű adatbázist a ElasticPool01 nevű rugalmas készletben a kiszolgálói Server01.</span><span class="sxs-lookup"><span data-stu-id="55f42-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="55f42-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55f42-113">PARAMETERS</span></span>

### <span data-ttu-id="55f42-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55f42-114">-AsJob</span></span>
<span data-ttu-id="55f42-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="55f42-115">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="55f42-116">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="55f42-116">-CatalogCollation</span></span>
<span data-ttu-id="55f42-117">Az SQL adatbázis-katalógus egybevetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55f42-117">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="55f42-118">-CollationName</span><span class="sxs-lookup"><span data-stu-id="55f42-118">-CollationName</span></span>
<span data-ttu-id="55f42-119">Az SQL-adatbázis egybevetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55f42-119">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="55f42-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="55f42-120">-DatabaseName</span></span>
<span data-ttu-id="55f42-121">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55f42-121">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f42-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f42-122">-DefaultProfile</span></span>
<span data-ttu-id="55f42-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="55f42-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55f42-124">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="55f42-124">-Edition</span></span>
<span data-ttu-id="55f42-125">Az adatbázishoz hozzárendelni kívánt kiadást adja meg.</span><span class="sxs-lookup"><span data-stu-id="55f42-125">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="55f42-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="55f42-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55f42-127">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="55f42-127">Default</span></span>
- <span data-ttu-id="55f42-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="55f42-128">None</span></span>
- <span data-ttu-id="55f42-129">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="55f42-129">Premium</span></span>
- <span data-ttu-id="55f42-130">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="55f42-130">Basic</span></span>
- <span data-ttu-id="55f42-131">Standard</span><span class="sxs-lookup"><span data-stu-id="55f42-131">Standard</span></span>
- <span data-ttu-id="55f42-132">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="55f42-132">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f42-133">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="55f42-133">-ElasticPoolName</span></span>
<span data-ttu-id="55f42-134">Annak a rugalmas készletnek a nevét adja meg, amelyben az adatbázist el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="55f42-134">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="55f42-135">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="55f42-135">-MaxSizeBytes</span></span>
<span data-ttu-id="55f42-136">Az adatbázis maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="55f42-136">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="55f42-137">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="55f42-137">-ReadScale</span></span>
<span data-ttu-id="55f42-138">Az Azure SQL-adatbázishoz rendelt olvasási méretarány beállítás. (Engedélyezve/letiltva)</span><span class="sxs-lookup"><span data-stu-id="55f42-138">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f42-139">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="55f42-139">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="55f42-140">Az adatbázishoz hozzárendelni kívánt szolgáltatási cél nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55f42-140">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="55f42-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f42-141">-ResourceGroupName</span></span>
<span data-ttu-id="55f42-142">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="55f42-142">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="55f42-143">-SampleName</span><span class="sxs-lookup"><span data-stu-id="55f42-143">-SampleName</span></span>
<span data-ttu-id="55f42-144">Az adatbázis létrehozásakor alkalmazandó minta-séma neve.</span><span class="sxs-lookup"><span data-stu-id="55f42-144">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f42-145">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="55f42-145">-ServerName</span></span>
<span data-ttu-id="55f42-146">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55f42-146">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="55f42-147">-Címkék</span><span class="sxs-lookup"><span data-stu-id="55f42-147">-Tags</span></span>
<span data-ttu-id="55f42-148">A kulcs-érték párok szótárát adja meg egy kivonatoló táblázat formájában, amelyre a parancsmag társítva van az új adatbázissal.</span><span class="sxs-lookup"><span data-stu-id="55f42-148">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="55f42-149">Példa:</span><span class="sxs-lookup"><span data-stu-id="55f42-149">For example:</span></span>

<span data-ttu-id="55f42-150">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="55f42-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f42-151">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="55f42-151">-ZoneRedundant</span></span>
<span data-ttu-id="55f42-152">A zóna redundancia az Azure SQL-adatbázishoz való társításhoz</span><span class="sxs-lookup"><span data-stu-id="55f42-152">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="55f42-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="55f42-153">-Confirm</span></span>
<span data-ttu-id="55f42-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="55f42-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55f42-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f42-155">-WhatIf</span></span>
<span data-ttu-id="55f42-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="55f42-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55f42-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55f42-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55f42-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f42-158">CommonParameters</span></span>
<span data-ttu-id="55f42-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55f42-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f42-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55f42-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f42-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55f42-161">INPUTS</span></span>

### <span data-ttu-id="55f42-162">Nincs</span><span class="sxs-lookup"><span data-stu-id="55f42-162">None</span></span>
<span data-ttu-id="55f42-163">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="55f42-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55f42-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55f42-164">OUTPUTS</span></span>

### <span data-ttu-id="55f42-165">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="55f42-165">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="55f42-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55f42-166">NOTES</span></span>

## <span data-ttu-id="55f42-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55f42-167">RELATED LINKS</span></span>

[<span data-ttu-id="55f42-168">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55f42-168">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="55f42-169">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="55f42-169">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="55f42-170">Új – AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="55f42-170">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="55f42-171">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55f42-171">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="55f42-172">Önéletrajz – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55f42-172">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="55f42-173">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55f42-173">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="55f42-174">Felfüggesztés – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55f42-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="55f42-175">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="55f42-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
