---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163291"
---
# <span data-ttu-id="630b8-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="630b8-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="630b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="630b8-102">SYNOPSIS</span></span>
<span data-ttu-id="630b8-103">Eltávolítja az adatbázis adatmaszkolási szabályát.</span><span class="sxs-lookup"><span data-stu-id="630b8-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="630b8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="630b8-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="630b8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="630b8-105">DESCRIPTION</span></span>
<span data-ttu-id="630b8-106">A **Remove-AzSqlDatabaseDataMaskingRule** parancsmag eltávolít egy adott adatmaszkolási szabályt egy Azure SQL-adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="630b8-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="630b8-107">Az adatmaszkolási szabályok eltávolításához használja az *ResourceGroupName,* *a ServerName,* a *DatabaseName* és a *RuleId* paramétert a parancsmag által eltávolított szabály azonosításához.</span><span class="sxs-lookup"><span data-stu-id="630b8-107">You can remove a data masking rule by using the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="630b8-108">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="630b8-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="630b8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="630b8-109">EXAMPLES</span></span>

### <span data-ttu-id="630b8-110">1. példa: Adatbázis-adatmaszkolási szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="630b8-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="630b8-111">Ez a parancs eltávolítja az Adatbázis01 adatbázishoz definiált Szabály01 szabályt.</span><span class="sxs-lookup"><span data-stu-id="630b8-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="630b8-112">Az adatbázis a Server01 kiszolgálón található, és az ResourceGroup01 erőforráscsoporthoz van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="630b8-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="630b8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="630b8-113">PARAMETERS</span></span>

### <span data-ttu-id="630b8-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="630b8-114">-ColumnName</span></span>
<span data-ttu-id="630b8-115">A maszkolási szabály által megcélzott oszlop nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="630b8-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="630b8-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="630b8-116">-DatabaseName</span></span>
<span data-ttu-id="630b8-117">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="630b8-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="630b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="630b8-118">-DefaultProfile</span></span>
<span data-ttu-id="630b8-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="630b8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="630b8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="630b8-120">-Force</span></span>
<span data-ttu-id="630b8-121">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="630b8-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="630b8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="630b8-122">-PassThru</span></span>
<span data-ttu-id="630b8-123">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="630b8-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="630b8-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="630b8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="630b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="630b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="630b8-126">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="630b8-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="630b8-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="630b8-127">-SchemaName</span></span>
<span data-ttu-id="630b8-128">Egy séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="630b8-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="630b8-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="630b8-129">-ServerName</span></span>
<span data-ttu-id="630b8-130">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="630b8-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="630b8-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="630b8-131">-TableName</span></span>
<span data-ttu-id="630b8-132">Egy Azure SQL-tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="630b8-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="630b8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="630b8-133">-Confirm</span></span>
<span data-ttu-id="630b8-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="630b8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="630b8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="630b8-135">-WhatIf</span></span>
<span data-ttu-id="630b8-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="630b8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="630b8-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="630b8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="630b8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="630b8-138">CommonParameters</span></span>
<span data-ttu-id="630b8-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="630b8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="630b8-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="630b8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="630b8-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="630b8-141">INPUTS</span></span>

### <span data-ttu-id="630b8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="630b8-142">System.String</span></span>

## <span data-ttu-id="630b8-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="630b8-143">OUTPUTS</span></span>

### <span data-ttu-id="630b8-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="630b8-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="630b8-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="630b8-145">NOTES</span></span>

## <span data-ttu-id="630b8-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="630b8-146">RELATED LINKS</span></span>

[<span data-ttu-id="630b8-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="630b8-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="630b8-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="630b8-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="630b8-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="630b8-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="630b8-150">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="630b8-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


