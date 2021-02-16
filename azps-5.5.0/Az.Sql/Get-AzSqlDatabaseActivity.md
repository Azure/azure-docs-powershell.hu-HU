---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: df4ad0ea9f0e1990fa3c71915b1882baf1d3a762
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150602"
---
# <span data-ttu-id="d19f5-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="d19f5-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="d19f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d19f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d19f5-103">Az adatbázis-műveletek állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d19f5-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="d19f5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d19f5-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d19f5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d19f5-105">DESCRIPTION</span></span>
<span data-ttu-id="d19f5-106">A **Get-AzSqlDatabaseActivity** parancsmag az Azure SQL-adatbázisban lekért adatbázis-műveletek állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d19f5-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="d19f5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d19f5-107">EXAMPLES</span></span>

### <span data-ttu-id="d19f5-108">1. példa: Állapot lekérte az összes SQL-adatbázispéldány állapotát</span><span class="sxs-lookup"><span data-stu-id="d19f5-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="d19f5-109">Ez a parancs egy RugalmasságPool01 nevű rugalmas készlet összes SQL-adatbázis-példányának műveletállapotát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d19f5-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="d19f5-110">2. példa: Állapot lekérte az ÖSSZES SQL-adatbázis-művelet állapotát</span><span class="sxs-lookup"><span data-stu-id="d19f5-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d19f5-111">Ez a parancs egy adatbázis összes SQL-adatbázis-műveletének állapotát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d19f5-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="d19f5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d19f5-112">PARAMETERS</span></span>

### <span data-ttu-id="d19f5-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d19f5-113">-DatabaseName</span></span>
<span data-ttu-id="d19f5-114">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="d19f5-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d19f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d19f5-115">-DefaultProfile</span></span>
<span data-ttu-id="d19f5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d19f5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d19f5-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d19f5-117">-ElasticPoolName</span></span>
<span data-ttu-id="d19f5-118">Annak a rugalmas adatbáziskészletnek a neve, amelynek a parancsmagja állapotát kapja.</span><span class="sxs-lookup"><span data-stu-id="d19f5-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="d19f5-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d19f5-119">-OperationId</span></span>
<span data-ttu-id="d19f5-120">A parancsmag által lekért művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d19f5-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d19f5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d19f5-121">-ResourceGroupName</span></span>
<span data-ttu-id="d19f5-122">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="d19f5-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d19f5-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d19f5-123">-ServerName</span></span>
<span data-ttu-id="d19f5-124">Az adatbázist tartalmazó Microsoft SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="d19f5-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="d19f5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d19f5-125">-Confirm</span></span>
<span data-ttu-id="d19f5-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d19f5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d19f5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d19f5-127">-WhatIf</span></span>
<span data-ttu-id="d19f5-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d19f5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d19f5-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d19f5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d19f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d19f5-130">CommonParameters</span></span>
<span data-ttu-id="d19f5-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d19f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d19f5-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d19f5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d19f5-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d19f5-133">INPUTS</span></span>

### <span data-ttu-id="d19f5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d19f5-134">System.String</span></span>

### <span data-ttu-id="d19f5-135">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d19f5-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d19f5-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d19f5-136">OUTPUTS</span></span>

### <span data-ttu-id="d19f5-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="d19f5-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="d19f5-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d19f5-138">NOTES</span></span>

## <span data-ttu-id="d19f5-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d19f5-139">RELATED LINKS</span></span>
