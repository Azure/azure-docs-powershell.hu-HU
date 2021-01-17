---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 7577809134987bd1a0092e28170d5bf25ccac04e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375604"
---
# <span data-ttu-id="4d46b-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4d46b-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="4d46b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d46b-102">SYNOPSIS</span></span>
<span data-ttu-id="4d46b-103">Hozzáad egy vagy több adatbázist egy Azure SQL-adatbázis feladatátvételi csoportjához.</span><span class="sxs-lookup"><span data-stu-id="4d46b-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="4d46b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d46b-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d46b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d46b-105">DESCRIPTION</span></span>
<span data-ttu-id="4d46b-106">Hozzáad egy vagy több adatbázist egy Azure SQL-adatbázis feladatátvételi csoportjának elsődleges kiszolgálóhoz a feladatátvételi csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="4d46b-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="4d46b-107">Az adatbázisok nem lehetek másodlagos adatbázisok a meglévő replikációs kapcsolatokban.</span><span class="sxs-lookup"><span data-stu-id="4d46b-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="4d46b-108">A parancs elindítja az esetleges hozzáadott adatbázisok georeplikációját a feladatátvételi csoport másodlagos kiszolgálójára.</span><span class="sxs-lookup"><span data-stu-id="4d46b-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="4d46b-109">Ha olyan adatbázis-objektumokat keres, amelyek az "-Database" paramétert kitöltik, használja (például) a Get-AzSqlDatabase parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4d46b-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="4d46b-110">A feladatátvételi csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="4d46b-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="4d46b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d46b-111">EXAMPLES</span></span>

### <span data-ttu-id="4d46b-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="4d46b-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="4d46b-113">Ez a parancs egy adatbázist ad hozzá a feladatátvételi csoporthoz a bemászva.</span><span class="sxs-lookup"><span data-stu-id="4d46b-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="4d46b-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="4d46b-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="4d46b-115">Ez a parancs hozzáadja a kiszolgáló összes adatbázisát egy feladatátvételi csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="4d46b-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="4d46b-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="4d46b-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="4d46b-117">Ez a parancs hozzáadja a rugalmas készletben található összes adatbázist egy feladatátvételi csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="4d46b-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="4d46b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d46b-118">PARAMETERS</span></span>

### <span data-ttu-id="4d46b-119">-Database</span><span class="sxs-lookup"><span data-stu-id="4d46b-119">-Database</span></span>
<span data-ttu-id="4d46b-120">A feladatátvételi csoport elsődleges kiszolgálójának egy vagy több Azure SQL-adatbázisát hozzá kell adni a feladatátvételi csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="4d46b-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="4d46b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d46b-121">-DefaultProfile</span></span>
<span data-ttu-id="4d46b-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4d46b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d46b-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="4d46b-123">-FailoverGroupName</span></span>
<span data-ttu-id="4d46b-124">Az Azure SQL-adatbázis feladatátvételi csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="4d46b-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="4d46b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d46b-125">-ResourceGroupName</span></span>
<span data-ttu-id="4d46b-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d46b-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d46b-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4d46b-127">-ServerName</span></span>
<span data-ttu-id="4d46b-128">A feladatátvételi csoport elsődleges Azure SQL Database Server-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="4d46b-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="4d46b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d46b-129">CommonParameters</span></span>
<span data-ttu-id="4d46b-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d46b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d46b-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d46b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d46b-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d46b-132">INPUTS</span></span>

### <span data-ttu-id="4d46b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4d46b-133">System.String</span></span>

### <span data-ttu-id="4d46b-134">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4d46b-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4d46b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d46b-135">OUTPUTS</span></span>

### <span data-ttu-id="4d46b-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4d46b-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="4d46b-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d46b-137">NOTES</span></span>

## <span data-ttu-id="4d46b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d46b-138">RELATED LINKS</span></span>

[<span data-ttu-id="4d46b-139">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4d46b-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4d46b-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4d46b-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4d46b-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4d46b-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4d46b-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4d46b-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="4d46b-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4d46b-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4d46b-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4d46b-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4d46b-145">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4d46b-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
