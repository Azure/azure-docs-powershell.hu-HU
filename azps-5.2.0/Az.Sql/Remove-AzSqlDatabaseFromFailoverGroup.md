---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 7fa7c09d5c6c992dfa3eab7a6f81b70e820a9ee4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343049"
---
# <span data-ttu-id="623d6-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="623d6-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="623d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="623d6-102">SYNOPSIS</span></span>
<span data-ttu-id="623d6-103">Eltávolít egy vagy több adatbázist egy Azure SQL-adatbázis feladatátvételi csoportjából.</span><span class="sxs-lookup"><span data-stu-id="623d6-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="623d6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="623d6-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="623d6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="623d6-105">DESCRIPTION</span></span>
<span data-ttu-id="623d6-106">Eltávolít egy vagy több adatbázist a megadott Azure SQL-adatbázis feladatátvételi csoportjából.</span><span class="sxs-lookup"><span data-stu-id="623d6-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="623d6-107">Az adatbázisok és a replikációs kapcsolatok érintetlenek maradnak, de a továbbiakban nem lesznek elérhetők a feladatátvételi csoport végpontjain keresztül.</span><span class="sxs-lookup"><span data-stu-id="623d6-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="623d6-108">Ha olyan adatbázis-objektumokat keres, amelyek az "-Database" paramétert kitöltik, használja (például) a Get-AzSqlDatabase parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="623d6-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="623d6-109">A feladatátvételi csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="623d6-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="623d6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="623d6-110">EXAMPLES</span></span>

### <span data-ttu-id="623d6-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="623d6-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="623d6-112">Ez a parancs úgy távolít el egy adatbázist a feladatátvételi csoportból, hogy bemászik.</span><span class="sxs-lookup"><span data-stu-id="623d6-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="623d6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="623d6-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="623d6-114">Ez a parancs eltávolítja az összes adatbázist a feladatátvételi csoportból.</span><span class="sxs-lookup"><span data-stu-id="623d6-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="623d6-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="623d6-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="623d6-116">Ez a parancs eltávolítja egy rugalmas készlet összes adatbázisát egy feladatátvételi csoportból.</span><span class="sxs-lookup"><span data-stu-id="623d6-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="623d6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="623d6-117">PARAMETERS</span></span>

### <span data-ttu-id="623d6-118">-Database</span><span class="sxs-lookup"><span data-stu-id="623d6-118">-Database</span></span>
<span data-ttu-id="623d6-119">A feladatátvételi csoport elsődleges kiszolgálójának egy vagy több Azure SQL-adatbázisát el kell távolítani a feladatátvételi csoportból.</span><span class="sxs-lookup"><span data-stu-id="623d6-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="623d6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623d6-120">-DefaultProfile</span></span>
<span data-ttu-id="623d6-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="623d6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="623d6-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="623d6-122">-FailoverGroupName</span></span>
<span data-ttu-id="623d6-123">Az Azure SQL-adatbázis feladatátvételi csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="623d6-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="623d6-124">-Force</span><span class="sxs-lookup"><span data-stu-id="623d6-124">-Force</span></span>
<span data-ttu-id="623d6-125">Hagyja ki a művelet végrehajtásához szükséges megerősítő üzenetet.</span><span class="sxs-lookup"><span data-stu-id="623d6-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="623d6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="623d6-126">-ResourceGroupName</span></span>
<span data-ttu-id="623d6-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="623d6-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="623d6-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="623d6-128">-ServerName</span></span>
<span data-ttu-id="623d6-129">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="623d6-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="623d6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="623d6-130">-Confirm</span></span>
<span data-ttu-id="623d6-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="623d6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="623d6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="623d6-132">-WhatIf</span></span>
<span data-ttu-id="623d6-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="623d6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="623d6-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="623d6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="623d6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623d6-135">CommonParameters</span></span>
<span data-ttu-id="623d6-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="623d6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623d6-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="623d6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623d6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="623d6-138">INPUTS</span></span>

### <span data-ttu-id="623d6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="623d6-139">System.String</span></span>

### <span data-ttu-id="623d6-140">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="623d6-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="623d6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="623d6-141">OUTPUTS</span></span>

### <span data-ttu-id="623d6-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="623d6-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="623d6-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="623d6-143">NOTES</span></span>

## <span data-ttu-id="623d6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="623d6-144">RELATED LINKS</span></span>

[<span data-ttu-id="623d6-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="623d6-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="623d6-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="623d6-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="623d6-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="623d6-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="623d6-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="623d6-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="623d6-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="623d6-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="623d6-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="623d6-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="623d6-151">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="623d6-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
