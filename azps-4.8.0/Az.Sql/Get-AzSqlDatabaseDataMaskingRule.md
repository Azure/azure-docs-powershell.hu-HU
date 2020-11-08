---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 8813d405ebc8fadafa037afb884240dcdbb95383
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017573"
---
# <span data-ttu-id="87dab-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="87dab-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="87dab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87dab-102">SYNOPSIS</span></span>
<span data-ttu-id="87dab-103">Egy adatbázis adatmaszkolási szabályait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="87dab-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="87dab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87dab-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87dab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="87dab-105">DESCRIPTION</span></span>
<span data-ttu-id="87dab-106">A **Get-AzSqlDatabaseDataMaskingRule** parancsmag egy bizonyos adatmaszkolási szabályt vagy az Azure SQL-adatbázis minden adatmaszkolási szabályát kapja.</span><span class="sxs-lookup"><span data-stu-id="87dab-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="87dab-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist, és a *RuleId* paraméterrel adja meg, hogy melyik szabály a parancsmagot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="87dab-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="87dab-108">Ha nem ad meg *RuleId* , az adott Azure SQL-adatbázishoz tartozó összes adatmaszkolási szabály visszakerül.</span><span class="sxs-lookup"><span data-stu-id="87dab-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="87dab-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="87dab-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="87dab-110">Példák</span><span class="sxs-lookup"><span data-stu-id="87dab-110">EXAMPLES</span></span>

### <span data-ttu-id="87dab-111">Példa 1: az adatmaszkolási szabályok beszerzése adatbázisból</span><span class="sxs-lookup"><span data-stu-id="87dab-111">Example 1: Get all data masking rules from a database</span></span>
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

### <span data-ttu-id="87dab-112">2. példa: a "dbo", "tábla1" és "Oszlop1" oszlop adatmaszkolási szabályának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="87dab-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
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

## <span data-ttu-id="87dab-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87dab-113">PARAMETERS</span></span>

### <span data-ttu-id="87dab-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="87dab-114">-ColumnName</span></span>
<span data-ttu-id="87dab-115">A maszkolási szabály által célzott oszlop nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87dab-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="87dab-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="87dab-116">-DatabaseName</span></span>
<span data-ttu-id="87dab-117">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87dab-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="87dab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87dab-118">-DefaultProfile</span></span>
<span data-ttu-id="87dab-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="87dab-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87dab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87dab-120">-ResourceGroupName</span></span>
<span data-ttu-id="87dab-121">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="87dab-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="87dab-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="87dab-122">-SchemaName</span></span>
<span data-ttu-id="87dab-123">A séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87dab-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="87dab-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="87dab-124">-ServerName</span></span>
<span data-ttu-id="87dab-125">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87dab-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="87dab-126">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="87dab-126">-TableName</span></span>
<span data-ttu-id="87dab-127">Egy Azure SQL-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87dab-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="87dab-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87dab-128">-Confirm</span></span>
<span data-ttu-id="87dab-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87dab-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87dab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87dab-130">-WhatIf</span></span>
<span data-ttu-id="87dab-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="87dab-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87dab-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87dab-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87dab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87dab-133">CommonParameters</span></span>
<span data-ttu-id="87dab-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87dab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87dab-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="87dab-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87dab-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87dab-136">INPUTS</span></span>

### <span data-ttu-id="87dab-137">System. String</span><span class="sxs-lookup"><span data-stu-id="87dab-137">System.String</span></span>

## <span data-ttu-id="87dab-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87dab-138">OUTPUTS</span></span>

### <span data-ttu-id="87dab-139">Microsoft. Azure. Command. SQL. DataMasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="87dab-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="87dab-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87dab-140">NOTES</span></span>

## <span data-ttu-id="87dab-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87dab-141">RELATED LINKS</span></span>

[<span data-ttu-id="87dab-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="87dab-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="87dab-143">Új – AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="87dab-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="87dab-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="87dab-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="87dab-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="87dab-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="87dab-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="87dab-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


