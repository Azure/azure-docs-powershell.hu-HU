---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: a962ca86c3d65cd11da4169626ed932bb78653b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680467"
---
# <span data-ttu-id="7287b-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7287b-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="7287b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7287b-102">SYNOPSIS</span></span>
<span data-ttu-id="7287b-103">Egy SQL-adatbázis másolatát hozza létre, amely az aktuális időpontban a pillanatképet használja.</span><span class="sxs-lookup"><span data-stu-id="7287b-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7287b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7287b-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7287b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7287b-105">DESCRIPTION</span></span>
<span data-ttu-id="7287b-106">A **New-AzureRmSqlDatabaseCopy** parancsmag egy olyan Azure SQL-adatbázis másolatát hozza létre, amely az aktuális időpontban az adatok pillanatképét használja.</span><span class="sxs-lookup"><span data-stu-id="7287b-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="7287b-107">A Start-AzureSqlDatabaseCopy parancsmag helyett használja az egyszer használatos adatbázis-másolatot.</span><span class="sxs-lookup"><span data-stu-id="7287b-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="7287b-108">Ez a parancsmag a másolat **adatbázis** -objektumát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="7287b-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="7287b-109">Megjegyzés: az adatbázis geo-replikációját az New-AzureRmSqlDatabaseSecondary parancsmag használatával állíthatja be.</span><span class="sxs-lookup"><span data-stu-id="7287b-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="7287b-110">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="7287b-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7287b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7287b-111">EXAMPLES</span></span>

## <span data-ttu-id="7287b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7287b-112">PARAMETERS</span></span>

### <span data-ttu-id="7287b-113">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7287b-113">-CopyDatabaseName</span></span>
<span data-ttu-id="7287b-114">Az SQL-adatbázis másolatának neve.</span><span class="sxs-lookup"><span data-stu-id="7287b-114">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="7287b-115">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7287b-115">-CopyResourceGroupName</span></span>
<span data-ttu-id="7287b-116">Annak az Azure erőforrás-csoportnak a nevét adja meg, amelybe a másolatot hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="7287b-116">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="7287b-117">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="7287b-117">-CopyServerName</span></span>
<span data-ttu-id="7287b-118">Annak az SQL-kiszolgálónak a nevét adja meg, amely a másolatot tárolja.</span><span class="sxs-lookup"><span data-stu-id="7287b-118">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="7287b-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7287b-119">-DatabaseName</span></span>
<span data-ttu-id="7287b-120">A másolandó SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7287b-120">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="7287b-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7287b-121">-ElasticPoolName</span></span>
<span data-ttu-id="7287b-122">Annak a rugalmas készletnek a nevét adja meg, amelybe a másolatot hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="7287b-122">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="7287b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7287b-123">-ResourceGroupName</span></span>
<span data-ttu-id="7287b-124">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag a másolt adatbázist rendeli.</span><span class="sxs-lookup"><span data-stu-id="7287b-124">Specifies the name of the  Resource Group to which this cmdlet assigns the copied database.</span></span>

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

### <span data-ttu-id="7287b-125">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7287b-125">-ServerName</span></span>
<span data-ttu-id="7287b-126">Annak az SQL-kiszolgálónak a neve, amely a másolni kívánt adatbázist tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7287b-126">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="7287b-127">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="7287b-127">-ServiceObjectiveName</span></span>
<span data-ttu-id="7287b-128">Annak a szolgáltatásnak a nevét adja meg, amelyet a másolathoz szeretne rendelni.</span><span class="sxs-lookup"><span data-stu-id="7287b-128">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="7287b-129">-Címkék</span><span class="sxs-lookup"><span data-stu-id="7287b-129">-Tags</span></span>
<span data-ttu-id="7287b-130">A kulcs-érték párokat az Azure SQL adatbázis-példánnyal társítani kívánt kivonatoló táblázat formájában adja meg.</span><span class="sxs-lookup"><span data-stu-id="7287b-130">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="7287b-131">Példa:</span><span class="sxs-lookup"><span data-stu-id="7287b-131">For example:</span></span>

<span data-ttu-id="7287b-132">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="7287b-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7287b-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7287b-133">-Confirm</span></span>
<span data-ttu-id="7287b-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7287b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7287b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7287b-135">-WhatIf</span></span>
<span data-ttu-id="7287b-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7287b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7287b-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7287b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7287b-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7287b-138">-DefaultProfile</span></span>
<span data-ttu-id="7287b-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7287b-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7287b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7287b-140">CommonParameters</span></span>
<span data-ttu-id="7287b-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7287b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7287b-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7287b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7287b-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7287b-143">INPUTS</span></span>

## <span data-ttu-id="7287b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7287b-144">OUTPUTS</span></span>

### <span data-ttu-id="7287b-145">Microsoft. Azure. Command. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="7287b-145">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="7287b-146">Ez a parancsmag egy **adatbázis** -objektumot ad eredményül, amely a másolt adatbázist jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7287b-146">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="7287b-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7287b-147">NOTES</span></span>

## <span data-ttu-id="7287b-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7287b-148">RELATED LINKS</span></span>

[<span data-ttu-id="7287b-149">Új – AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7287b-149">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="7287b-150">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7287b-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
