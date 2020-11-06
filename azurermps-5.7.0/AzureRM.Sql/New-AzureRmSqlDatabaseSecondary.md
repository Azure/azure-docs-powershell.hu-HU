---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: b23128d2ef55e971f20569e251601b410b218ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492125"
---
# <span data-ttu-id="3ac1d-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3ac1d-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="3ac1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ac1d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac1d-103">Egy meglévő adatbázis másodlagos adatbázisát hozza létre, és elindítja az adatreplikálást.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ac1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ac1d-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ac1d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ac1d-105">DESCRIPTION</span></span>
<span data-ttu-id="3ac1d-106">A **New-AzureRMSqlDatabaseSecondary** parancsmag lecseréli az Start-AzureSqlDatabaseCopy parancsmagot az adatbázis földrajzi replikálásának beállításához.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="3ac1d-107">Az elsődlegestől a másodlagos adatbázishoz tartozó geo-replikációs hivatkozás objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="3ac1d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3ac1d-108">EXAMPLES</span></span>

### <span data-ttu-id="3ac1d-109">1: aktív Geo-Replication létrehozása</span><span class="sxs-lookup"><span data-stu-id="3ac1d-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="3ac1d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ac1d-110">PARAMETERS</span></span>

### <span data-ttu-id="3ac1d-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="3ac1d-111">-AllowConnections</span></span>
<span data-ttu-id="3ac1d-112">A másodlagos Azure SQL-adatbázis olvasási szándékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="3ac1d-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3ac1d-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ac1d-114">nem</span><span class="sxs-lookup"><span data-stu-id="3ac1d-114">No</span></span>
- <span data-ttu-id="3ac1d-115">Minden</span><span class="sxs-lookup"><span data-stu-id="3ac1d-115">All</span></span>

```yaml
Type: AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac1d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ac1d-116">-AsJob</span></span>
<span data-ttu-id="3ac1d-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3ac1d-117">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="3ac1d-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3ac1d-118">-DatabaseName</span></span>
<span data-ttu-id="3ac1d-119">Annak az adatbázisnak a nevét adja meg, amely az elsődlegesként működik.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-119">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac1d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac1d-120">-DefaultProfile</span></span>
<span data-ttu-id="3ac1d-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3ac1d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ac1d-122">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac1d-122">-PartnerResourceGroupName</span></span>
<span data-ttu-id="3ac1d-123">Annak az Azure erőforrás-csoportnak a neve, amelyhez a parancsmag a másodlagos adatbázist rendeli.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac1d-124">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="3ac1d-124">-PartnerServerName</span></span>
<span data-ttu-id="3ac1d-125">Annak az Azure SQL adatbázis-kiszolgálónak a nevét adja meg, amely másodlagosként működik.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-125">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac1d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac1d-126">-ResourceGroupName</span></span>
<span data-ttu-id="3ac1d-127">Annak az Azure erőforrás-csoportnak a neve, amelyhez a parancsmag az elsődleges adatbázist rendeli.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="3ac1d-128">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3ac1d-128">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="3ac1d-129">Annak a rugalmas készletnek a nevét adja meg, amelybe a másodlagos adatbázist el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-129">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="3ac1d-130">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="3ac1d-130">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="3ac1d-131">Annak a szolgáltatási célnak a nevét adja meg, amelyet a másodlagos adatbázishoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-131">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="3ac1d-132">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3ac1d-132">-ServerName</span></span>
<span data-ttu-id="3ac1d-133">Az elsődleges SQL-adatbázis SQL-kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-133">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="3ac1d-134">-Címkék</span><span class="sxs-lookup"><span data-stu-id="3ac1d-134">-Tags</span></span>
<span data-ttu-id="3ac1d-135">Az SQL-adatbázis replikációs hivatkozásával társítani kívánt kivonatoló táblázat kulcs-érték párokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-135">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="3ac1d-136">Példa:</span><span class="sxs-lookup"><span data-stu-id="3ac1d-136">For example:</span></span>

<span data-ttu-id="3ac1d-137">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3ac1d-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3ac1d-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ac1d-138">-Confirm</span></span>
<span data-ttu-id="3ac1d-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ac1d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ac1d-140">-WhatIf</span></span>
<span data-ttu-id="3ac1d-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ac1d-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ac1d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac1d-143">CommonParameters</span></span>
<span data-ttu-id="3ac1d-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ac1d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac1d-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ac1d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac1d-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ac1d-146">INPUTS</span></span>

### <span data-ttu-id="3ac1d-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="3ac1d-147">None</span></span>
<span data-ttu-id="3ac1d-148">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ac1d-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ac1d-149">OUTPUTS</span></span>

### <span data-ttu-id="3ac1d-150">Microsoft. Azure. Command. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="3ac1d-150">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="3ac1d-151">Ez a parancsmag **ReplicationLink** -objektumokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-151">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="3ac1d-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ac1d-152">NOTES</span></span>

## <span data-ttu-id="3ac1d-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ac1d-153">RELATED LINKS</span></span>

[<span data-ttu-id="3ac1d-154">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3ac1d-154">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="3ac1d-155">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3ac1d-155">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="3ac1d-156">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3ac1d-156">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
