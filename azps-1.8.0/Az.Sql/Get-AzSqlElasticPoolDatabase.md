---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: f03d172db1a4e8952fea989499f1689d9e0b6a83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668984"
---
# <span data-ttu-id="7f9c6-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="7f9c6-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="7f9c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="7f9c6-103">Elasztikus adatbázisokat kap egy rugalmas készletben és a hozzájuk tartozó tulajdonsági értékeken.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="7f9c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f9c6-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f9c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f9c6-105">DESCRIPTION</span></span>
<span data-ttu-id="7f9c6-106">A **Get-AzSqlElasticPoolDatabase** parancsmag rugalmasan változó adatbázisokat és a hozzájuk tartozó tulajdonságértékeket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="7f9c6-107">Az Azure SQL-adatbázisban megadhatja a rugalmas adatbázis nevét úgy, hogy csak az adott adatbázishoz tartozó tulajdonságértékeket láthassa.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="7f9c6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7f9c6-108">EXAMPLES</span></span>

### <span data-ttu-id="7f9c6-109">Példa 1: az összes adatbázis beszerzése rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="7f9c6-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="7f9c6-110">Ez a parancs a ElasticPool01 nevű rugalmas készlet minden adatbázisát bekapja.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="7f9c6-111">2. példa: az összes adatbázis beolvasása egy rugalmas készletbe szűréssel</span><span class="sxs-lookup"><span data-stu-id="7f9c6-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="7f9c6-112">Ez a parancs a ElasticPool01 nevű rugalmas készlet minden adatbázisát beilleszti az "adatbázis" értékkel kezdődően.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="7f9c6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f9c6-113">PARAMETERS</span></span>

### <span data-ttu-id="7f9c6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7f9c6-114">-DatabaseName</span></span>
<span data-ttu-id="7f9c6-115">Annak az SQL-adatbázisnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7f9c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f9c6-116">-DefaultProfile</span></span>
<span data-ttu-id="7f9c6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f9c6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f9c6-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7f9c6-118">-ElasticPoolName</span></span>
<span data-ttu-id="7f9c6-119">Egy rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="7f9c6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f9c6-120">-ResourceGroupName</span></span>
<span data-ttu-id="7f9c6-121">Annak a csoportnak a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="7f9c6-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7f9c6-122">-ServerName</span></span>
<span data-ttu-id="7f9c6-123">Egy rugalmas készletet tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="7f9c6-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7f9c6-124">-Confirm</span></span>
<span data-ttu-id="7f9c6-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f9c6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f9c6-126">-WhatIf</span></span>
<span data-ttu-id="7f9c6-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f9c6-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f9c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f9c6-129">CommonParameters</span></span>
<span data-ttu-id="7f9c6-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f9c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f9c6-131">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7f9c6-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f9c6-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f9c6-132">INPUTS</span></span>

### <span data-ttu-id="7f9c6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7f9c6-133">System.String</span></span>

## <span data-ttu-id="7f9c6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f9c6-134">OUTPUTS</span></span>

### <span data-ttu-id="7f9c6-135">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7f9c6-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="7f9c6-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f9c6-136">NOTES</span></span>

## <span data-ttu-id="7f9c6-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f9c6-137">RELATED LINKS</span></span>

[<span data-ttu-id="7f9c6-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7f9c6-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="7f9c6-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="7f9c6-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="7f9c6-140">Új – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7f9c6-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="7f9c6-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7f9c6-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="7f9c6-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7f9c6-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

