---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 7fa7c09d5c6c992dfa3eab7a6f81b70e820a9ee4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163290"
---
# <span data-ttu-id="ea0c4-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ea0c4-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="ea0c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0c4-103">Eltávolít egy vagy több adatbázist egy Azure SQL-adatbázis feladatátvételi csoportjából.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="ea0c4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea0c4-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea0c4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea0c4-105">DESCRIPTION</span></span>
<span data-ttu-id="ea0c4-106">Eltávolít egy vagy több adatbázist a megadott Azure SQL-adatbázis feladatátvételi csoportjából.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="ea0c4-107">Az adatbázisok és a replikációs kapcsolatok érintetlenek maradnak, de a továbbiakban nem lesznek elérhetők a feladatátvételi csoport végpontjain keresztül.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="ea0c4-108">Ha olyan adatbázis-objektumokat keres, amelyek az "-Database" paramétert kitöltik, használja (például) a Get-AzSqlDatabase parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="ea0c4-109">A feladatátvételi csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="ea0c4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea0c4-110">EXAMPLES</span></span>

### <span data-ttu-id="ea0c4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ea0c4-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="ea0c4-112">Ez a parancs úgy távolít el egy adatbázist a feladatátvételi csoportból, hogy bemászik.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="ea0c4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ea0c4-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="ea0c4-114">Ez a parancs eltávolítja az összes adatbázist a feladatátvételi csoportból.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="ea0c4-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="ea0c4-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="ea0c4-116">Ez a parancs eltávolítja egy rugalmas készlet összes adatbázisát egy feladatátvételi csoportból.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="ea0c4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea0c4-117">PARAMETERS</span></span>

### <span data-ttu-id="ea0c4-118">-Database</span><span class="sxs-lookup"><span data-stu-id="ea0c4-118">-Database</span></span>
<span data-ttu-id="ea0c4-119">A feladatátvételi csoport elsődleges kiszolgálójának egy vagy több Azure SQL-adatbázisát el kell távolítani a feladatátvételi csoportból.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="ea0c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0c4-120">-DefaultProfile</span></span>
<span data-ttu-id="ea0c4-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ea0c4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea0c4-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="ea0c4-122">-FailoverGroupName</span></span>
<span data-ttu-id="ea0c4-123">Az Azure SQL-adatbázis feladatátvételi csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="ea0c4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ea0c4-124">-Force</span></span>
<span data-ttu-id="ea0c4-125">A művelet végrehajtásához hagyja ki a megerősítő üzenetet.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="ea0c4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea0c4-126">-ResourceGroupName</span></span>
<span data-ttu-id="ea0c4-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="ea0c4-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ea0c4-128">-ServerName</span></span>
<span data-ttu-id="ea0c4-129">A feladatátvételi csoport elsődleges Azure SQL Database Server-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="ea0c4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea0c4-130">-Confirm</span></span>
<span data-ttu-id="ea0c4-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea0c4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea0c4-132">-WhatIf</span></span>
<span data-ttu-id="ea0c4-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea0c4-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea0c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0c4-135">CommonParameters</span></span>
<span data-ttu-id="ea0c4-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0c4-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea0c4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0c4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea0c4-138">INPUTS</span></span>

### <span data-ttu-id="ea0c4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ea0c4-139">System.String</span></span>

### <span data-ttu-id="ea0c4-140">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="ea0c4-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ea0c4-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea0c4-141">OUTPUTS</span></span>

### <span data-ttu-id="ea0c4-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ea0c4-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="ea0c4-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea0c4-143">NOTES</span></span>

## <span data-ttu-id="ea0c4-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea0c4-144">RELATED LINKS</span></span>

[<span data-ttu-id="ea0c4-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ea0c4-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ea0c4-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ea0c4-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ea0c4-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ea0c4-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ea0c4-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ea0c4-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="ea0c4-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ea0c4-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ea0c4-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ea0c4-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ea0c4-151">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="ea0c4-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
