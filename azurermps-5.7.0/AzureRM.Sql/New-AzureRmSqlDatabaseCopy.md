---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 4e9d33691cfd09681bb115c89d0eaf351ef14f13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492127"
---
# <span data-ttu-id="bf545-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="bf545-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="bf545-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf545-102">SYNOPSIS</span></span>
<span data-ttu-id="bf545-103">Egy SQL-adatbázis másolatát hozza létre, amely az aktuális időpontban a pillanatképet használja.</span><span class="sxs-lookup"><span data-stu-id="bf545-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf545-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf545-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf545-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf545-105">DESCRIPTION</span></span>
<span data-ttu-id="bf545-106">A **New-AzureRmSqlDatabaseCopy** parancsmag egy olyan Azure SQL-adatbázis másolatát hozza létre, amely az aktuális időpontban az adatok pillanatképét használja.</span><span class="sxs-lookup"><span data-stu-id="bf545-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="bf545-107">A Start-AzureSqlDatabaseCopy parancsmag helyett használja az egyszer használatos adatbázis-másolatot.</span><span class="sxs-lookup"><span data-stu-id="bf545-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="bf545-108">Ez a parancsmag a másolat **adatbázis** -objektumát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="bf545-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="bf545-109">Megjegyzés: az adatbázis geo-replikációját az New-AzureRmSqlDatabaseSecondary parancsmag használatával állíthatja be.</span><span class="sxs-lookup"><span data-stu-id="bf545-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="bf545-110">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="bf545-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="bf545-111">Példák</span><span class="sxs-lookup"><span data-stu-id="bf545-111">EXAMPLES</span></span>

## <span data-ttu-id="bf545-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf545-112">PARAMETERS</span></span>

### <span data-ttu-id="bf545-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf545-113">-AsJob</span></span>
<span data-ttu-id="bf545-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bf545-114">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="bf545-115">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="bf545-115">-CopyDatabaseName</span></span>
<span data-ttu-id="bf545-116">Az SQL-adatbázis másolatának neve.</span><span class="sxs-lookup"><span data-stu-id="bf545-116">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="bf545-117">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf545-117">-CopyResourceGroupName</span></span>
<span data-ttu-id="bf545-118">Annak az Azure erőforrás-csoportnak a nevét adja meg, amelybe a másolatot hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="bf545-118">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="bf545-119">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="bf545-119">-CopyServerName</span></span>
<span data-ttu-id="bf545-120">Annak az SQL-kiszolgálónak a nevét adja meg, amely a másolatot tárolja.</span><span class="sxs-lookup"><span data-stu-id="bf545-120">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="bf545-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bf545-121">-DatabaseName</span></span>
<span data-ttu-id="bf545-122">A másolandó SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf545-122">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="bf545-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf545-123">-DefaultProfile</span></span>
<span data-ttu-id="bf545-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bf545-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf545-125">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="bf545-125">-ElasticPoolName</span></span>
<span data-ttu-id="bf545-126">Annak a rugalmas készletnek a nevét adja meg, amelybe a másolatot hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="bf545-126">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="bf545-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf545-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf545-128">A másolandó adatbázist tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf545-128">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="bf545-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="bf545-129">-ServerName</span></span>
<span data-ttu-id="bf545-130">Annak az SQL-kiszolgálónak a neve, amely a másolni kívánt adatbázist tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bf545-130">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="bf545-131">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="bf545-131">-ServiceObjectiveName</span></span>
<span data-ttu-id="bf545-132">Annak a szolgáltatásnak a nevét adja meg, amelyet a másolathoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="bf545-132">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="bf545-133">-Címkék</span><span class="sxs-lookup"><span data-stu-id="bf545-133">-Tags</span></span>
<span data-ttu-id="bf545-134">A kulcs-érték párokat az Azure SQL adatbázis-példánnyal társítani kívánt kivonatoló táblázat formájában adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf545-134">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="bf545-135">Példa:</span><span class="sxs-lookup"><span data-stu-id="bf545-135">For example:</span></span>

<span data-ttu-id="bf545-136">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="bf545-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bf545-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf545-137">-Confirm</span></span>
<span data-ttu-id="bf545-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf545-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf545-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf545-139">-WhatIf</span></span>
<span data-ttu-id="bf545-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf545-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf545-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf545-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf545-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf545-142">CommonParameters</span></span>
<span data-ttu-id="bf545-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf545-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf545-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf545-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf545-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf545-145">INPUTS</span></span>

### <span data-ttu-id="bf545-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="bf545-146">None</span></span>
<span data-ttu-id="bf545-147">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="bf545-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf545-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf545-148">OUTPUTS</span></span>

### <span data-ttu-id="bf545-149">Microsoft. Azure. Command. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="bf545-149">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="bf545-150">Ez a parancsmag egy **adatbázis** -objektumot ad eredményül, amely a másolt adatbázist jelképezi.</span><span class="sxs-lookup"><span data-stu-id="bf545-150">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="bf545-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf545-151">NOTES</span></span>

## <span data-ttu-id="bf545-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf545-152">RELATED LINKS</span></span>

[<span data-ttu-id="bf545-153">Új – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="bf545-153">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="bf545-154">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bf545-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
