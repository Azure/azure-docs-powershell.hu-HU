---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 8813d405ebc8fadafa037afb884240dcdbb95383
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164979"
---
# <span data-ttu-id="4f310-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4f310-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="4f310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f310-102">SYNOPSIS</span></span>
<span data-ttu-id="4f310-103">Beveszi az adatbázisból az adatmaszkolási szabályokat.</span><span class="sxs-lookup"><span data-stu-id="4f310-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="4f310-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4f310-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f310-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4f310-105">DESCRIPTION</span></span>
<span data-ttu-id="4f310-106">A **Get-AzSqlDatabaseDataMaskingRule** parancsmag egy adott adatmaszkolási szabályt vagy egy Azure SQL-adatbázis összes adatmaszkolási szabályát megkapja.</span><span class="sxs-lookup"><span data-stu-id="4f310-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="4f310-107">A parancsmagot a *ResourceGroupName,* *a ServerName* és a *DatabaseName* paraméter használatával azonosíthatja az adatbázist, a *RuleId* paraméterrel pedig megadhatja, hogy ez a parancsmag melyik szabályt adja vissza.</span><span class="sxs-lookup"><span data-stu-id="4f310-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="4f310-108">Ha nem adja meg a *RuleId adatot,* az adott Azure SQL-adatbázis összes adatmaszkolási szabályát visszaadja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="4f310-108">If you do not provide *RuleId*, all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="4f310-109">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="4f310-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4f310-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4f310-110">EXAMPLES</span></span>

### <span data-ttu-id="4f310-111">1. példa: Az összes adatmaszkolási szabály be szerezni egy adatbázisból</span><span class="sxs-lookup"><span data-stu-id="4f310-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :

DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table2
ColumnName        : column2
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

### <span data-ttu-id="4f310-112">2. példa: A "dbo", a "table1" táblában és az "oszlop1" oszlopban definiált adatmaszkolási szabály be szerezni.</span><span class="sxs-lookup"><span data-stu-id="4f310-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

## <span data-ttu-id="4f310-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f310-113">PARAMETERS</span></span>

### <span data-ttu-id="4f310-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="4f310-114">-ColumnName</span></span>
<span data-ttu-id="4f310-115">A maszkolási szabály által megcélzott oszlop nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f310-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="4f310-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4f310-116">-DatabaseName</span></span>
<span data-ttu-id="4f310-117">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f310-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="4f310-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f310-118">-DefaultProfile</span></span>
<span data-ttu-id="4f310-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4f310-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f310-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f310-120">-ResourceGroupName</span></span>
<span data-ttu-id="4f310-121">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="4f310-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4f310-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4f310-122">-SchemaName</span></span>
<span data-ttu-id="4f310-123">Egy séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f310-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="4f310-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4f310-124">-ServerName</span></span>
<span data-ttu-id="4f310-125">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f310-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="4f310-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="4f310-126">-TableName</span></span>
<span data-ttu-id="4f310-127">Egy Azure SQL-tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f310-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="4f310-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f310-128">-Confirm</span></span>
<span data-ttu-id="4f310-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4f310-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f310-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f310-130">-WhatIf</span></span>
<span data-ttu-id="4f310-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4f310-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f310-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4f310-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f310-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f310-133">CommonParameters</span></span>
<span data-ttu-id="4f310-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f310-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f310-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f310-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f310-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f310-136">INPUTS</span></span>

### <span data-ttu-id="4f310-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4f310-137">System.String</span></span>

## <span data-ttu-id="4f310-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f310-138">OUTPUTS</span></span>

### <span data-ttu-id="4f310-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="4f310-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="4f310-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4f310-140">NOTES</span></span>

## <span data-ttu-id="4f310-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f310-141">RELATED LINKS</span></span>

[<span data-ttu-id="4f310-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="4f310-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="4f310-143">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4f310-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="4f310-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4f310-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="4f310-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="4f310-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="4f310-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4f310-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


