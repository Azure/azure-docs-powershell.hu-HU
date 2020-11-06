---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 2772f806ba5297ee9809a8800b25b4c42daf171e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499939"
---
# <span data-ttu-id="bb750-101">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bb750-101">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="bb750-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb750-102">SYNOPSIS</span></span>
<span data-ttu-id="bb750-103">Egy vagy több adatbázis hozzáadása egy Azure SQL-adatbázis feladatátvételi csoportjához.</span><span class="sxs-lookup"><span data-stu-id="bb750-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb750-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb750-104">SYNTAX</span></span>

```
Add-AzureRmSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb750-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb750-105">DESCRIPTION</span></span>
<span data-ttu-id="bb750-106">Egy vagy több adatbázis hozzáadása egy Azure SQL-adatbázis feladatátvételi csoportjához tartozó elsődleges kiszolgálón az adott feladatátvételi csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="bb750-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="bb750-107">Az adatbázisok nem lehetnek másodlagos adatbázisok a meglévő replikációs kapcsolatokban.</span><span class="sxs-lookup"><span data-stu-id="bb750-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="bb750-108">A parancs minden hozzáadott adatbázis geo-replikációját a feladatátvételi csoport másodlagos kiszolgálójához fogja elindítani.</span><span class="sxs-lookup"><span data-stu-id="bb750-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>

<span data-ttu-id="bb750-109">Ha olyan adatbázis-objektumokat szeretne beolvasni, amelyekkel feltöltheti az "-Database" paramétert, használja (például) az Get-AzureRmSqlDatabase parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bb750-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="bb750-110">A feladatátvevő csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="bb750-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="bb750-111">Példák</span><span class="sxs-lookup"><span data-stu-id="bb750-111">EXAMPLES</span></span>

### <span data-ttu-id="bb750-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bb750-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="bb750-113">Ebben a parancsban a program kijelöli az egyik adatbázist a feladatátvételi csoportba.</span><span class="sxs-lookup"><span data-stu-id="bb750-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="bb750-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="bb750-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="bb750-115">Ez a parancs hozzáadja a kiszolgáló minden adatbázisát a feladatátvételi csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="bb750-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="bb750-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="bb750-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzureRmSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="bb750-117">Ez a parancs egy rugalmas készlet minden adatbázisát felveszi a feladatátvételi csoportba.</span><span class="sxs-lookup"><span data-stu-id="bb750-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="bb750-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb750-118">PARAMETERS</span></span>

### <span data-ttu-id="bb750-119">-Database (adatbázis)</span><span class="sxs-lookup"><span data-stu-id="bb750-119">-Database</span></span>
<span data-ttu-id="bb750-120">A feladatátvételi csoport elsődleges kiszolgálóin egy vagy több Azure SQL-adatbázis szerepelni fog a feladatátvételi csoportban.</span><span class="sxs-lookup"><span data-stu-id="bb750-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="bb750-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="bb750-121">-FailoverGroupName</span></span>
<span data-ttu-id="bb750-122">Az Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="bb750-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="bb750-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb750-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb750-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bb750-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="bb750-125">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="bb750-125">-ServerName</span></span>
<span data-ttu-id="bb750-126">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="bb750-126">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="bb750-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb750-127">-DefaultProfile</span></span>
<span data-ttu-id="bb750-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb750-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb750-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb750-129">CommonParameters</span></span>
<span data-ttu-id="bb750-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb750-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb750-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb750-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb750-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb750-132">INPUTS</span></span>

### <span data-ttu-id="bb750-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bb750-133">System.String</span></span>
<span data-ttu-id="bb750-134">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. commands. SQL. database. Model. AzureSqlDatabaseModel, Microsoft. Azure. Command. SQL, Version = 2.5.0.0, Culture = semleges, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="bb750-134">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="bb750-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb750-135">OUTPUTS</span></span>

### <span data-ttu-id="bb750-136">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="bb750-136">System.Object</span></span>

## <span data-ttu-id="bb750-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb750-137">NOTES</span></span>

## <span data-ttu-id="bb750-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb750-138">RELATED LINKS</span></span>

[<span data-ttu-id="bb750-139">Új – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bb750-139">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bb750-140">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bb750-140">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bb750-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bb750-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bb750-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bb750-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="bb750-143">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bb750-143">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bb750-144">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bb750-144">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bb750-145">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="bb750-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
