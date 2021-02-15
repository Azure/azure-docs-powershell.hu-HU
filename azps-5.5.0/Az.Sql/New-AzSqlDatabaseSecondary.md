---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: cc8881657c541a15ade44242ab5fb0e84c9bbab8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145651"
---
# <span data-ttu-id="30d78-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="30d78-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="30d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30d78-102">SYNOPSIS</span></span>
<span data-ttu-id="30d78-103">Létrehoz egy másodlagos adatbázist egy meglévő adatbázishoz, és megkezdi az adatreplikációt.</span><span class="sxs-lookup"><span data-stu-id="30d78-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="30d78-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="30d78-104">SYNTAX</span></span>

### <span data-ttu-id="30d78-105">DtuBasedDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30d78-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30d78-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="30d78-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30d78-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="30d78-107">DESCRIPTION</span></span>
<span data-ttu-id="30d78-108">A **New-AzSqlDatabaseSecondary** parancsmag lecseréli a Start-AzSqlDatabaseCopy parancsmagot, amikor georeplikációt hoz létre egy adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="30d78-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="30d78-109">Visszaadja a geo replikációs kapcsolatobjektumot az elsődlegesről a másodlagos adatbázisra.</span><span class="sxs-lookup"><span data-stu-id="30d78-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="30d78-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="30d78-110">EXAMPLES</span></span>

### <span data-ttu-id="30d78-111">1. példa: Aktív Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="30d78-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="30d78-112">2. példa: Az Geo-Replication létrehozása és a partneradatbázis nevének megadása a forrásadatbázis nevétől eltérőre</span><span class="sxs-lookup"><span data-stu-id="30d78-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="30d78-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30d78-113">PARAMETERS</span></span>

### <span data-ttu-id="30d78-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="30d78-114">-AllowConnections</span></span>
<span data-ttu-id="30d78-115">A másodlagos Azure SQL-adatbázis olvasási célját adja meg.</span><span class="sxs-lookup"><span data-stu-id="30d78-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="30d78-116">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="30d78-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30d78-117">nem</span><span class="sxs-lookup"><span data-stu-id="30d78-117">No</span></span>
- <span data-ttu-id="30d78-118">Mind</span><span class="sxs-lookup"><span data-stu-id="30d78-118">All</span></span>

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

### <span data-ttu-id="30d78-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30d78-119">-AsJob</span></span>
<span data-ttu-id="30d78-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="30d78-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30d78-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="30d78-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="30d78-122">Az SQL-adatbázis biztonsági másolatai tárolásához használt biztonsági mentési tárterület redundancia.</span><span class="sxs-lookup"><span data-stu-id="30d78-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="30d78-123">A beállítások a helyi, a zóna és a földrajzi hely.</span><span class="sxs-lookup"><span data-stu-id="30d78-123">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="30d78-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30d78-124">-DatabaseName</span></span>
<span data-ttu-id="30d78-125">Megadja az elsődlegesként viselkedő adatbázis nevét.</span><span class="sxs-lookup"><span data-stu-id="30d78-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="30d78-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d78-126">-DefaultProfile</span></span>
<span data-ttu-id="30d78-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="30d78-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30d78-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="30d78-128">-LicenseType</span></span>
<span data-ttu-id="30d78-129">Az Azure Sql-adatbázis licenctípusa.</span><span class="sxs-lookup"><span data-stu-id="30d78-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="30d78-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="30d78-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="30d78-131">A létrehozni szükséges másodlagos adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="30d78-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="30d78-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30d78-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="30d78-133">Annak az Azure Erőforráscsoportnak a nevét adja meg, amelyhez a parancsmag hozzárendeli a másodlagos adatbázist.</span><span class="sxs-lookup"><span data-stu-id="30d78-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="30d78-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="30d78-134">-PartnerServerName</span></span>
<span data-ttu-id="30d78-135">Megadja annak az Azure SQL-adatbáziskiszolgálónak a nevét, amely másodlagosként működik.</span><span class="sxs-lookup"><span data-stu-id="30d78-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="30d78-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30d78-136">-ResourceGroupName</span></span>
<span data-ttu-id="30d78-137">Annak az Azure Erőforráscsoportnak a nevét adja meg, amelyhez ez a parancsmag hozzárendeli az elsődleges adatbázist.</span><span class="sxs-lookup"><span data-stu-id="30d78-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="30d78-138">-SecondaryComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="30d78-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="30d78-139">A másodlagos Azure Sql-adatbázis számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="30d78-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="30d78-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="30d78-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="30d78-141">Annak a rugalmas készletnek a neve, amelybe a másodlagos adatbázist be kell tenni.</span><span class="sxs-lookup"><span data-stu-id="30d78-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="30d78-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="30d78-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="30d78-143">Megadja a másodlagos adatbázishoz hozzárendelni szükséges szolgáltatási célként megadott célként megadott nevet.</span><span class="sxs-lookup"><span data-stu-id="30d78-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="30d78-144">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="30d78-144">-SecondaryType</span></span>
<span data-ttu-id="30d78-145">Az adatbázis másodlagos típusa, ha az másodlagos.</span><span class="sxs-lookup"><span data-stu-id="30d78-145">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="30d78-146">Érvényes értékek: Földrajzi név és Név.</span><span class="sxs-lookup"><span data-stu-id="30d78-146">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d78-147">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="30d78-147">-SecondaryVCore</span></span>
<span data-ttu-id="30d78-148">A másodlagos Azure Sql-adatbázis Vcore-számai.</span><span class="sxs-lookup"><span data-stu-id="30d78-148">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="30d78-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="30d78-149">-ServerName</span></span>
<span data-ttu-id="30d78-150">Az elsődleges SQL-adatbázis SQL Server-kiszolgálójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30d78-150">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="30d78-151">-Címkék</span><span class="sxs-lookup"><span data-stu-id="30d78-151">-Tags</span></span>
<span data-ttu-id="30d78-152">Az SQL-adatbázis replikációs hivatkozásához társítható kulcsérték-párokat adja meg kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="30d78-152">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="30d78-153">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="30d78-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="30d78-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30d78-154">-Confirm</span></span>
<span data-ttu-id="30d78-155">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="30d78-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30d78-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30d78-156">-WhatIf</span></span>
<span data-ttu-id="30d78-157">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="30d78-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30d78-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30d78-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30d78-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d78-159">CommonParameters</span></span>
<span data-ttu-id="30d78-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30d78-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d78-161">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30d78-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d78-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30d78-162">INPUTS</span></span>

### <span data-ttu-id="30d78-163">System.String</span><span class="sxs-lookup"><span data-stu-id="30d78-163">System.String</span></span>

## <span data-ttu-id="30d78-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30d78-164">OUTPUTS</span></span>

### <span data-ttu-id="30d78-165">Microsoft.Azure.Commands.Sql.Replikáció.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="30d78-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="30d78-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="30d78-166">NOTES</span></span>

## <span data-ttu-id="30d78-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30d78-167">RELATED LINKS</span></span>

[<span data-ttu-id="30d78-168">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="30d78-168">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="30d78-169">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="30d78-169">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="30d78-170">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="30d78-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
