---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 016b77c7e58a3c95405d6364118a9d0ec7815660
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668863"
---
# <span data-ttu-id="76b7d-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="76b7d-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="76b7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="76b7d-103">Az adatmaszkolási szabály eltávolítása egy adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="76b7d-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="76b7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76b7d-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76b7d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="76b7d-105">DESCRIPTION</span></span>
<span data-ttu-id="76b7d-106">A **Remove-AzSqlDatabaseDataMaskingRule** parancsmag egy adott adatmaszkolási szabályt távolít el egy Azure SQL-adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="76b7d-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="76b7d-107">Az adatmaszkolási szabályokat a *ResourceGroupName* , a *kiszolgálónév* , a *databasename* és a *RuleId* paraméter használatával távolíthatja el a parancsmag által eltávolított szabály meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="76b7d-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="76b7d-108">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="76b7d-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="76b7d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="76b7d-109">EXAMPLES</span></span>

### <span data-ttu-id="76b7d-110">1. példa: az adatbázis-adatmaszkolási szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="76b7d-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="76b7d-111">Ez a parancs eltávolítja az adatbázis-Database01 definiált szabály neve Rule01.</span><span class="sxs-lookup"><span data-stu-id="76b7d-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="76b7d-112">Az adatbázis a Server01-on található, és az erőforráscsoport ResourceGroup01 van társítva.</span><span class="sxs-lookup"><span data-stu-id="76b7d-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="76b7d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76b7d-113">PARAMETERS</span></span>

### <span data-ttu-id="76b7d-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="76b7d-114">-ColumnName</span></span>
<span data-ttu-id="76b7d-115">A maszkolási szabály által célzott oszlop nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76b7d-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="76b7d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="76b7d-116">-DatabaseName</span></span>
<span data-ttu-id="76b7d-117">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76b7d-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="76b7d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b7d-118">-DefaultProfile</span></span>
<span data-ttu-id="76b7d-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="76b7d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76b7d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="76b7d-120">-Force</span></span>
<span data-ttu-id="76b7d-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="76b7d-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="76b7d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76b7d-122">-PassThru</span></span>
<span data-ttu-id="76b7d-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="76b7d-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="76b7d-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="76b7d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="76b7d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76b7d-125">-ResourceGroupName</span></span>
<span data-ttu-id="76b7d-126">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="76b7d-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="76b7d-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="76b7d-127">-SchemaName</span></span>
<span data-ttu-id="76b7d-128">A séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76b7d-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="76b7d-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="76b7d-129">-ServerName</span></span>
<span data-ttu-id="76b7d-130">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76b7d-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="76b7d-131">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="76b7d-131">-TableName</span></span>
<span data-ttu-id="76b7d-132">Egy Azure SQL-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76b7d-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="76b7d-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="76b7d-133">-Confirm</span></span>
<span data-ttu-id="76b7d-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76b7d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76b7d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76b7d-135">-WhatIf</span></span>
<span data-ttu-id="76b7d-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="76b7d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76b7d-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76b7d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76b7d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b7d-138">CommonParameters</span></span>
<span data-ttu-id="76b7d-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76b7d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b7d-140">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="76b7d-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b7d-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76b7d-141">INPUTS</span></span>

### <span data-ttu-id="76b7d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="76b7d-142">System.String</span></span>

## <span data-ttu-id="76b7d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76b7d-143">OUTPUTS</span></span>

### <span data-ttu-id="76b7d-144">Microsoft. Azure. Command. SQL. DataMasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="76b7d-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="76b7d-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76b7d-145">NOTES</span></span>

## <span data-ttu-id="76b7d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76b7d-146">RELATED LINKS</span></span>

[<span data-ttu-id="76b7d-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="76b7d-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="76b7d-148">Új – AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="76b7d-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="76b7d-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="76b7d-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="76b7d-150">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="76b7d-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


