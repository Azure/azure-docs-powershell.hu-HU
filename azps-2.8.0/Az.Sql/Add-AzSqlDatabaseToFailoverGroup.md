---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: aaf2063d82e0140e9abe07b7343a2c314e2fbd7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837980"
---
# <span data-ttu-id="89b8a-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="89b8a-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="89b8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="89b8a-103">Egy vagy több adatbázis hozzáadása egy Azure SQL-adatbázis feladatátvételi csoportjához.</span><span class="sxs-lookup"><span data-stu-id="89b8a-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="89b8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89b8a-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89b8a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89b8a-105">DESCRIPTION</span></span>
<span data-ttu-id="89b8a-106">Egy vagy több adatbázis hozzáadása egy Azure SQL-adatbázis feladatátvételi csoportjához tartozó elsődleges kiszolgálón az adott feladatátvételi csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="89b8a-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="89b8a-107">Az adatbázisok nem lehetnek másodlagos adatbázisok a meglévő replikációs kapcsolatokban.</span><span class="sxs-lookup"><span data-stu-id="89b8a-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="89b8a-108">A parancs minden hozzáadott adatbázis geo-replikációját a feladatátvételi csoport másodlagos kiszolgálójához fogja elindítani.</span><span class="sxs-lookup"><span data-stu-id="89b8a-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="89b8a-109">Ha olyan adatbázis-objektumokat szeretne beolvasni, amelyekkel feltöltheti az "-Database" paramétert, használja (például) az Get-AzSqlDatabase parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="89b8a-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="89b8a-110">A feladatátvevő csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="89b8a-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="89b8a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="89b8a-111">EXAMPLES</span></span>

### <span data-ttu-id="89b8a-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="89b8a-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="89b8a-113">Ebben a parancsban a program kijelöli az egyik adatbázist a feladatátvételi csoportba.</span><span class="sxs-lookup"><span data-stu-id="89b8a-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="89b8a-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="89b8a-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="89b8a-115">Ez a parancs hozzáadja a kiszolgáló minden adatbázisát a feladatátvételi csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="89b8a-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="89b8a-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="89b8a-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="89b8a-117">Ez a parancs egy rugalmas készlet minden adatbázisát felveszi a feladatátvételi csoportba.</span><span class="sxs-lookup"><span data-stu-id="89b8a-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="89b8a-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89b8a-118">PARAMETERS</span></span>

### <span data-ttu-id="89b8a-119">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="89b8a-119">-Database</span></span>
<span data-ttu-id="89b8a-120">A feladatátvételi csoport elsődleges kiszolgálóin egy vagy több Azure SQL-adatbázis szerepelni fog a feladatátvételi csoportban.</span><span class="sxs-lookup"><span data-stu-id="89b8a-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="89b8a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b8a-121">-DefaultProfile</span></span>
<span data-ttu-id="89b8a-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="89b8a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89b8a-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="89b8a-123">-FailoverGroupName</span></span>
<span data-ttu-id="89b8a-124">Az Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="89b8a-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="89b8a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89b8a-125">-ResourceGroupName</span></span>
<span data-ttu-id="89b8a-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="89b8a-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="89b8a-127">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="89b8a-127">-ServerName</span></span>
<span data-ttu-id="89b8a-128">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="89b8a-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="89b8a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b8a-129">CommonParameters</span></span>
<span data-ttu-id="89b8a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89b8a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b8a-131">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="89b8a-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b8a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89b8a-132">INPUTS</span></span>

### <span data-ttu-id="89b8a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="89b8a-133">System.String</span></span>

### <span data-ttu-id="89b8a-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. SQL. database. Model. AzureSqlDatabaseModel, Microsoft. Azure. PowerShell. parancsmag. SQL, Version = 1.3.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="89b8a-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="89b8a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89b8a-135">OUTPUTS</span></span>

### <span data-ttu-id="89b8a-136">Microsoft. Azure. Command. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="89b8a-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="89b8a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89b8a-137">NOTES</span></span>

## <span data-ttu-id="89b8a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89b8a-138">RELATED LINKS</span></span>

[<span data-ttu-id="89b8a-139">Új – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="89b8a-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="89b8a-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="89b8a-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="89b8a-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="89b8a-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="89b8a-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="89b8a-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="89b8a-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="89b8a-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="89b8a-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="89b8a-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="89b8a-145">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="89b8a-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
