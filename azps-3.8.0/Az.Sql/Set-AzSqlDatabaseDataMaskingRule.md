---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 10afb514284fb3083110c068b33ffd189afd4039
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846638"
---
# <span data-ttu-id="78161-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="78161-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="78161-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78161-102">SYNOPSIS</span></span>
<span data-ttu-id="78161-103">Egy adatbázis adatmaszkolási szabályának tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="78161-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="78161-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78161-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78161-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="78161-105">DESCRIPTION</span></span>
<span data-ttu-id="78161-106">A **set-AzSqlDatabaseDataMaskingRule** parancsmag adatmaszkolási szabályt állít be egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="78161-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="78161-107">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* , a *databasename* és az *RuleId* paramétert a szabály meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="78161-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="78161-108">A *SchemaName* , az *Táblanév* és a *ColumnName* bármelyik paraméterét megadhatja a szabály átcélzásához.</span><span class="sxs-lookup"><span data-stu-id="78161-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="78161-109">Adja meg a *MaskingFunction* paramétert az adatmaszkolás módjának módosításához.</span><span class="sxs-lookup"><span data-stu-id="78161-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="78161-110">Ha megad egy szám vagy szöveg értékét a *MaskingFunction* , megadhatja a *NumberFrom* és az *NumberTo* paramétert a szám maszkolásához, illetve a szöveg maszkolásához használt *PrefixSize* , *ReplacementString* és *SuffixSize* paramétereket.</span><span class="sxs-lookup"><span data-stu-id="78161-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="78161-111">Ha a parancs sikeres, és ha a *PassThru* paramétert adja meg, a parancsmag egy olyan objektumot ad eredményül, amely leírja az adatmaszkolási szabály tulajdonságait és a szabályok azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="78161-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="78161-112">A **ResourceGroupName** , a **kiszolgálónév** , a **databasename** és a **RuleId** nem csak a szabály-azonosítókat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="78161-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="78161-113">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="78161-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="78161-114">Példák</span><span class="sxs-lookup"><span data-stu-id="78161-114">EXAMPLES</span></span>

### <span data-ttu-id="78161-115">Példa 1: adatmaszkolási szabály tartományának módosítása az adatbázisban</span><span class="sxs-lookup"><span data-stu-id="78161-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="78161-116">Ez a parancs módosítja az adatmaszkolási szabályokat az azonosító Rule17.</span><span class="sxs-lookup"><span data-stu-id="78161-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="78161-117">Ez a szabály a kiszolgáló Server01 Database01 nevű adatbázisban működik.</span><span class="sxs-lookup"><span data-stu-id="78161-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="78161-118">Ez a parancs módosítja annak az intervallumnak a szegélyét, amelyben a véletlenszerűen kiválasztott szám a maszkolt érték lesz.</span><span class="sxs-lookup"><span data-stu-id="78161-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="78161-119">Az új címtartomány 23 és 42 között van.</span><span class="sxs-lookup"><span data-stu-id="78161-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="78161-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78161-120">PARAMETERS</span></span>

### <span data-ttu-id="78161-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="78161-121">-ColumnName</span></span>
<span data-ttu-id="78161-122">A maszkolási szabály által célzott oszlop nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78161-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="78161-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="78161-123">-DatabaseName</span></span>
<span data-ttu-id="78161-124">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78161-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="78161-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78161-125">-DefaultProfile</span></span>
<span data-ttu-id="78161-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="78161-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78161-127">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="78161-127">-MaskingFunction</span></span>
<span data-ttu-id="78161-128">A szabály által használt maszkolás függvényt adja meg.</span><span class="sxs-lookup"><span data-stu-id="78161-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="78161-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="78161-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="78161-130">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="78161-130">Default</span></span>
- <span data-ttu-id="78161-131">A kitakarás</span><span class="sxs-lookup"><span data-stu-id="78161-131">NoMasking</span></span>
- <span data-ttu-id="78161-132">Szöveg</span><span class="sxs-lookup"><span data-stu-id="78161-132">Text</span></span>
- <span data-ttu-id="78161-133">Szám</span><span class="sxs-lookup"><span data-stu-id="78161-133">Number</span></span>
- <span data-ttu-id="78161-134">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="78161-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="78161-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="78161-135">CreditCardNumber</span></span>
- <span data-ttu-id="78161-136">E-mail: az alapértelmezett érték az alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="78161-136">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78161-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="78161-137">-NumberFrom</span></span>
<span data-ttu-id="78161-138">Annak az intervallumnak az alsó határát adja meg, amelyből egy véletlenszerű érték van kijelölve.</span><span class="sxs-lookup"><span data-stu-id="78161-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="78161-139">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.</span><span class="sxs-lookup"><span data-stu-id="78161-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="78161-140">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="78161-140">The default value is 0.</span></span>

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

### <span data-ttu-id="78161-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="78161-141">-NumberTo</span></span>
<span data-ttu-id="78161-142">Annak az intervallumnak a felső határát adja meg, amelyből egy véletlenszerű érték van kijelölve.</span><span class="sxs-lookup"><span data-stu-id="78161-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="78161-143">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.</span><span class="sxs-lookup"><span data-stu-id="78161-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="78161-144">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="78161-144">The default value is 0.</span></span>

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

### <span data-ttu-id="78161-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78161-145">-PassThru</span></span>
<span data-ttu-id="78161-146">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="78161-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78161-147">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="78161-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="78161-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="78161-148">-PrefixSize</span></span>
<span data-ttu-id="78161-149">Itt adhatja meg, hogy a program hány karaktert tartalmaz a nem maszkolt szöveg elején.</span><span class="sxs-lookup"><span data-stu-id="78161-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="78161-150">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="78161-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="78161-151">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="78161-151">The default value is 0.</span></span>

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

### <span data-ttu-id="78161-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="78161-152">-ReplacementString</span></span>
<span data-ttu-id="78161-153">A nem maszkolt szöveg végén található karakterek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="78161-153">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="78161-154">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="78161-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="78161-155">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="78161-155">The default value is 0.</span></span>

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

### <span data-ttu-id="78161-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78161-156">-ResourceGroupName</span></span>
<span data-ttu-id="78161-157">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="78161-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="78161-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="78161-158">-SchemaName</span></span>
<span data-ttu-id="78161-159">A séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78161-159">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="78161-160">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="78161-160">-ServerName</span></span>
<span data-ttu-id="78161-161">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78161-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="78161-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="78161-162">-SuffixSize</span></span>
<span data-ttu-id="78161-163">A nem maszkolt szöveg végén található karakterek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="78161-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="78161-164">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="78161-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="78161-165">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="78161-165">The default value is 0.</span></span>

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

### <span data-ttu-id="78161-166">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="78161-166">-TableName</span></span>
<span data-ttu-id="78161-167">A maszkolt oszlopot tartalmazó adatbázis-tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78161-167">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="78161-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="78161-168">-Confirm</span></span>
<span data-ttu-id="78161-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78161-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78161-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78161-170">-WhatIf</span></span>
<span data-ttu-id="78161-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="78161-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78161-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78161-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78161-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78161-173">CommonParameters</span></span>
<span data-ttu-id="78161-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78161-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78161-175">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="78161-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78161-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78161-176">INPUTS</span></span>

### <span data-ttu-id="78161-177">System. String</span><span class="sxs-lookup"><span data-stu-id="78161-177">System.String</span></span>

### <span data-ttu-id="78161-178">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="78161-178">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="78161-179">System. null ' 1 [[System. Double, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="78161-179">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="78161-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78161-180">OUTPUTS</span></span>

### <span data-ttu-id="78161-181">Microsoft. Azure. Command. SQL. DataMasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="78161-181">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="78161-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78161-182">NOTES</span></span>

## <span data-ttu-id="78161-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78161-183">RELATED LINKS</span></span>

[<span data-ttu-id="78161-184">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="78161-184">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="78161-185">Új – AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="78161-185">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="78161-186">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="78161-186">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="78161-187">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="78161-187">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


