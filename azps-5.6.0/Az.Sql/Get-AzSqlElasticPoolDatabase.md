---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 4a9e128fb8c67c44329dd2b99da8ce4722835323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999526"
---
# <span data-ttu-id="d601b-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="d601b-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="d601b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d601b-102">SYNOPSIS</span></span>
<span data-ttu-id="d601b-103">Rugalmas adatbázisokat és tulajdonságértékeket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d601b-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="d601b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d601b-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d601b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d601b-105">DESCRIPTION</span></span>
<span data-ttu-id="d601b-106">A **Get-AzSqlElasticPoolDatabase** parancsmag rugalmas adatbázisokat kap egy rugalmas készletben és azok tulajdonságértékeivel.</span><span class="sxs-lookup"><span data-stu-id="d601b-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="d601b-107">Megadhatja egy rugalmas adatbázis nevét az Azure SQL-adatbázisban, hogy csak az adott adatbázis tulajdonságértékét lássa.</span><span class="sxs-lookup"><span data-stu-id="d601b-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="d601b-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d601b-108">EXAMPLES</span></span>

### <span data-ttu-id="d601b-109">1. példa: Az összes adatbázis behozása rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="d601b-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="d601b-110">Ez a parancs az összes adatbázist egy RugalmasságPool01 nevű rugalmas készletbe kapja.</span><span class="sxs-lookup"><span data-stu-id="d601b-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="d601b-111">2. példa: Az összes adatbázis behozása rugalmas készletbe szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="d601b-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="d601b-112">Ez a parancs az összes adatbázist egy RugalmasságPool01 nevű rugalmas készletbe beveszi, amely az "Adatbázis" kezdetű.</span><span class="sxs-lookup"><span data-stu-id="d601b-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="d601b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d601b-113">PARAMETERS</span></span>

### <span data-ttu-id="d601b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d601b-114">-DatabaseName</span></span>
<span data-ttu-id="d601b-115">Annak az SQL-adatbázisnak a nevét adja meg, amelybe a parancsmagot beállítja.</span><span class="sxs-lookup"><span data-stu-id="d601b-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d601b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d601b-116">-DefaultProfile</span></span>
<span data-ttu-id="d601b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d601b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d601b-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d601b-118">-ElasticPoolName</span></span>
<span data-ttu-id="d601b-119">Egy rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d601b-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="d601b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d601b-120">-ResourceGroupName</span></span>
<span data-ttu-id="d601b-121">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a rugalmas készlet hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="d601b-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="d601b-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d601b-122">-ServerName</span></span>
<span data-ttu-id="d601b-123">Egy rugalmas készletet tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d601b-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="d601b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d601b-124">-Confirm</span></span>
<span data-ttu-id="d601b-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d601b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d601b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d601b-126">-WhatIf</span></span>
<span data-ttu-id="d601b-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d601b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d601b-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d601b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d601b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d601b-129">CommonParameters</span></span>
<span data-ttu-id="d601b-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d601b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d601b-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d601b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d601b-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d601b-132">INPUTS</span></span>

### <span data-ttu-id="d601b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d601b-133">System.String</span></span>

## <span data-ttu-id="d601b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d601b-134">OUTPUTS</span></span>

### <span data-ttu-id="d601b-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d601b-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d601b-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d601b-136">NOTES</span></span>

## <span data-ttu-id="d601b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d601b-137">RELATED LINKS</span></span>

[<span data-ttu-id="d601b-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d601b-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="d601b-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="d601b-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="d601b-140">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d601b-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="d601b-141">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d601b-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="d601b-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d601b-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

