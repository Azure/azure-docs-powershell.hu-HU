---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: eb5e809b3f48403a6095f84643af0a169b2cecf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839427"
---
# <span data-ttu-id="0d6e3-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0d6e3-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="0d6e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d6e3-102">SYNOPSIS</span></span>
<span data-ttu-id="0d6e3-103">Adatmaszkolási szabályt hoz létre egy adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="0d6e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d6e3-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d6e3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d6e3-105">DESCRIPTION</span></span>
<span data-ttu-id="0d6e3-106">A **New-AzSqlDatabaseDataMaskingRule** parancsmag adatmaszkolási szabályt hoz létre egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="0d6e3-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* , a *databasename* és a *RuleId* paraméterrel keresse meg a szabályt.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="0d6e3-108">Adja meg a *Táblanév* és a *ColumnName* a szabály céljának és a *MaskingFunction* paraméternek az adatainak maszkolási módjának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="0d6e3-109">Ha a *MaskingFunction* szám vagy szöveg van megadva, megadhatja a *NumberFrom* és az *NumberTo* paramétert, a szám maszkolását, valamint a *PrefixSize* , a *ReplacementString* és a *SuffixSize* a szöveg maszkolásához.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="0d6e3-110">Ha a parancs sikeres, és a *PassThru* paramétert használja, a parancsmag egy olyan objektumot ad eredményül, amely leírja az adatmaszkolási szabály tulajdonságait a szabály-azonosítók mellett.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="0d6e3-111">A *ResourceGroupName* , a *kiszolgálónév* , a *databasename* és a *RuleID* nem csak a szabály-azonosítókat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="0d6e3-112">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0d6e3-113">Példák</span><span class="sxs-lookup"><span data-stu-id="0d6e3-113">EXAMPLES</span></span>

### <span data-ttu-id="0d6e3-114">Példa 1: adatmaszkolási szabály létrehozása egy adatbázis szám oszlopához</span><span class="sxs-lookup"><span data-stu-id="0d6e3-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="0d6e3-115">Ez a parancs létrehoz egy adatmaszkolási szabályt a Column01 nevű oszlophoz a Schema01 nevű Table01 nevű táblázatban.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="0d6e3-116">A Database01 nevű adatbázis az összes elemet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="0d6e3-117">A szabály egy olyan számozási szabály, amely 5 és 14 közötti véletlenszerű számot használ a maszk értékeként.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="0d6e3-118">A szabály neve Rule01.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="0d6e3-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d6e3-119">PARAMETERS</span></span>

### <span data-ttu-id="0d6e3-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="0d6e3-120">-ColumnName</span></span>
<span data-ttu-id="0d6e3-121">A maszkolási szabály által célzott oszlop nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="0d6e3-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0d6e3-122">-DatabaseName</span></span>
<span data-ttu-id="0d6e3-123">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="0d6e3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d6e3-124">-DefaultProfile</span></span>
<span data-ttu-id="0d6e3-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0d6e3-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d6e3-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="0d6e3-126">-MaskingFunction</span></span>
<span data-ttu-id="0d6e3-127">A szabály által használt maszkolás függvényt adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="0d6e3-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0d6e3-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0d6e3-129">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="0d6e3-129">Default</span></span>
- <span data-ttu-id="0d6e3-130">A kitakarás</span><span class="sxs-lookup"><span data-stu-id="0d6e3-130">NoMasking</span></span>
- <span data-ttu-id="0d6e3-131">Szöveg</span><span class="sxs-lookup"><span data-stu-id="0d6e3-131">Text</span></span>
- <span data-ttu-id="0d6e3-132">Szám</span><span class="sxs-lookup"><span data-stu-id="0d6e3-132">Number</span></span>
- <span data-ttu-id="0d6e3-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="0d6e3-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="0d6e3-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="0d6e3-134">CreditCardNumber</span></span>
- <span data-ttu-id="0d6e3-135">E-mail: az alapértelmezett érték az alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-135">Email The default value is Default.</span></span>

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

### <span data-ttu-id="0d6e3-136">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="0d6e3-136">-NumberFrom</span></span>
<span data-ttu-id="0d6e3-137">Annak az intervallumnak az alsó határát adja meg, amelyből egy véletlenszerű érték van kijelölve.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="0d6e3-138">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="0d6e3-139">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-139">The default value is 0.</span></span>

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

### <span data-ttu-id="0d6e3-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="0d6e3-140">-NumberTo</span></span>
<span data-ttu-id="0d6e3-141">Annak az intervallumnak a felső határát adja meg, amelyből egy véletlenszerű érték van kijelölve.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="0d6e3-142">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="0d6e3-143">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-143">The default value is 0.</span></span>

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

### <span data-ttu-id="0d6e3-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d6e3-144">-PassThru</span></span>
<span data-ttu-id="0d6e3-145">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0d6e3-146">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d6e3-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="0d6e3-147">-PrefixSize</span></span>
<span data-ttu-id="0d6e3-148">Itt adhatja meg, hogy a program hány karaktert tartalmaz a nem maszkolt szöveg elején.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="0d6e3-149">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="0d6e3-150">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-150">The default value is 0.</span></span>

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

### <span data-ttu-id="0d6e3-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="0d6e3-151">-ReplacementString</span></span>
<span data-ttu-id="0d6e3-152">Itt adhatja meg, hogy a program hány karaktert tartalmaz a nem maszkolt szöveg végén.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-152">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="0d6e3-153">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="0d6e3-154">Az alapértelmezett érték egy üres karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-154">The default value is an empty string.</span></span>

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

### <span data-ttu-id="0d6e3-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d6e3-155">-ResourceGroupName</span></span>
<span data-ttu-id="0d6e3-156">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0d6e3-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0d6e3-157">-SchemaName</span></span>
<span data-ttu-id="0d6e3-158">A séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="0d6e3-159">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0d6e3-159">-ServerName</span></span>
<span data-ttu-id="0d6e3-160">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="0d6e3-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="0d6e3-161">-SuffixSize</span></span>
<span data-ttu-id="0d6e3-162">A nem maszkolt szöveg végén található karakterek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="0d6e3-163">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="0d6e3-164">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-164">The default value is 0.</span></span>

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

### <span data-ttu-id="0d6e3-165">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="0d6e3-165">-TableName</span></span>
<span data-ttu-id="0d6e3-166">A maszkolt oszlopot tartalmazó adatbázis-tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="0d6e3-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0d6e3-167">-Confirm</span></span>
<span data-ttu-id="0d6e3-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d6e3-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d6e3-169">-WhatIf</span></span>
<span data-ttu-id="0d6e3-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d6e3-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d6e3-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d6e3-172">CommonParameters</span></span>
<span data-ttu-id="0d6e3-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d6e3-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d6e3-174">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0d6e3-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d6e3-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d6e3-175">INPUTS</span></span>

### <span data-ttu-id="0d6e3-176">System. String</span><span class="sxs-lookup"><span data-stu-id="0d6e3-176">System.String</span></span>

### <span data-ttu-id="0d6e3-177">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0d6e3-177">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0d6e3-178">System. null ' 1 [[System. Double, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0d6e3-178">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0d6e3-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d6e3-179">OUTPUTS</span></span>

### <span data-ttu-id="0d6e3-180">Microsoft. Azure. Command. SQL. DataMasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="0d6e3-180">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="0d6e3-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d6e3-181">NOTES</span></span>

## <span data-ttu-id="0d6e3-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d6e3-182">RELATED LINKS</span></span>

[<span data-ttu-id="0d6e3-183">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0d6e3-183">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0d6e3-184">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0d6e3-184">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0d6e3-185">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0d6e3-185">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0d6e3-186">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0d6e3-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


