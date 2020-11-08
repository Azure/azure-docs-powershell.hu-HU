---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 35f2bc63366a86501650af1808274a3a0403e77f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194183"
---
# <span data-ttu-id="a54f7-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a54f7-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="a54f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a54f7-102">SYNOPSIS</span></span>
<span data-ttu-id="a54f7-103">Adatmaszkolási szabályt hoz létre egy adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="a54f7-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="a54f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a54f7-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a54f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a54f7-105">DESCRIPTION</span></span>
<span data-ttu-id="a54f7-106">A **New-AzSqlDatabaseDataMaskingRule** parancsmag adatmaszkolási szabályt hoz létre egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="a54f7-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="a54f7-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg a szabályt.</span><span class="sxs-lookup"><span data-stu-id="a54f7-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the rule.</span></span>
<span data-ttu-id="a54f7-108">Adja meg a *Táblanév* és a *ColumnName* a szabály céljának és a *MaskingFunction* paraméternek az adatainak maszkolási módjának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="a54f7-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="a54f7-109">Ha a *MaskingFunction* szám vagy szöveg van megadva, megadhatja a *NumberFrom* és az *NumberTo* paramétert, a szám maszkolását, valamint a *PrefixSize* , a *ReplacementString* és a *SuffixSize* a szöveg maszkolásához.</span><span class="sxs-lookup"><span data-stu-id="a54f7-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="a54f7-110">Ha a parancs sikeres, és a *PassThru* paramétert használja, a parancsmag egy olyan objektumot ad eredményül, amely leírja az adatmaszkolási szabály tulajdonságait a szabály-azonosítók mellett.</span><span class="sxs-lookup"><span data-stu-id="a54f7-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="a54f7-111">A *ResourceGroupName* , a *kiszolgálónév* , a *databasename* és a *RuleID* nem csak a szabály-azonosítókat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="a54f7-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="a54f7-112">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="a54f7-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a54f7-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a54f7-113">EXAMPLES</span></span>

### <span data-ttu-id="a54f7-114">Példa 1: adatmaszkolási szabály létrehozása egy adatbázis szám oszlopához</span><span class="sxs-lookup"><span data-stu-id="a54f7-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="a54f7-115">Ez a parancs létrehoz egy adatmaszkolási szabályt a Column01 nevű oszlophoz a Schema01 nevű Table01 nevű táblázatban.</span><span class="sxs-lookup"><span data-stu-id="a54f7-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="a54f7-116">A Database01 nevű adatbázis az összes elemet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a54f7-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="a54f7-117">A szabály egy olyan számozási szabály, amely 5 és 14 közötti véletlenszerű számot használ a maszk értékeként.</span><span class="sxs-lookup"><span data-stu-id="a54f7-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>

## <span data-ttu-id="a54f7-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a54f7-118">PARAMETERS</span></span>

### <span data-ttu-id="a54f7-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a54f7-119">-ColumnName</span></span>
<span data-ttu-id="a54f7-120">A maszkolási szabály által célzott oszlop nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a54f7-120">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="a54f7-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a54f7-121">-DatabaseName</span></span>
<span data-ttu-id="a54f7-122">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a54f7-122">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="a54f7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a54f7-123">-DefaultProfile</span></span>
<span data-ttu-id="a54f7-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a54f7-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a54f7-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="a54f7-125">-MaskingFunction</span></span>
<span data-ttu-id="a54f7-126">A szabály által használt maszkolás függvényt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a54f7-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="a54f7-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a54f7-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a54f7-128">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="a54f7-128">Default</span></span>
- <span data-ttu-id="a54f7-129">A kitakarás</span><span class="sxs-lookup"><span data-stu-id="a54f7-129">NoMasking</span></span>
- <span data-ttu-id="a54f7-130">Szöveg</span><span class="sxs-lookup"><span data-stu-id="a54f7-130">Text</span></span>
- <span data-ttu-id="a54f7-131">Szám</span><span class="sxs-lookup"><span data-stu-id="a54f7-131">Number</span></span>
- <span data-ttu-id="a54f7-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="a54f7-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="a54f7-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="a54f7-133">CreditCardNumber</span></span>
- <span data-ttu-id="a54f7-134">E-mail: az alapértelmezett érték az alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="a54f7-134">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a54f7-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="a54f7-135">-NumberFrom</span></span>
<span data-ttu-id="a54f7-136">Annak az intervallumnak az alsó határát adja meg, amelyből egy véletlenszerű érték van kijelölve.</span><span class="sxs-lookup"><span data-stu-id="a54f7-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="a54f7-137">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.</span><span class="sxs-lookup"><span data-stu-id="a54f7-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a54f7-138">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="a54f7-138">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a54f7-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="a54f7-139">-NumberTo</span></span>
<span data-ttu-id="a54f7-140">Annak az intervallumnak a felső határát adja meg, amelyből egy véletlenszerű érték van kijelölve.</span><span class="sxs-lookup"><span data-stu-id="a54f7-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="a54f7-141">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.</span><span class="sxs-lookup"><span data-stu-id="a54f7-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a54f7-142">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="a54f7-142">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a54f7-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a54f7-143">-PassThru</span></span>
<span data-ttu-id="a54f7-144">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a54f7-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a54f7-145">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a54f7-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a54f7-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="a54f7-146">-PrefixSize</span></span>
<span data-ttu-id="a54f7-147">Itt adhatja meg, hogy a program hány karaktert tartalmaz a nem maszkolt szöveg elején.</span><span class="sxs-lookup"><span data-stu-id="a54f7-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="a54f7-148">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="a54f7-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a54f7-149">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="a54f7-149">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a54f7-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="a54f7-150">-ReplacementString</span></span>
<span data-ttu-id="a54f7-151">Itt adhatja meg, hogy a program hány karaktert tartalmaz a nem maszkolt szöveg végén.</span><span class="sxs-lookup"><span data-stu-id="a54f7-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="a54f7-152">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="a54f7-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a54f7-153">Az alapértelmezett érték egy üres karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="a54f7-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="a54f7-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a54f7-154">-ResourceGroupName</span></span>
<span data-ttu-id="a54f7-155">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a54f7-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a54f7-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a54f7-156">-SchemaName</span></span>
<span data-ttu-id="a54f7-157">A séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a54f7-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="a54f7-158">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a54f7-158">-ServerName</span></span>
<span data-ttu-id="a54f7-159">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a54f7-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="a54f7-160">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="a54f7-160">-SuffixSize</span></span>
<span data-ttu-id="a54f7-161">A nem maszkolt szöveg végén található karakterek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a54f7-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="a54f7-162">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="a54f7-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a54f7-163">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="a54f7-163">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a54f7-164">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="a54f7-164">-TableName</span></span>
<span data-ttu-id="a54f7-165">A maszkolt oszlopot tartalmazó adatbázis-tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a54f7-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="a54f7-166">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a54f7-166">-Confirm</span></span>
<span data-ttu-id="a54f7-167">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a54f7-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a54f7-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a54f7-168">-WhatIf</span></span>
<span data-ttu-id="a54f7-169">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a54f7-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a54f7-170">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a54f7-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a54f7-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a54f7-171">CommonParameters</span></span>
<span data-ttu-id="a54f7-172">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a54f7-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a54f7-173">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a54f7-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a54f7-174">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a54f7-174">INPUTS</span></span>

### <span data-ttu-id="a54f7-175">System. String</span><span class="sxs-lookup"><span data-stu-id="a54f7-175">System.String</span></span>

### <span data-ttu-id="a54f7-176">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a54f7-176">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a54f7-177">System. null ' 1 [[System. Double, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a54f7-177">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a54f7-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a54f7-178">OUTPUTS</span></span>

### <span data-ttu-id="a54f7-179">Microsoft. Azure. Command. SQL. DataMasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="a54f7-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="a54f7-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a54f7-180">NOTES</span></span>

## <span data-ttu-id="a54f7-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a54f7-181">RELATED LINKS</span></span>

[<span data-ttu-id="a54f7-182">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a54f7-182">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a54f7-183">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a54f7-183">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a54f7-184">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a54f7-184">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a54f7-185">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a54f7-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


