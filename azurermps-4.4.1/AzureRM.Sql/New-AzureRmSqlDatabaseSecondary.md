---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 226910b81da287c04adb05574b77713e97c6a045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672190"
---
# <span data-ttu-id="d983b-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d983b-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="d983b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d983b-102">SYNOPSIS</span></span>
<span data-ttu-id="d983b-103">Egy meglévő adatbázis másodlagos adatbázisát hozza létre, és elindítja az adatreplikálást.</span><span class="sxs-lookup"><span data-stu-id="d983b-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d983b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d983b-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d983b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d983b-105">DESCRIPTION</span></span>
<span data-ttu-id="d983b-106">A **New-AzureRMSqlDatabaseSecondary** parancsmag lecseréli az Start-AzureSqlDatabaseCopy parancsmagot az adatbázis földrajzi replikálásának beállításához.</span><span class="sxs-lookup"><span data-stu-id="d983b-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="d983b-107">Az elsődlegestől a másodlagos adatbázishoz tartozó geo-replikációs hivatkozás objektumot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d983b-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="d983b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d983b-108">EXAMPLES</span></span>

### <span data-ttu-id="d983b-109">1: aktív Geo-Replication létrehozása</span><span class="sxs-lookup"><span data-stu-id="d983b-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="d983b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d983b-110">PARAMETERS</span></span>

### <span data-ttu-id="d983b-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="d983b-111">-AllowConnections</span></span>
<span data-ttu-id="d983b-112">A másodlagos Azure SQL-adatbázis olvasási szándékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d983b-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="d983b-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d983b-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d983b-114">nem</span><span class="sxs-lookup"><span data-stu-id="d983b-114">No</span></span>
- <span data-ttu-id="d983b-115">Minden</span><span class="sxs-lookup"><span data-stu-id="d983b-115">All</span></span>

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

### <span data-ttu-id="d983b-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d983b-116">-DatabaseName</span></span>
<span data-ttu-id="d983b-117">Annak az adatbázisnak a nevét adja meg, amely az elsődlegesként működik.</span><span class="sxs-lookup"><span data-stu-id="d983b-117">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="d983b-118">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d983b-118">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d983b-119">Annak az Azure erőforrás-csoportnak a neve, amelyhez a parancsmag a másodlagos adatbázist rendeli.</span><span class="sxs-lookup"><span data-stu-id="d983b-119">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="d983b-120">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="d983b-120">-PartnerServerName</span></span>
<span data-ttu-id="d983b-121">Annak az Azure SQL adatbázis-kiszolgálónak a nevét adja meg, amely másodlagosként működik.</span><span class="sxs-lookup"><span data-stu-id="d983b-121">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="d983b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d983b-122">-ResourceGroupName</span></span>
<span data-ttu-id="d983b-123">Annak az Azure erőforrás-csoportnak a neve, amelyhez a parancsmag az elsődleges adatbázist rendeli.</span><span class="sxs-lookup"><span data-stu-id="d983b-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="d983b-124">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d983b-124">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="d983b-125">Annak a rugalmas készletnek a nevét adja meg, amelybe a másodlagos adatbázist el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="d983b-125">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="d983b-126">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="d983b-126">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="d983b-127">Annak a szolgáltatási célnak a nevét adja meg, amelyet a másodlagos adatbázishoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="d983b-127">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="d983b-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d983b-128">-ServerName</span></span>
<span data-ttu-id="d983b-129">Az elsődleges SQL-adatbázis SQL-kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d983b-129">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="d983b-130">-Címkék</span><span class="sxs-lookup"><span data-stu-id="d983b-130">-Tags</span></span>
<span data-ttu-id="d983b-131">Az SQL-adatbázis replikációs hivatkozásával társítani kívánt kivonatoló táblázat kulcs-érték párokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d983b-131">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="d983b-132">Példa:</span><span class="sxs-lookup"><span data-stu-id="d983b-132">For example:</span></span>

<span data-ttu-id="d983b-133">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="d983b-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d983b-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d983b-134">-Confirm</span></span>
<span data-ttu-id="d983b-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d983b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d983b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d983b-136">-WhatIf</span></span>
<span data-ttu-id="d983b-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d983b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d983b-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d983b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d983b-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d983b-139">-DefaultProfile</span></span>
<span data-ttu-id="d983b-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d983b-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d983b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d983b-141">CommonParameters</span></span>
<span data-ttu-id="d983b-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d983b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d983b-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d983b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d983b-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d983b-144">INPUTS</span></span>

## <span data-ttu-id="d983b-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d983b-145">OUTPUTS</span></span>

### <span data-ttu-id="d983b-146">Microsoft. Azure. Command. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d983b-146">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="d983b-147">Ez a parancsmag **ReplicationLink** -objektumokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d983b-147">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="d983b-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d983b-148">NOTES</span></span>

## <span data-ttu-id="d983b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d983b-149">RELATED LINKS</span></span>

[<span data-ttu-id="d983b-150">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d983b-150">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="d983b-151">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d983b-151">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="d983b-152">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d983b-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
