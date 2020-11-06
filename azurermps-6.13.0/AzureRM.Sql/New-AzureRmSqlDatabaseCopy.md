---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 7019fc7345b4296d9c35f11c6acec5bf5a42d966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502868"
---
# <span data-ttu-id="6a55d-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6a55d-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="6a55d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a55d-102">SYNOPSIS</span></span>
<span data-ttu-id="6a55d-103">Egy SQL-adatbázis másolatát hozza létre, amely az aktuális időpontban a pillanatképet használja.</span><span class="sxs-lookup"><span data-stu-id="6a55d-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a55d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a55d-104">SYNTAX</span></span>

### <span data-ttu-id="6a55d-105">DtuBasedDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a55d-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a55d-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="6a55d-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a55d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a55d-107">DESCRIPTION</span></span>
<span data-ttu-id="6a55d-108">A **New-AzureRmSqlDatabaseCopy** parancsmag egy olyan Azure SQL-adatbázis másolatát hozza létre, amely az aktuális időpontban az adatok pillanatképét használja.</span><span class="sxs-lookup"><span data-stu-id="6a55d-108">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="6a55d-109">A Start-AzureSqlDatabaseCopy parancsmag helyett használja az egyszer használatos adatbázis-másolatot.</span><span class="sxs-lookup"><span data-stu-id="6a55d-109">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="6a55d-110">Ez a parancsmag a másolat **adatbázis** -objektumát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="6a55d-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="6a55d-111">Megjegyzés: az adatbázis geo-replikációját az New-AzureRmSqlDatabaseSecondary parancsmag használatával állíthatja be.</span><span class="sxs-lookup"><span data-stu-id="6a55d-111">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="6a55d-112">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="6a55d-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6a55d-113">Példák</span><span class="sxs-lookup"><span data-stu-id="6a55d-113">EXAMPLES</span></span>

## <span data-ttu-id="6a55d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a55d-114">PARAMETERS</span></span>

### <span data-ttu-id="6a55d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a55d-115">-AsJob</span></span>
<span data-ttu-id="6a55d-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6a55d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a55d-117">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="6a55d-117">-ComputeGeneration</span></span>
<span data-ttu-id="6a55d-118">A számítási generáció az új példányhoz társítva.</span><span class="sxs-lookup"><span data-stu-id="6a55d-118">The compute generation to assign to the new copy.</span></span>

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

### <span data-ttu-id="6a55d-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a55d-119">-CopyDatabaseName</span></span>
<span data-ttu-id="6a55d-120">Az SQL-adatbázis másolatának neve.</span><span class="sxs-lookup"><span data-stu-id="6a55d-120">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="6a55d-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a55d-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="6a55d-122">Annak az Azure erőforrás-csoportnak a nevét adja meg, amelybe a másolatot hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="6a55d-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="6a55d-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="6a55d-123">-CopyServerName</span></span>
<span data-ttu-id="6a55d-124">Annak az SQL-kiszolgálónak a nevét adja meg, amely a másolatot tárolja.</span><span class="sxs-lookup"><span data-stu-id="6a55d-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="6a55d-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a55d-125">-DatabaseName</span></span>
<span data-ttu-id="6a55d-126">A másolandó SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a55d-126">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="6a55d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a55d-127">-DefaultProfile</span></span>
<span data-ttu-id="6a55d-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6a55d-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a55d-129">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6a55d-129">-ElasticPoolName</span></span>
<span data-ttu-id="6a55d-130">Annak a rugalmas készletnek a nevét adja meg, amelybe a másolatot hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="6a55d-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="6a55d-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6a55d-131">-LicenseType</span></span>
<span data-ttu-id="6a55d-132">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="6a55d-132">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="6a55d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a55d-133">-ResourceGroupName</span></span>
<span data-ttu-id="6a55d-134">A másolandó adatbázist tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a55d-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="6a55d-135">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6a55d-135">-ServerName</span></span>
<span data-ttu-id="6a55d-136">Annak az SQL-kiszolgálónak a neve, amely a másolni kívánt adatbázist tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6a55d-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="6a55d-137">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="6a55d-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="6a55d-138">Annak a szolgáltatásnak a nevét adja meg, amelyet a másolathoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="6a55d-138">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="6a55d-139">-Címkék</span><span class="sxs-lookup"><span data-stu-id="6a55d-139">-Tags</span></span>
<span data-ttu-id="6a55d-140">A kulcs-érték párokat az Azure SQL adatbázis-példánnyal társítani kívánt kivonatoló táblázat formájában adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a55d-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="6a55d-141">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="6a55d-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6a55d-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="6a55d-142">-VCore</span></span>
<span data-ttu-id="6a55d-143">Az Azure SQL-adatbázis példányának vcore száma.</span><span class="sxs-lookup"><span data-stu-id="6a55d-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

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

### <span data-ttu-id="6a55d-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a55d-144">-Confirm</span></span>
<span data-ttu-id="6a55d-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a55d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a55d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a55d-146">-WhatIf</span></span>
<span data-ttu-id="6a55d-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a55d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a55d-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a55d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a55d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a55d-149">CommonParameters</span></span>
<span data-ttu-id="6a55d-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a55d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a55d-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a55d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a55d-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a55d-152">INPUTS</span></span>

### <span data-ttu-id="6a55d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="6a55d-153">System.String</span></span>

## <span data-ttu-id="6a55d-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a55d-154">OUTPUTS</span></span>

### <span data-ttu-id="6a55d-155">Microsoft. Azure. Command. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="6a55d-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="6a55d-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a55d-156">NOTES</span></span>

## <span data-ttu-id="6a55d-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a55d-157">RELATED LINKS</span></span>

[<span data-ttu-id="6a55d-158">Új – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6a55d-158">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="6a55d-159">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6a55d-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
