---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 4a39cd97936ef72615e30072de1988304fc5ad09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668859"
---
# <span data-ttu-id="f2764-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f2764-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="f2764-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2764-102">SYNOPSIS</span></span>
<span data-ttu-id="f2764-103">Egy vagy több adatbázis eltávolítása egy Azure SQL-adatbázis feladatátvételi csoportjához.</span><span class="sxs-lookup"><span data-stu-id="f2764-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="f2764-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2764-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2764-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2764-105">DESCRIPTION</span></span>
<span data-ttu-id="f2764-106">Egy vagy több adatbázis eltávolítása a megadott Azure SQL-adatbázis feladatátvételi csoportjához.</span><span class="sxs-lookup"><span data-stu-id="f2764-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="f2764-107">Az adatbázisok és a replikációs kapcsolatok érintetlen állapotban maradnak, de nem lesznek elérhetők a feladatátvétel csoport végpontjai között.</span><span class="sxs-lookup"><span data-stu-id="f2764-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="f2764-108">Ha olyan adatbázis-objektumokat szeretne beolvasni, amelyekkel feltöltheti az "-Database" paramétert, használja (például) az Get-AzSqlDatabase parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f2764-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="f2764-109">A feladatátvevő csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="f2764-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="f2764-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f2764-110">EXAMPLES</span></span>

### <span data-ttu-id="f2764-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f2764-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="f2764-112">Ez a parancs eltávolítja az egyik adatbázist a feladatátvételi csoportból.</span><span class="sxs-lookup"><span data-stu-id="f2764-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="f2764-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f2764-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="f2764-114">Ez a parancs eltávolítja a feladatátvételi csoport összes adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="f2764-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="f2764-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="f2764-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="f2764-116">Ez a parancs eltávolítja az összes adatbázist egy rugalmas készletből egy feladatátvételi csoportból.</span><span class="sxs-lookup"><span data-stu-id="f2764-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="f2764-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2764-117">PARAMETERS</span></span>

### <span data-ttu-id="f2764-118">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="f2764-118">-Database</span></span>
<span data-ttu-id="f2764-119">A feladatátvételi csoport elsődleges kiszolgálóin egy vagy több Azure SQL-adatbázis törlődik a feladatátvételi csoportból.</span><span class="sxs-lookup"><span data-stu-id="f2764-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="f2764-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2764-120">-DefaultProfile</span></span>
<span data-ttu-id="f2764-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f2764-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2764-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="f2764-122">-FailoverGroupName</span></span>
<span data-ttu-id="f2764-123">Az Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2764-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="f2764-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f2764-124">-Force</span></span>
<span data-ttu-id="f2764-125">A művelet elvégzésére vonatkozó megerősítési üzenet kihagyása.</span><span class="sxs-lookup"><span data-stu-id="f2764-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="f2764-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2764-126">-ResourceGroupName</span></span>
<span data-ttu-id="f2764-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2764-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2764-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f2764-128">-ServerName</span></span>
<span data-ttu-id="f2764-129">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="f2764-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="f2764-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f2764-130">-Confirm</span></span>
<span data-ttu-id="f2764-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f2764-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2764-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2764-132">-WhatIf</span></span>
<span data-ttu-id="f2764-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f2764-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2764-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f2764-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2764-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2764-135">CommonParameters</span></span>
<span data-ttu-id="f2764-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2764-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2764-137">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f2764-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2764-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2764-138">INPUTS</span></span>

### <span data-ttu-id="f2764-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f2764-139">System.String</span></span>

### <span data-ttu-id="f2764-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. SQL. database. Model. AzureSqlDatabaseModel, Microsoft. Azure. PowerShell. parancsmag. SQL, Version = 1.3.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f2764-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f2764-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2764-141">OUTPUTS</span></span>

### <span data-ttu-id="f2764-142">Microsoft. Azure. Command. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f2764-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="f2764-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2764-143">NOTES</span></span>

## <span data-ttu-id="f2764-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2764-144">RELATED LINKS</span></span>

[<span data-ttu-id="f2764-145">Új – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f2764-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f2764-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f2764-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f2764-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f2764-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f2764-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f2764-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="f2764-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f2764-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f2764-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f2764-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f2764-151">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f2764-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
