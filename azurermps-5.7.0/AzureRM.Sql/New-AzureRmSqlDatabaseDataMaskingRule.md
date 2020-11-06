---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: b53b32b30e1b69da94ac8319ed3a5f4eee7ffc0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492128"
---
# <span data-ttu-id="2c49e-101">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2c49e-101">New-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="2c49e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c49e-102">SYNOPSIS</span></span>
<span data-ttu-id="2c49e-103">Adatmaszkolási szabályt hoz létre egy adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="2c49e-103">Creates a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c49e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c49e-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c49e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c49e-105">DESCRIPTION</span></span>
<span data-ttu-id="2c49e-106">A **New-AzureRmSqlDatabaseDataMaskingRule** parancsmag adatmaszkolási szabályt hoz létre egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="2c49e-106">The **New-AzureRmSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="2c49e-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* , a *databasename* és a *RuleId* paraméterrel keresse meg a szabályt.</span><span class="sxs-lookup"><span data-stu-id="2c49e-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="2c49e-108">Adja meg a *Táblanév* és a *ColumnName* a szabály céljának és a *MaskingFunction* paraméternek az adatainak maszkolási módjának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="2c49e-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>

<span data-ttu-id="2c49e-109">Ha a *MaskingFunction* szám vagy szöveg van megadva, megadhatja a *NumberFrom* és az *NumberTo* paramétert, a szám maszkolását, valamint a *PrefixSize* , a *ReplacementString* és a *SuffixSize* a szöveg maszkolásához.</span><span class="sxs-lookup"><span data-stu-id="2c49e-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>

<span data-ttu-id="2c49e-110">Ha a parancs sikeres, és a *PassThru* paramétert használja, a parancsmag egy olyan objektumot ad eredményül, amely leírja az adatmaszkolási szabály tulajdonságait a szabály-azonosítók mellett.</span><span class="sxs-lookup"><span data-stu-id="2c49e-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="2c49e-111">A *ResourceGroupName* , a *kiszolgálónév* , a *databasename* és a *RuleID* nem csak a szabály-azonosítókat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="2c49e-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>

<span data-ttu-id="2c49e-112">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="2c49e-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2c49e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="2c49e-113">EXAMPLES</span></span>

### <span data-ttu-id="2c49e-114">Példa 1: adatmaszkolási szabály létrehozása egy adatbázis szám oszlopához</span><span class="sxs-lookup"><span data-stu-id="2c49e-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="2c49e-115">Ez a parancs létrehoz egy adatmaszkolási szabályt a Column01 nevű oszlophoz a Schema01 nevű Table01 nevű táblázatban.</span><span class="sxs-lookup"><span data-stu-id="2c49e-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="2c49e-116">A Database01 nevű adatbázis az összes elemet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2c49e-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="2c49e-117">A szabály egy olyan számozási szabály, amely 5 és 14 közötti véletlenszerű számot használ a maszk értékeként.</span><span class="sxs-lookup"><span data-stu-id="2c49e-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="2c49e-118">A szabály neve Rule01.</span><span class="sxs-lookup"><span data-stu-id="2c49e-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="2c49e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c49e-119">PARAMETERS</span></span>

### <span data-ttu-id="2c49e-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="2c49e-120">-ColumnName</span></span>
<span data-ttu-id="2c49e-121">A maszkolási szabály által célzott oszlop nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c49e-121">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c49e-122">-DatabaseName</span></span>
<span data-ttu-id="2c49e-123">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c49e-123">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c49e-124">-DefaultProfile</span></span>
<span data-ttu-id="2c49e-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2c49e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="2c49e-126">-MaskingFunction</span></span>
<span data-ttu-id="2c49e-127">A szabály által használt maszkolás függvényt adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c49e-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="2c49e-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2c49e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2c49e-129">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="2c49e-129">Default</span></span>
- <span data-ttu-id="2c49e-130">A kitakarás</span><span class="sxs-lookup"><span data-stu-id="2c49e-130">NoMasking</span></span>
- <span data-ttu-id="2c49e-131">Szöveg</span><span class="sxs-lookup"><span data-stu-id="2c49e-131">Text</span></span>
- <span data-ttu-id="2c49e-132">Szám</span><span class="sxs-lookup"><span data-stu-id="2c49e-132">Number</span></span>
- <span data-ttu-id="2c49e-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="2c49e-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="2c49e-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="2c49e-134">CreditCardNumber</span></span>
- <span data-ttu-id="2c49e-135">E-mail</span><span class="sxs-lookup"><span data-stu-id="2c49e-135">Email</span></span>

<span data-ttu-id="2c49e-136">Az alapértelmezett érték az alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="2c49e-136">The default value is Default.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="2c49e-137">-NumberFrom</span></span>
<span data-ttu-id="2c49e-138">Annak az intervallumnak az alsó határát adja meg, amelyből egy véletlenszerű érték van kijelölve.</span><span class="sxs-lookup"><span data-stu-id="2c49e-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="2c49e-139">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.</span><span class="sxs-lookup"><span data-stu-id="2c49e-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2c49e-140">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="2c49e-140">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="2c49e-141">-NumberTo</span></span>
<span data-ttu-id="2c49e-142">Annak az intervallumnak a felső határát adja meg, amelyből egy véletlenszerű érték van kijelölve.</span><span class="sxs-lookup"><span data-stu-id="2c49e-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="2c49e-143">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.</span><span class="sxs-lookup"><span data-stu-id="2c49e-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2c49e-144">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="2c49e-144">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c49e-145">-PassThru</span></span>
<span data-ttu-id="2c49e-146">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2c49e-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2c49e-147">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2c49e-147">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="2c49e-148">-PrefixSize</span></span>
<span data-ttu-id="2c49e-149">Itt adhatja meg, hogy a program hány karaktert tartalmaz a nem maszkolt szöveg elején.</span><span class="sxs-lookup"><span data-stu-id="2c49e-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="2c49e-150">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="2c49e-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2c49e-151">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="2c49e-151">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="2c49e-152">-ReplacementString</span></span>
<span data-ttu-id="2c49e-153">Itt adhatja meg, hogy a program hány karaktert tartalmaz a nem maszkolt szöveg végén.</span><span class="sxs-lookup"><span data-stu-id="2c49e-153">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="2c49e-154">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="2c49e-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2c49e-155">Az alapértelmezett érték egy üres karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="2c49e-155">The default value is an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c49e-156">-ResourceGroupName</span></span>
<span data-ttu-id="2c49e-157">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="2c49e-157">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="2c49e-158">-SchemaName</span></span>
<span data-ttu-id="2c49e-159">A séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c49e-159">Specifies the name of a schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-160">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2c49e-160">-ServerName</span></span>
<span data-ttu-id="2c49e-161">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c49e-161">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="2c49e-162">-SuffixSize</span></span>
<span data-ttu-id="2c49e-163">A nem maszkolt szöveg végén található karakterek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c49e-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="2c49e-164">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="2c49e-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2c49e-165">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="2c49e-165">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-166">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="2c49e-166">-TableName</span></span>
<span data-ttu-id="2c49e-167">A maszkolt oszlopot tartalmazó adatbázis-tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c49e-167">Specifies the name of the database table that contains the masked column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c49e-168">-Confirm</span></span>
<span data-ttu-id="2c49e-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c49e-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c49e-170">-WhatIf</span></span>
<span data-ttu-id="2c49e-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c49e-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c49e-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c49e-172">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c49e-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c49e-173">CommonParameters</span></span>
<span data-ttu-id="2c49e-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c49e-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c49e-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c49e-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c49e-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c49e-176">INPUTS</span></span>

###  
<span data-ttu-id="2c49e-177">Nincs.</span><span class="sxs-lookup"><span data-stu-id="2c49e-177">None.</span></span>

## <span data-ttu-id="2c49e-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c49e-178">OUTPUTS</span></span>

### <span data-ttu-id="2c49e-179">Microsoft. Azure. Command. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="2c49e-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="2c49e-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c49e-180">NOTES</span></span>

## <span data-ttu-id="2c49e-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c49e-181">RELATED LINKS</span></span>

[<span data-ttu-id="2c49e-182">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2c49e-182">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2c49e-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2c49e-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2c49e-184">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2c49e-184">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2c49e-185">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="2c49e-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


