---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
ms.openlocfilehash: aa2ba844e364d1c95274573a6b1b38e4550c70f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668906"
---
# <span data-ttu-id="b8b8e-101">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b8b8e-101">New-AzSqlDatabaseCopy</span></span>

## <span data-ttu-id="b8b8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b8e-103">Egy SQL-adatbázis másolatát hozza létre, amely az aktuális időpontban a pillanatképet használja.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

## <span data-ttu-id="b8b8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8b8e-104">SYNTAX</span></span>

### <span data-ttu-id="b8b8e-105">DtuBasedDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8b8e-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>] -CopyDatabaseName <String>
 [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8b8e-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="b8b8e-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8b8e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8b8e-107">DESCRIPTION</span></span>
<span data-ttu-id="b8b8e-108">A **New-AzSqlDatabaseCopy** parancsmag egy olyan Azure SQL-adatbázis másolatát hozza létre, amely az aktuális időpontban az adatok pillanatképét használja.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-108">The **New-AzSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="b8b8e-109">A Start-AzSqlDatabaseCopy parancsmag helyett használja az egyszer használatos adatbázis-másolatot.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-109">Use this cmdlet instead of the Start-AzSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="b8b8e-110">Ez a parancsmag a másolat **adatbázis** -objektumát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="b8b8e-111">Megjegyzés: az adatbázis geo-replikációját az New-AzSqlDatabaseSecondary parancsmag használatával állíthatja be.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-111">Note: Use the New-AzSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="b8b8e-112">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b8b8e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b8b8e-113">EXAMPLES</span></span>

## <span data-ttu-id="b8b8e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8b8e-114">PARAMETERS</span></span>

### <span data-ttu-id="b8b8e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8b8e-115">-AsJob</span></span>
<span data-ttu-id="b8b8e-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b8b8e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8b8e-117">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="b8b8e-117">-ComputeGeneration</span></span>
<span data-ttu-id="b8b8e-118">A számítási generáció az új példányhoz társítva.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-118">The compute generation to assign to the new copy.</span></span>

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

### <span data-ttu-id="b8b8e-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8b8e-119">-CopyDatabaseName</span></span>
<span data-ttu-id="b8b8e-120">Az SQL-adatbázis másolatának neve.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-120">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="b8b8e-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8b8e-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="b8b8e-122">Annak az Azure erőforrás-csoportnak a nevét adja meg, amelybe a másolatot hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="b8b8e-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="b8b8e-123">-CopyServerName</span></span>
<span data-ttu-id="b8b8e-124">Annak az SQL-kiszolgálónak a nevét adja meg, amely a másolatot tárolja.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="b8b8e-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8b8e-125">-DatabaseName</span></span>
<span data-ttu-id="b8b8e-126">A másolandó SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-126">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="b8b8e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b8e-127">-DefaultProfile</span></span>
<span data-ttu-id="b8b8e-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b8b8e-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8b8e-129">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b8b8e-129">-ElasticPoolName</span></span>
<span data-ttu-id="b8b8e-130">Annak a rugalmas készletnek a nevét adja meg, amelybe a másolatot hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="b8b8e-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b8b8e-131">-LicenseType</span></span>
<span data-ttu-id="b8b8e-132">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-132">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="b8b8e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8b8e-133">-ResourceGroupName</span></span>
<span data-ttu-id="b8b8e-134">A másolandó adatbázist tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="b8b8e-135">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b8b8e-135">-ServerName</span></span>
<span data-ttu-id="b8b8e-136">Annak az SQL-kiszolgálónak a neve, amely a másolni kívánt adatbázist tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="b8b8e-137">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b8b8e-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="b8b8e-138">Annak a szolgáltatásnak a nevét adja meg, amelyet a másolathoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-138">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="b8b8e-139">-Címkék</span><span class="sxs-lookup"><span data-stu-id="b8b8e-139">-Tags</span></span>
<span data-ttu-id="b8b8e-140">A kulcs-érték párokat az Azure SQL adatbázis-példánnyal társítani kívánt kivonatoló táblázat formájában adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="b8b8e-141">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="b8b8e-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b8b8e-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="b8b8e-142">-VCore</span></span>
<span data-ttu-id="b8b8e-143">Az Azure SQL-adatbázis példányának vcore száma.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

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

### <span data-ttu-id="b8b8e-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8b8e-144">-Confirm</span></span>
<span data-ttu-id="b8b8e-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8b8e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8b8e-146">-WhatIf</span></span>
<span data-ttu-id="b8b8e-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8b8e-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8b8e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b8e-149">CommonParameters</span></span>
<span data-ttu-id="b8b8e-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8b8e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b8e-151">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b8b8e-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b8e-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8b8e-152">INPUTS</span></span>

### <span data-ttu-id="b8b8e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="b8b8e-153">System.String</span></span>

## <span data-ttu-id="b8b8e-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8b8e-154">OUTPUTS</span></span>

### <span data-ttu-id="b8b8e-155">Microsoft. Azure. Command. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="b8b8e-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="b8b8e-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8b8e-156">NOTES</span></span>

## <span data-ttu-id="b8b8e-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8b8e-157">RELATED LINKS</span></span>

[<span data-ttu-id="b8b8e-158">Új – AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b8b8e-158">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="b8b8e-159">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b8b8e-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)