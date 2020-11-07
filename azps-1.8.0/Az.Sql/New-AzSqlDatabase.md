---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: ff474116854838c40a4862cf93f4d017ccdf4527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668908"
---
# <span data-ttu-id="36346-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36346-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="36346-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36346-102">SYNOPSIS</span></span>
<span data-ttu-id="36346-103">Adatbázis vagy rugalmas adatbázis létrehozása</span><span class="sxs-lookup"><span data-stu-id="36346-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="36346-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36346-104">SYNTAX</span></span>

### <span data-ttu-id="36346-105">DtuBasedDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36346-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36346-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="36346-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36346-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="36346-107">DESCRIPTION</span></span>
<span data-ttu-id="36346-108">A **New-AzSqlDatabase** PARANCSMAG Azure SQL-adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="36346-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="36346-109">Rugalmas adatbázist úgy is létrehozhat, hogy a *ElasticPoolName* paramétert egy meglévő rugalmas készletre állítja.</span><span class="sxs-lookup"><span data-stu-id="36346-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="36346-110">Példák</span><span class="sxs-lookup"><span data-stu-id="36346-110">EXAMPLES</span></span>

### <span data-ttu-id="36346-111">Példa 1: adatbázis létrehozása egy megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="36346-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="36346-112">A parancs létrehoz egy Database01 nevű adatbázist a kiszolgálók Server01.</span><span class="sxs-lookup"><span data-stu-id="36346-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="36346-113">2. példa: rugalmas adatbázis létrehozása egy megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="36346-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="36346-114">A parancs létrehoz egy Database02 nevű adatbázist a ElasticPool01 nevű rugalmas készletben a kiszolgálói Server01.</span><span class="sxs-lookup"><span data-stu-id="36346-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="36346-115">3. példa: vcore-adatbázis létrehozása egy megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="36346-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
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

<span data-ttu-id="36346-116">Ez a parancs létrehoz egy Database03 nevű vcore-adatbázist a kiszolgálói Server01.</span><span class="sxs-lookup"><span data-stu-id="36346-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="36346-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36346-117">PARAMETERS</span></span>

### <span data-ttu-id="36346-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36346-118">-AsJob</span></span>
<span data-ttu-id="36346-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="36346-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36346-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="36346-120">-CatalogCollation</span></span>
<span data-ttu-id="36346-121">Az SQL adatbázis-katalógus egybevetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36346-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="36346-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="36346-122">-CollationName</span></span>
<span data-ttu-id="36346-123">Az SQL-adatbázis egybevetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36346-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="36346-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="36346-124">-ComputeGeneration</span></span>
<span data-ttu-id="36346-125">A hozzárendelni kívánt számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="36346-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="36346-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36346-126">-DatabaseName</span></span>
<span data-ttu-id="36346-127">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36346-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="36346-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36346-128">-DefaultProfile</span></span>
<span data-ttu-id="36346-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="36346-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36346-130">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="36346-130">-Edition</span></span>
<span data-ttu-id="36346-131">Az adatbázishoz hozzárendelni kívánt kiadást adja meg.</span><span class="sxs-lookup"><span data-stu-id="36346-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="36346-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="36346-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="36346-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="36346-133">None</span></span>
- <span data-ttu-id="36346-134">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="36346-134">Basic</span></span>
- <span data-ttu-id="36346-135">Standard</span><span class="sxs-lookup"><span data-stu-id="36346-135">Standard</span></span>
- <span data-ttu-id="36346-136">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="36346-136">Premium</span></span>
- <span data-ttu-id="36346-137">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="36346-137">DataWarehouse</span></span>
- <span data-ttu-id="36346-138">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="36346-138">Free</span></span>
- <span data-ttu-id="36346-139">Nyúlik</span><span class="sxs-lookup"><span data-stu-id="36346-139">Stretch</span></span>
- <span data-ttu-id="36346-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="36346-140">GeneralPurpose</span></span>
- <span data-ttu-id="36346-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="36346-141">BusinessCritical</span></span>

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

### <span data-ttu-id="36346-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="36346-142">-ElasticPoolName</span></span>
<span data-ttu-id="36346-143">Annak a rugalmas készletnek a nevét adja meg, amelyben az adatbázist el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="36346-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="36346-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="36346-144">-LicenseType</span></span>
<span data-ttu-id="36346-145">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="36346-145">The license type for the Azure Sql database.</span></span> <span data-ttu-id="36346-146">A lehetséges értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="36346-146">Possible values are:</span></span>
- <span data-ttu-id="36346-147">BasePrice – Azure hibrid haszon (AHB) a meglévő SQL Server-licenccel rendelkező tulajdonosok kedvezményes árait alkalmazzák.</span><span class="sxs-lookup"><span data-stu-id="36346-147">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="36346-148">Az adatbázis ára a meglévő SQL Server-licenccel rendelkező tulajdonosok számára diszkontálva lesz.</span><span class="sxs-lookup"><span data-stu-id="36346-148">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="36346-149">A LicenseIncluded-Azure Hybrid haszon (AHB) árengedménye nem érvényes a meglévő SQL Server-licenccel rendelkező tulajdonosok esetében.</span><span class="sxs-lookup"><span data-stu-id="36346-149">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="36346-150">Az adatbázis ára tartalmazni fogja az új SQL Server-licencek költségeit.</span><span class="sxs-lookup"><span data-stu-id="36346-150">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="36346-151">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="36346-151">-MaxSizeBytes</span></span>
<span data-ttu-id="36346-152">Az adatbázis maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="36346-152">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="36346-153">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="36346-153">-ReadScale</span></span>
<span data-ttu-id="36346-154">Az Azure SQL-adatbázishoz rendelt olvasási méretarány beállítás. (Engedélyezve/letiltva)</span><span class="sxs-lookup"><span data-stu-id="36346-154">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="36346-155">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="36346-155">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="36346-156">Az adatbázishoz hozzárendelni kívánt szolgáltatási cél nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36346-156">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="36346-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36346-157">-ResourceGroupName</span></span>
<span data-ttu-id="36346-158">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="36346-158">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="36346-159">-SampleName</span><span class="sxs-lookup"><span data-stu-id="36346-159">-SampleName</span></span>
<span data-ttu-id="36346-160">Az adatbázis létrehozásakor alkalmazandó minta-séma neve.</span><span class="sxs-lookup"><span data-stu-id="36346-160">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="36346-161">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="36346-161">-ServerName</span></span>
<span data-ttu-id="36346-162">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36346-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="36346-163">-Címkék</span><span class="sxs-lookup"><span data-stu-id="36346-163">-Tags</span></span>
<span data-ttu-id="36346-164">A kulcs-érték párok szótárát adja meg egy kivonatoló táblázat formájában, amelyre a parancsmag társítva van az új adatbázissal.</span><span class="sxs-lookup"><span data-stu-id="36346-164">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="36346-165">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="36346-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="36346-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="36346-166">-VCore</span></span>
<span data-ttu-id="36346-167">Az Azure SQL-adatbázis vcore száma</span><span class="sxs-lookup"><span data-stu-id="36346-167">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="36346-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="36346-168">-ZoneRedundant</span></span>
<span data-ttu-id="36346-169">A zóna redundancia az Azure SQL-adatbázishoz való társításhoz</span><span class="sxs-lookup"><span data-stu-id="36346-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="36346-170">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36346-170">-Confirm</span></span>
<span data-ttu-id="36346-171">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36346-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36346-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36346-172">-WhatIf</span></span>
<span data-ttu-id="36346-173">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36346-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36346-174">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36346-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36346-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36346-175">CommonParameters</span></span>
<span data-ttu-id="36346-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36346-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36346-177">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="36346-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36346-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36346-178">INPUTS</span></span>

### <span data-ttu-id="36346-179">System. String</span><span class="sxs-lookup"><span data-stu-id="36346-179">System.String</span></span>

## <span data-ttu-id="36346-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36346-180">OUTPUTS</span></span>

### <span data-ttu-id="36346-181">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="36346-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="36346-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36346-182">NOTES</span></span>

## <span data-ttu-id="36346-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36346-183">RELATED LINKS</span></span>

[<span data-ttu-id="36346-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36346-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="36346-185">Új – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="36346-185">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="36346-186">Új – AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="36346-186">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="36346-187">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36346-187">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="36346-188">Önéletrajz – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36346-188">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="36346-189">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36346-189">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="36346-190">Felfüggesztés – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="36346-190">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="36346-191">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="36346-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

