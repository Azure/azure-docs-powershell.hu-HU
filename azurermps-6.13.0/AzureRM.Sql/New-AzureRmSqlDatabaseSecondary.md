---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: d2af2095198cf0a1102e3422716013f2f2e02fc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494884"
---
# <span data-ttu-id="5a5a8-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5a5a8-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="5a5a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="5a5a8-103">Egy meglévő adatbázis másodlagos adatbázisát hozza létre, és elindítja az adatreplikálást.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a5a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a5a8-104">SYNTAX</span></span>

### <span data-ttu-id="5a5a8-105">DtuBasedDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a5a8-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a5a8-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="5a5a8-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a5a8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a5a8-107">DESCRIPTION</span></span>
<span data-ttu-id="5a5a8-108">A **New-AzureRMSqlDatabaseSecondary** parancsmag lecseréli az Start-AzureSqlDatabaseCopy parancsmagot az adatbázis földrajzi replikálásának beállításához.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-108">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="5a5a8-109">Az elsődlegestől a másodlagos adatbázishoz tartozó geo-replikációs hivatkozás objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="5a5a8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5a5a8-110">EXAMPLES</span></span>

### <span data-ttu-id="5a5a8-111">1: aktív Geo-Replication létrehozása</span><span class="sxs-lookup"><span data-stu-id="5a5a8-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="5a5a8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a5a8-112">PARAMETERS</span></span>

### <span data-ttu-id="5a5a8-113">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="5a5a8-113">-AllowConnections</span></span>
<span data-ttu-id="5a5a8-114">A másodlagos Azure SQL-adatbázis olvasási szándékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="5a5a8-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5a5a8-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5a5a8-116">nem</span><span class="sxs-lookup"><span data-stu-id="5a5a8-116">No</span></span>
- <span data-ttu-id="5a5a8-117">Minden</span><span class="sxs-lookup"><span data-stu-id="5a5a8-117">All</span></span>

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

### <span data-ttu-id="5a5a8-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a5a8-118">-AsJob</span></span>
<span data-ttu-id="5a5a8-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5a5a8-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a5a8-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a5a8-120">-DatabaseName</span></span>
<span data-ttu-id="5a5a8-121">Annak az adatbázisnak a nevét adja meg, amely az elsődlegesként működik.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-121">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="5a5a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a5a8-122">-DefaultProfile</span></span>
<span data-ttu-id="5a5a8-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5a5a8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a5a8-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5a5a8-124">-LicenseType</span></span>
<span data-ttu-id="5a5a8-125">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="5a5a8-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a5a8-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="5a5a8-127">Annak az Azure erőforrás-csoportnak a neve, amelyhez a parancsmag a másodlagos adatbázist rendeli.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="5a5a8-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="5a5a8-128">-PartnerServerName</span></span>
<span data-ttu-id="5a5a8-129">Annak az Azure SQL adatbázis-kiszolgálónak a nevét adja meg, amely másodlagosként működik.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="5a5a8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a5a8-130">-ResourceGroupName</span></span>
<span data-ttu-id="5a5a8-131">Annak az Azure erőforrás-csoportnak a neve, amelyhez a parancsmag az elsődleges adatbázist rendeli.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="5a5a8-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5a5a8-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="5a5a8-133">A másodlagos Azure SQL-adatbázis számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-133">The compute generation of teh Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="5a5a8-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5a5a8-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="5a5a8-135">Annak a rugalmas készletnek a nevét adja meg, amelybe a másodlagos adatbázist el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="5a5a8-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="5a5a8-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="5a5a8-137">Annak a szolgáltatási célnak a nevét adja meg, amelyet a másodlagos adatbázishoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="5a5a8-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="5a5a8-138">-SecondaryVCore</span></span>
<span data-ttu-id="5a5a8-139">Az Azure SQL-adatbázis másodlagos vcore száma.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="5a5a8-140">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5a5a8-140">-ServerName</span></span>
<span data-ttu-id="5a5a8-141">Az elsődleges SQL-adatbázis SQL-kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="5a5a8-142">-Címkék</span><span class="sxs-lookup"><span data-stu-id="5a5a8-142">-Tags</span></span>
<span data-ttu-id="5a5a8-143">Az SQL-adatbázis replikációs hivatkozásával társítani kívánt kivonatoló táblázat kulcs-érték párokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="5a5a8-144">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="5a5a8-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5a5a8-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5a5a8-145">-Confirm</span></span>
<span data-ttu-id="5a5a8-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a5a8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a5a8-147">-WhatIf</span></span>
<span data-ttu-id="5a5a8-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a5a8-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a5a8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a5a8-150">CommonParameters</span></span>
<span data-ttu-id="5a5a8-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a5a8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a5a8-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a5a8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a5a8-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a5a8-153">INPUTS</span></span>

### <span data-ttu-id="5a5a8-154">System. String</span><span class="sxs-lookup"><span data-stu-id="5a5a8-154">System.String</span></span>

## <span data-ttu-id="5a5a8-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a5a8-155">OUTPUTS</span></span>

### <span data-ttu-id="5a5a8-156">Microsoft. Azure. Command. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="5a5a8-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="5a5a8-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a5a8-157">NOTES</span></span>

## <span data-ttu-id="5a5a8-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a5a8-158">RELATED LINKS</span></span>

[<span data-ttu-id="5a5a8-159">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5a5a8-159">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="5a5a8-160">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5a5a8-160">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="5a5a8-161">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="5a5a8-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
