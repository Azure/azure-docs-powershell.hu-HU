---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 0b0934ffe9a5721ff08438ca7a24d97e2b4a34cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186981"
---
# <span data-ttu-id="70196-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="70196-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="70196-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70196-102">SYNOPSIS</span></span>
<span data-ttu-id="70196-103">Egy meglévő adatbázis másodlagos adatbázisát hozza létre, és elindítja az adatreplikálást.</span><span class="sxs-lookup"><span data-stu-id="70196-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="70196-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70196-104">SYNTAX</span></span>

### <span data-ttu-id="70196-105">DtuBasedDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70196-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70196-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="70196-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70196-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="70196-107">DESCRIPTION</span></span>
<span data-ttu-id="70196-108">A **New-AzSqlDatabaseSecondary** parancsmag lecseréli az Start-AzSqlDatabaseCopy parancsmagot az adatbázis földrajzi replikálásának beállításához.</span><span class="sxs-lookup"><span data-stu-id="70196-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="70196-109">Az elsődlegestől a másodlagos adatbázishoz tartozó geo-replikációs hivatkozás objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="70196-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="70196-110">Példák</span><span class="sxs-lookup"><span data-stu-id="70196-110">EXAMPLES</span></span>

### <span data-ttu-id="70196-111">1. példa: aktív Geo-Replication létrehozása</span><span class="sxs-lookup"><span data-stu-id="70196-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="70196-112">2. példa: az aktív Geo-Replication létrehozása és a partner adatbázis nevének meghatározása a forrás adatbázis nevétől eltérő értékre</span><span class="sxs-lookup"><span data-stu-id="70196-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="70196-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70196-113">PARAMETERS</span></span>

### <span data-ttu-id="70196-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="70196-114">-AllowConnections</span></span>
<span data-ttu-id="70196-115">A másodlagos Azure SQL-adatbázis olvasási szándékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="70196-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="70196-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="70196-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="70196-117">nem</span><span class="sxs-lookup"><span data-stu-id="70196-117">No</span></span>
- <span data-ttu-id="70196-118">Minden</span><span class="sxs-lookup"><span data-stu-id="70196-118">All</span></span>

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

### <span data-ttu-id="70196-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70196-119">-AsJob</span></span>
<span data-ttu-id="70196-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="70196-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70196-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="70196-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="70196-122">Az SQL-adatbázis biztonsági mentéseit tároló biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="70196-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="70196-123">A beállítások a következők: helyi, zóna és Geo.</span><span class="sxs-lookup"><span data-stu-id="70196-123">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70196-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="70196-124">-DatabaseName</span></span>
<span data-ttu-id="70196-125">Annak az adatbázisnak a nevét adja meg, amely az elsődlegesként működik.</span><span class="sxs-lookup"><span data-stu-id="70196-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="70196-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70196-126">-DefaultProfile</span></span>
<span data-ttu-id="70196-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="70196-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70196-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="70196-128">-LicenseType</span></span>
<span data-ttu-id="70196-129">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="70196-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="70196-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="70196-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="70196-131">A létrehozandó másodlagos adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="70196-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="70196-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70196-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="70196-133">Annak az Azure erőforrás-csoportnak a neve, amelyhez a parancsmag a másodlagos adatbázist rendeli.</span><span class="sxs-lookup"><span data-stu-id="70196-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="70196-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="70196-134">-PartnerServerName</span></span>
<span data-ttu-id="70196-135">Annak az Azure SQL adatbázis-kiszolgálónak a nevét adja meg, amely másodlagosként működik.</span><span class="sxs-lookup"><span data-stu-id="70196-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="70196-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70196-136">-ResourceGroupName</span></span>
<span data-ttu-id="70196-137">Annak az Azure erőforrás-csoportnak a neve, amelyhez a parancsmag az elsődleges adatbázist rendeli.</span><span class="sxs-lookup"><span data-stu-id="70196-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="70196-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="70196-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="70196-139">A másodlagos Azure SQL-adatbázis számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="70196-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="70196-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="70196-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="70196-141">Annak a rugalmas készletnek a nevét adja meg, amelybe a másodlagos adatbázist el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="70196-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="70196-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="70196-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="70196-143">Annak a szolgáltatási célnak a nevét adja meg, amelyet a másodlagos adatbázishoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="70196-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="70196-144">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="70196-144">-SecondaryVCore</span></span>
<span data-ttu-id="70196-145">Az Azure SQL-adatbázis másodlagos vcore száma.</span><span class="sxs-lookup"><span data-stu-id="70196-145">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="70196-146">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="70196-146">-ServerName</span></span>
<span data-ttu-id="70196-147">Az elsődleges SQL-adatbázis SQL-kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70196-147">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="70196-148">-Címkék</span><span class="sxs-lookup"><span data-stu-id="70196-148">-Tags</span></span>
<span data-ttu-id="70196-149">Az SQL-adatbázis replikációs hivatkozásával társítani kívánt kivonatoló táblázat kulcs-érték párokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="70196-149">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="70196-150">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="70196-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="70196-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70196-151">-Confirm</span></span>
<span data-ttu-id="70196-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70196-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70196-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70196-153">-WhatIf</span></span>
<span data-ttu-id="70196-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70196-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70196-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70196-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70196-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70196-156">CommonParameters</span></span>
<span data-ttu-id="70196-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70196-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70196-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="70196-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70196-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70196-159">INPUTS</span></span>

### <span data-ttu-id="70196-160">System. String</span><span class="sxs-lookup"><span data-stu-id="70196-160">System.String</span></span>

## <span data-ttu-id="70196-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70196-161">OUTPUTS</span></span>

### <span data-ttu-id="70196-162">Microsoft. Azure. Command. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="70196-162">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="70196-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70196-163">NOTES</span></span>

## <span data-ttu-id="70196-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70196-164">RELATED LINKS</span></span>

[<span data-ttu-id="70196-165">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="70196-165">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="70196-166">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="70196-166">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="70196-167">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="70196-167">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
