---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: a8f147b4e2c8a1f4525585f8622b7195ed759022
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499339"
---
# <span data-ttu-id="efa5d-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="efa5d-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="efa5d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="efa5d-102">SYNOPSIS</span></span>
<span data-ttu-id="efa5d-103">Egy vagy több adatbázis eltávolítása egy Azure SQL-adatbázis feladatátvételi csoportjához.</span><span class="sxs-lookup"><span data-stu-id="efa5d-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efa5d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="efa5d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efa5d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="efa5d-105">DESCRIPTION</span></span>
<span data-ttu-id="efa5d-106">Egy vagy több adatbázis eltávolítása a megadott Azure SQL-adatbázis feladatátvételi csoportjához.</span><span class="sxs-lookup"><span data-stu-id="efa5d-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="efa5d-107">Az adatbázisok és a replikációs kapcsolatok érintetlen állapotban maradnak, de nem lesznek elérhetők a feladatátvétel csoport végpontjai között.</span><span class="sxs-lookup"><span data-stu-id="efa5d-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="efa5d-108">Ha olyan adatbázis-objektumokat szeretne beolvasni, amelyekkel feltöltheti az "-Database" paramétert, használja (például) az Get-AzureRmSqlDatabase parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="efa5d-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>
<span data-ttu-id="efa5d-109">A feladatátvevő csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="efa5d-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="efa5d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="efa5d-110">EXAMPLES</span></span>

### <span data-ttu-id="efa5d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="efa5d-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="efa5d-112">Ez a parancs eltávolítja az egyik adatbázist a feladatátvételi csoportból.</span><span class="sxs-lookup"><span data-stu-id="efa5d-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="efa5d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="efa5d-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="efa5d-114">Ez a parancs eltávolítja a feladatátvételi csoport összes adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="efa5d-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="efa5d-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="efa5d-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="efa5d-116">Ez a parancs eltávolítja az összes adatbázist egy rugalmas készletből egy feladatátvételi csoportból.</span><span class="sxs-lookup"><span data-stu-id="efa5d-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="efa5d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="efa5d-117">PARAMETERS</span></span>

### <span data-ttu-id="efa5d-118">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="efa5d-118">-Database</span></span>
<span data-ttu-id="efa5d-119">A feladatátvételi csoport elsődleges kiszolgálóin egy vagy több Azure SQL-adatbázis törlődik a feladatátvételi csoportból.</span><span class="sxs-lookup"><span data-stu-id="efa5d-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efa5d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa5d-120">-DefaultProfile</span></span>
<span data-ttu-id="efa5d-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="efa5d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efa5d-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="efa5d-122">-FailoverGroupName</span></span>
<span data-ttu-id="efa5d-123">Az Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="efa5d-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="efa5d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="efa5d-124">-Force</span></span>
<span data-ttu-id="efa5d-125">A művelet elvégzésére vonatkozó megerősítési üzenet kihagyása.</span><span class="sxs-lookup"><span data-stu-id="efa5d-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="efa5d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa5d-126">-ResourceGroupName</span></span>
<span data-ttu-id="efa5d-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="efa5d-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="efa5d-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="efa5d-128">-ServerName</span></span>
<span data-ttu-id="efa5d-129">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="efa5d-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="efa5d-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="efa5d-130">-Confirm</span></span>
<span data-ttu-id="efa5d-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="efa5d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efa5d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa5d-132">-WhatIf</span></span>
<span data-ttu-id="efa5d-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="efa5d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efa5d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efa5d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efa5d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa5d-135">CommonParameters</span></span>
<span data-ttu-id="efa5d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="efa5d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa5d-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efa5d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa5d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="efa5d-138">INPUTS</span></span>

### <span data-ttu-id="efa5d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="efa5d-139">System.String</span></span>

### <span data-ttu-id="efa5d-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. SQL. database. Model. AzureSqlDatabaseModel, Microsoft. Azure. Command. SQL, Version = 4.11.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="efa5d-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=4.11.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="efa5d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efa5d-141">OUTPUTS</span></span>

### <span data-ttu-id="efa5d-142">Microsoft. Azure. Command. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="efa5d-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="efa5d-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="efa5d-143">NOTES</span></span>

## <span data-ttu-id="efa5d-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efa5d-144">RELATED LINKS</span></span>

[<span data-ttu-id="efa5d-145">Új – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="efa5d-145">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="efa5d-146">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="efa5d-146">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="efa5d-147">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="efa5d-147">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="efa5d-148">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="efa5d-148">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="efa5d-149">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="efa5d-149">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="efa5d-150">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="efa5d-150">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="efa5d-151">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="efa5d-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
