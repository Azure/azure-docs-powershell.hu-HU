---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: f7dbffffe9a51d35ced8861894373322898fd0f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012468"
---
# <span data-ttu-id="4543b-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4543b-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="4543b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4543b-102">SYNOPSIS</span></span>
<span data-ttu-id="4543b-103">Egy meglévő adatbázis másodlagos adatbázisát hozza létre, és elindítja az adatreplikálást.</span><span class="sxs-lookup"><span data-stu-id="4543b-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="4543b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4543b-104">SYNTAX</span></span>

### <span data-ttu-id="4543b-105">DtuBasedDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4543b-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4543b-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="4543b-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4543b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4543b-107">DESCRIPTION</span></span>
<span data-ttu-id="4543b-108">A **New-AzSqlDatabaseSecondary** parancsmag lecseréli az Start-AzSqlDatabaseCopy parancsmagot az adatbázis földrajzi replikálásának beállításához.</span><span class="sxs-lookup"><span data-stu-id="4543b-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="4543b-109">Az elsődlegestől a másodlagos adatbázishoz tartozó geo-replikációs hivatkozás objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4543b-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="4543b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4543b-110">EXAMPLES</span></span>

### <span data-ttu-id="4543b-111">1: aktív Geo-Replication létrehozása</span><span class="sxs-lookup"><span data-stu-id="4543b-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="4543b-112">2: az aktív Geo-Replication létrehozása és a partner adatbázis nevének meghatározása a forrás adatbázis nevétől eltérő értékre</span><span class="sxs-lookup"><span data-stu-id="4543b-112">2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="4543b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4543b-113">PARAMETERS</span></span>

### <span data-ttu-id="4543b-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="4543b-114">-AllowConnections</span></span>
<span data-ttu-id="4543b-115">A másodlagos Azure SQL-adatbázis olvasási szándékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4543b-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="4543b-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4543b-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4543b-117">nem</span><span class="sxs-lookup"><span data-stu-id="4543b-117">No</span></span>
- <span data-ttu-id="4543b-118">Minden</span><span class="sxs-lookup"><span data-stu-id="4543b-118">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Replication.Model.AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4543b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4543b-119">-AsJob</span></span>
<span data-ttu-id="4543b-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4543b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4543b-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4543b-121">-DatabaseName</span></span>
<span data-ttu-id="4543b-122">Annak az adatbázisnak a nevét adja meg, amely az elsődlegesként működik.</span><span class="sxs-lookup"><span data-stu-id="4543b-122">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4543b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4543b-123">-DefaultProfile</span></span>
<span data-ttu-id="4543b-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4543b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4543b-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4543b-125">-LicenseType</span></span>
<span data-ttu-id="4543b-126">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="4543b-126">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="4543b-127">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4543b-127">-PartnerDatabaseName</span></span>
<span data-ttu-id="4543b-128">A létrehozandó másodlagos adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="4543b-128">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="4543b-129">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4543b-129">-PartnerResourceGroupName</span></span>
<span data-ttu-id="4543b-130">Annak az Azure erőforrás-csoportnak a neve, amelyhez a parancsmag a másodlagos adatbázist rendeli.</span><span class="sxs-lookup"><span data-stu-id="4543b-130">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4543b-131">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="4543b-131">-PartnerServerName</span></span>
<span data-ttu-id="4543b-132">Annak az Azure SQL adatbázis-kiszolgálónak a nevét adja meg, amely másodlagosként működik.</span><span class="sxs-lookup"><span data-stu-id="4543b-132">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4543b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4543b-133">-ResourceGroupName</span></span>
<span data-ttu-id="4543b-134">Annak az Azure erőforrás-csoportnak a neve, amelyhez a parancsmag az elsődleges adatbázist rendeli.</span><span class="sxs-lookup"><span data-stu-id="4543b-134">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="4543b-135">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="4543b-135">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="4543b-136">A másodlagos Azure SQL-adatbázis számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="4543b-136">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="4543b-137">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4543b-137">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="4543b-138">Annak a rugalmas készletnek a nevét adja meg, amelybe a másodlagos adatbázist el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="4543b-138">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="4543b-139">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="4543b-139">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="4543b-140">Annak a szolgáltatási célnak a nevét adja meg, amelyet a másodlagos adatbázishoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="4543b-140">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="4543b-141">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="4543b-141">-SecondaryVCore</span></span>
<span data-ttu-id="4543b-142">Az Azure SQL-adatbázis másodlagos vcore száma.</span><span class="sxs-lookup"><span data-stu-id="4543b-142">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="4543b-143">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="4543b-143">-ServerName</span></span>
<span data-ttu-id="4543b-144">Az elsődleges SQL-adatbázis SQL-kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4543b-144">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="4543b-145">-Címkék</span><span class="sxs-lookup"><span data-stu-id="4543b-145">-Tags</span></span>
<span data-ttu-id="4543b-146">Az SQL-adatbázis replikációs hivatkozásával társítani kívánt kivonatoló táblázat kulcs-érték párokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="4543b-146">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="4543b-147">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="4543b-147">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4543b-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4543b-148">-Confirm</span></span>
<span data-ttu-id="4543b-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4543b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4543b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4543b-150">-WhatIf</span></span>
<span data-ttu-id="4543b-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4543b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4543b-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4543b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4543b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4543b-153">CommonParameters</span></span>
<span data-ttu-id="4543b-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4543b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4543b-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4543b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4543b-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4543b-156">INPUTS</span></span>

### <span data-ttu-id="4543b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="4543b-157">System.String</span></span>

## <span data-ttu-id="4543b-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4543b-158">OUTPUTS</span></span>

### <span data-ttu-id="4543b-159">Microsoft. Azure. Command. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="4543b-159">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="4543b-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4543b-160">NOTES</span></span>

## <span data-ttu-id="4543b-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4543b-161">RELATED LINKS</span></span>

[<span data-ttu-id="4543b-162">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4543b-162">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="4543b-163">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4543b-163">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="4543b-164">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4543b-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
