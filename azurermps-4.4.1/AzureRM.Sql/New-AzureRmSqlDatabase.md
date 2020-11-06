---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 22b74b3dcd76577d7c864a3779d12c8474c431a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493328"
---
# <span data-ttu-id="bbc62-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bbc62-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="bbc62-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bbc62-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc62-103">Adatbázis vagy rugalmas adatbázis létrehozása</span><span class="sxs-lookup"><span data-stu-id="bbc62-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbc62-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bbc62-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbc62-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bbc62-105">DESCRIPTION</span></span>
<span data-ttu-id="bbc62-106">A **New-AzureRmSqlDatabase** PARANCSMAG Azure SQL-adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bbc62-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="bbc62-107">Rugalmas adatbázist úgy is létrehozhat, hogy a *ElasticPoolName* paramétert egy meglévő rugalmas készletre állítja.</span><span class="sxs-lookup"><span data-stu-id="bbc62-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="bbc62-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bbc62-108">EXAMPLES</span></span>

### <span data-ttu-id="bbc62-109">Példa 1: adatbázis létrehozása egy megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="bbc62-109">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="bbc62-110">A parancs létrehoz egy Database01 nevű adatbázist a kiszolgálók Server01.</span><span class="sxs-lookup"><span data-stu-id="bbc62-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="bbc62-111">2. példa: rugalmas adatbázis létrehozása egy megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="bbc62-111">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="bbc62-112">A parancs létrehoz egy Database01 nevű adatbázist a ElasticPool01 nevű rugalmas készletben a kiszolgálói Server01.</span><span class="sxs-lookup"><span data-stu-id="bbc62-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="bbc62-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bbc62-113">PARAMETERS</span></span>

### <span data-ttu-id="bbc62-114">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="bbc62-114">-CatalogCollation</span></span>
<span data-ttu-id="bbc62-115">Az SQL adatbázis-katalógus egybevetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbc62-115">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="bbc62-116">-CollationName</span><span class="sxs-lookup"><span data-stu-id="bbc62-116">-CollationName</span></span>
<span data-ttu-id="bbc62-117">Az SQL-adatbázis egybevetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbc62-117">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="bbc62-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bbc62-118">-DatabaseName</span></span>
<span data-ttu-id="bbc62-119">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbc62-119">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="bbc62-120">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="bbc62-120">-Edition</span></span>
<span data-ttu-id="bbc62-121">Az adatbázishoz hozzárendelni kívánt kiadást adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbc62-121">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="bbc62-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bbc62-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bbc62-123">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="bbc62-123">Default</span></span>
- <span data-ttu-id="bbc62-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="bbc62-124">None</span></span>
- <span data-ttu-id="bbc62-125">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="bbc62-125">Premium</span></span>
- <span data-ttu-id="bbc62-126">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="bbc62-126">Basic</span></span>
- <span data-ttu-id="bbc62-127">Standard</span><span class="sxs-lookup"><span data-stu-id="bbc62-127">Standard</span></span>
- <span data-ttu-id="bbc62-128">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="bbc62-128">DataWarehouse</span></span>
- <span data-ttu-id="bbc62-129">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="bbc62-129">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc62-130">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="bbc62-130">-ElasticPoolName</span></span>
<span data-ttu-id="bbc62-131">Annak a rugalmas készletnek a nevét adja meg, amelyben az adatbázist el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="bbc62-131">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="bbc62-132">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="bbc62-132">-MaxSizeBytes</span></span>
<span data-ttu-id="bbc62-133">Az adatbázis maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="bbc62-133">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="bbc62-134">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="bbc62-134">-ReadScale</span></span>
<span data-ttu-id="bbc62-135">Az Azure SQL-adatbázishoz rendelt olvasási méretarány beállítás. (Engedélyezve/letiltva)</span><span class="sxs-lookup"><span data-stu-id="bbc62-135">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="bbc62-136">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="bbc62-136">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="bbc62-137">Az adatbázishoz hozzárendelni kívánt szolgáltatási cél nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbc62-137">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="bbc62-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbc62-138">-ResourceGroupName</span></span>
<span data-ttu-id="bbc62-139">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="bbc62-139">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="bbc62-140">-SampleName</span><span class="sxs-lookup"><span data-stu-id="bbc62-140">-SampleName</span></span>
<span data-ttu-id="bbc62-141">Az adatbázis létrehozásakor alkalmazandó minta-séma neve.</span><span class="sxs-lookup"><span data-stu-id="bbc62-141">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="bbc62-142">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="bbc62-142">-ServerName</span></span>
<span data-ttu-id="bbc62-143">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bbc62-143">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="bbc62-144">-Címkék</span><span class="sxs-lookup"><span data-stu-id="bbc62-144">-Tags</span></span>
<span data-ttu-id="bbc62-145">A kulcs-érték párok szótárát adja meg egy kivonatoló táblázat formájában, amelyre a parancsmag társítva van az új adatbázissal.</span><span class="sxs-lookup"><span data-stu-id="bbc62-145">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="bbc62-146">Példa:</span><span class="sxs-lookup"><span data-stu-id="bbc62-146">For example:</span></span>

<span data-ttu-id="bbc62-147">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="bbc62-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bbc62-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bbc62-148">-Confirm</span></span>
<span data-ttu-id="bbc62-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bbc62-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbc62-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc62-150">-WhatIf</span></span>
<span data-ttu-id="bbc62-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bbc62-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbc62-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bbc62-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbc62-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc62-153">-DefaultProfile</span></span>
<span data-ttu-id="bbc62-154">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bbc62-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbc62-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc62-155">CommonParameters</span></span>
<span data-ttu-id="bbc62-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bbc62-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc62-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbc62-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc62-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbc62-158">INPUTS</span></span>

## <span data-ttu-id="bbc62-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbc62-159">OUTPUTS</span></span>

### <span data-ttu-id="bbc62-160">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bbc62-160">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="bbc62-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bbc62-161">NOTES</span></span>

## <span data-ttu-id="bbc62-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbc62-162">RELATED LINKS</span></span>

[<span data-ttu-id="bbc62-163">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bbc62-163">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="bbc62-164">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bbc62-164">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="bbc62-165">Új – AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="bbc62-165">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="bbc62-166">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bbc62-166">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="bbc62-167">Önéletrajz – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bbc62-167">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="bbc62-168">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bbc62-168">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="bbc62-169">Felfüggesztés – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bbc62-169">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="bbc62-170">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bbc62-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
