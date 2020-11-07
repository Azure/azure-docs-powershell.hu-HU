---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 7eaa753b973b887cbbddc132b998d05f3e374e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679815"
---
# <span data-ttu-id="bd145-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd145-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="bd145-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd145-102">SYNOPSIS</span></span>
<span data-ttu-id="bd145-103">Adatbázis vagy rugalmas adatbázis létrehozása</span><span class="sxs-lookup"><span data-stu-id="bd145-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd145-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd145-104">SYNTAX</span></span>

### <span data-ttu-id="bd145-105">DtuBasedDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd145-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd145-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="bd145-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd145-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd145-107">DESCRIPTION</span></span>
<span data-ttu-id="bd145-108">A **New-AzureRmSqlDatabase** PARANCSMAG Azure SQL-adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bd145-108">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="bd145-109">Rugalmas adatbázist úgy is létrehozhat, hogy a *ElasticPoolName* paramétert egy meglévő rugalmas készletre állítja.</span><span class="sxs-lookup"><span data-stu-id="bd145-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="bd145-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bd145-110">EXAMPLES</span></span>

### <span data-ttu-id="bd145-111">Példa 1: adatbázis létrehozása egy megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="bd145-111">Example 1: Create a database on a specified server</span></span>
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
LicenseType                   :
Tags                          :
```

<span data-ttu-id="bd145-112">A parancs létrehoz egy Database01 nevű adatbázist a kiszolgálók Server01.</span><span class="sxs-lookup"><span data-stu-id="bd145-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="bd145-113">2. példa: rugalmas adatbázis létrehozása egy megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="bd145-113">Example 2: Create an elastic database on a specified server</span></span>
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
LicenseType                   :
Tags                          :
```

<span data-ttu-id="bd145-114">A parancs létrehoz egy Database02 nevű adatbázist a ElasticPool01 nevű rugalmas készletben a kiszolgálói Server01.</span><span class="sxs-lookup"><span data-stu-id="bd145-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="bd145-115">3. példa: vcore-adatbázis létrehozása egy megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="bd145-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="bd145-116">Ez a parancs létrehoz egy Database03 nevű vcore-adatbázist a kiszolgálói Server01.</span><span class="sxs-lookup"><span data-stu-id="bd145-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="bd145-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd145-117">PARAMETERS</span></span>

### <span data-ttu-id="bd145-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd145-118">-AsJob</span></span>
<span data-ttu-id="bd145-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bd145-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd145-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="bd145-120">-CatalogCollation</span></span>
<span data-ttu-id="bd145-121">Az SQL adatbázis-katalógus egybevetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd145-121">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="bd145-122">-CollationName</span></span>
<span data-ttu-id="bd145-123">Az SQL-adatbázis egybevetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd145-123">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="bd145-124">-ComputeGeneration</span></span>
<span data-ttu-id="bd145-125">A hozzárendelni kívánt számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="bd145-125">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd145-126">-DatabaseName</span></span>
<span data-ttu-id="bd145-127">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd145-127">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd145-128">-DefaultProfile</span></span>
<span data-ttu-id="bd145-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bd145-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd145-130">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="bd145-130">-Edition</span></span>
<span data-ttu-id="bd145-131">Az adatbázishoz hozzárendelni kívánt kiadást adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd145-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="bd145-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bd145-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bd145-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="bd145-133">None</span></span>
- <span data-ttu-id="bd145-134">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="bd145-134">Basic</span></span>
- <span data-ttu-id="bd145-135">Standard</span><span class="sxs-lookup"><span data-stu-id="bd145-135">Standard</span></span>
- <span data-ttu-id="bd145-136">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="bd145-136">Premium</span></span>
- <span data-ttu-id="bd145-137">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="bd145-137">DataWarehouse</span></span>
- <span data-ttu-id="bd145-138">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="bd145-138">Free</span></span>
- <span data-ttu-id="bd145-139">Nyúlik</span><span class="sxs-lookup"><span data-stu-id="bd145-139">Stretch</span></span>
- <span data-ttu-id="bd145-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="bd145-140">GeneralPurpose</span></span>
- <span data-ttu-id="bd145-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="bd145-141">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="bd145-142">-ElasticPoolName</span></span>
<span data-ttu-id="bd145-143">Annak a rugalmas készletnek a nevét adja meg, amelyben az adatbázist el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="bd145-143">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="bd145-144">-LicenseType</span></span>
<span data-ttu-id="bd145-145">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="bd145-145">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-146">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="bd145-146">-MaxSizeBytes</span></span>
<span data-ttu-id="bd145-147">Az adatbázis maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="bd145-147">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-148">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="bd145-148">-ReadScale</span></span>
<span data-ttu-id="bd145-149">Az Azure SQL-adatbázishoz rendelt olvasási méretarány beállítás. (Engedélyezve/letiltva)</span><span class="sxs-lookup"><span data-stu-id="bd145-149">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-150">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="bd145-150">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="bd145-151">Az adatbázishoz hozzárendelni kívánt szolgáltatási cél nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd145-151">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd145-152">-ResourceGroupName</span></span>
<span data-ttu-id="bd145-153">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="bd145-153">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="bd145-154">-SampleName</span><span class="sxs-lookup"><span data-stu-id="bd145-154">-SampleName</span></span>
<span data-ttu-id="bd145-155">Az adatbázis létrehozásakor alkalmazandó minta-séma neve.</span><span class="sxs-lookup"><span data-stu-id="bd145-155">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-156">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="bd145-156">-ServerName</span></span>
<span data-ttu-id="bd145-157">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd145-157">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="bd145-158">-Címkék</span><span class="sxs-lookup"><span data-stu-id="bd145-158">-Tags</span></span>
<span data-ttu-id="bd145-159">A kulcs-érték párok szótárát adja meg egy kivonatoló táblázat formájában, amelyre a parancsmag társítva van az új adatbázissal.</span><span class="sxs-lookup"><span data-stu-id="bd145-159">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="bd145-160">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="bd145-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="bd145-161">-VCore</span></span>
<span data-ttu-id="bd145-162">Az Azure SQL-adatbázis vcore száma</span><span class="sxs-lookup"><span data-stu-id="bd145-162">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd145-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="bd145-163">-ZoneRedundant</span></span>
<span data-ttu-id="bd145-164">A zóna redundancia az Azure SQL-adatbázishoz való társításhoz</span><span class="sxs-lookup"><span data-stu-id="bd145-164">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="bd145-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bd145-165">-Confirm</span></span>
<span data-ttu-id="bd145-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bd145-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd145-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd145-167">-WhatIf</span></span>
<span data-ttu-id="bd145-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bd145-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd145-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd145-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd145-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd145-170">CommonParameters</span></span>
<span data-ttu-id="bd145-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd145-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd145-172">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd145-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd145-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd145-173">INPUTS</span></span>

### <span data-ttu-id="bd145-174">System. String</span><span class="sxs-lookup"><span data-stu-id="bd145-174">System.String</span></span>

## <span data-ttu-id="bd145-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd145-175">OUTPUTS</span></span>

### <span data-ttu-id="bd145-176">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bd145-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="bd145-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd145-177">NOTES</span></span>

## <span data-ttu-id="bd145-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd145-178">RELATED LINKS</span></span>

[<span data-ttu-id="bd145-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd145-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="bd145-180">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bd145-180">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="bd145-181">Új – AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="bd145-181">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="bd145-182">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd145-182">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="bd145-183">Önéletrajz – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd145-183">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="bd145-184">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd145-184">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="bd145-185">Felfüggesztés – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bd145-185">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="bd145-186">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bd145-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

