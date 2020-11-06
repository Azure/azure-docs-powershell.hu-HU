---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: ced87eb217347629752683be5c72229da92dea64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494629"
---
# <span data-ttu-id="21273-101">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="21273-101">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="21273-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21273-102">SYNOPSIS</span></span>
<span data-ttu-id="21273-103">Egy adatbázis adatmaszkolási szabályait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="21273-103">Gets the data masking rules from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21273-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21273-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21273-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="21273-105">DESCRIPTION</span></span>
<span data-ttu-id="21273-106">A **Get-AzureRmSqlDatabaseDataMaskingRule** parancsmag egy bizonyos adatmaszkolási szabályt vagy az Azure SQL-adatbázis minden adatmaszkolási szabályát kapja.</span><span class="sxs-lookup"><span data-stu-id="21273-106">The **Get-AzureRmSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="21273-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist, és a *RuleId* paraméterrel adja meg, hogy melyik szabály a parancsmagot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="21273-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="21273-108">Ha nem ad meg *RuleId* , az adott Azure SQL-adatbázishoz tartozó összes adatmaszkolási szabály visszakerül.</span><span class="sxs-lookup"><span data-stu-id="21273-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>

<span data-ttu-id="21273-109">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="21273-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="21273-110">Példák</span><span class="sxs-lookup"><span data-stu-id="21273-110">EXAMPLES</span></span>

### <span data-ttu-id="21273-111">Példa 1: az adatmaszkolási szabályok beszerzése adatbázisból</span><span class="sxs-lookup"><span data-stu-id="21273-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

### <span data-ttu-id="21273-112">2. példa: a "dbo", "tábla1" és "Oszlop1" oszlop adatmaszkolási szabályának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="21273-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
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

## <span data-ttu-id="21273-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21273-113">PARAMETERS</span></span>

### <span data-ttu-id="21273-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="21273-114">-ColumnName</span></span>
<span data-ttu-id="21273-115">A maszkolási szabály által célzott oszlop nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="21273-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="21273-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="21273-116">-DatabaseName</span></span>
<span data-ttu-id="21273-117">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="21273-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="21273-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21273-118">-ResourceGroupName</span></span>
<span data-ttu-id="21273-119">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="21273-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="21273-120">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="21273-120">-SchemaName</span></span>
<span data-ttu-id="21273-121">A séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="21273-121">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="21273-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="21273-122">-ServerName</span></span>
<span data-ttu-id="21273-123">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="21273-123">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="21273-124">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="21273-124">-TableName</span></span>
<span data-ttu-id="21273-125">Egy Azure SQL-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="21273-125">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="21273-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="21273-126">-Confirm</span></span>
<span data-ttu-id="21273-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21273-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21273-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21273-128">-WhatIf</span></span>
<span data-ttu-id="21273-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="21273-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21273-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21273-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21273-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21273-131">-DefaultProfile</span></span>
<span data-ttu-id="21273-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21273-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21273-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21273-133">CommonParameters</span></span>
<span data-ttu-id="21273-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21273-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21273-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21273-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21273-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21273-136">INPUTS</span></span>

###  
<span data-ttu-id="21273-137">Nincs.</span><span class="sxs-lookup"><span data-stu-id="21273-137">None.</span></span>

## <span data-ttu-id="21273-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21273-138">OUTPUTS</span></span>

### <span data-ttu-id="21273-139">Microsoft. Azure. Command. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="21273-139">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="21273-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21273-140">NOTES</span></span>

## <span data-ttu-id="21273-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21273-141">RELATED LINKS</span></span>

[<span data-ttu-id="21273-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="21273-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="21273-143">Új – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="21273-143">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="21273-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="21273-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="21273-145">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="21273-145">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="21273-146">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="21273-146">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


