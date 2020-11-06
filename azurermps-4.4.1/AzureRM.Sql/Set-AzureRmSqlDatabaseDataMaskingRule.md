---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 1a26cc83bfd42ba63f2ae914ea6c288b862ccaf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493314"
---
# <span data-ttu-id="f6f3a-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f6f3a-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="f6f3a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f3a-103">Egy adatbázis adatmaszkolási szabályának tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6f3a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6f3a-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6f3a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="f6f3a-106">A **set-AzureRmSqlDatabaseDataMaskingRule** parancsmag adatmaszkolási szabályt állít be egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="f6f3a-107">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* , a *databasename* és az *RuleId* paramétert a szabály meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="f6f3a-108">A *SchemaName* , az *Táblanév* és a *ColumnName* bármelyik paraméterét megadhatja a szabály átcélzásához.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="f6f3a-109">Adja meg a *MaskingFunction* paramétert az adatmaszkolás módjának módosításához.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>

<span data-ttu-id="f6f3a-110">Ha megad egy szám vagy szöveg értékét a *MaskingFunction* , megadhatja a *NumberFrom* és az *NumberTo* paramétert a szám maszkolásához, illetve a szöveg maszkolásához használt *PrefixSize* , *ReplacementString* és *SuffixSize* paramétereket.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="f6f3a-111">Ha a parancs sikeres, és ha a *PassThru* paramétert adja meg, a parancsmag egy olyan objektumot ad eredményül, amely leírja az adatmaszkolási szabály tulajdonságait és a szabályok azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="f6f3a-112">A **ResourceGroupName** , a **kiszolgálónév** , a **databasename** és a **RuleId** nem csak a szabály-azonosítókat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>

<span data-ttu-id="f6f3a-113">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f6f3a-114">Példák</span><span class="sxs-lookup"><span data-stu-id="f6f3a-114">EXAMPLES</span></span>

### <span data-ttu-id="f6f3a-115">Példa 1: adatmaszkolási szabály tartományának módosítása az adatbázisban</span><span class="sxs-lookup"><span data-stu-id="f6f3a-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="f6f3a-116">Ez a parancs módosítja az adatmaszkolási szabályokat az azonosító Rule17.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="f6f3a-117">Ez a szabály a kiszolgáló Server01 Database01 nevű adatbázisban működik.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="f6f3a-118">Ez a parancs módosítja annak az intervallumnak a szegélyét, amelyben a véletlenszerűen kiválasztott szám a maszkolt érték lesz.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="f6f3a-119">Az új címtartomány 23 és 42 között van.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="f6f3a-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6f3a-120">PARAMETERS</span></span>

### <span data-ttu-id="f6f3a-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="f6f3a-121">-ColumnName</span></span>
<span data-ttu-id="f6f3a-122">A maszkolási szabály által célzott oszlop nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="f6f3a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f6f3a-123">-DatabaseName</span></span>
<span data-ttu-id="f6f3a-124">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="f6f3a-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="f6f3a-125">-MaskingFunction</span></span>
<span data-ttu-id="f6f3a-126">A szabály által használt maszkolás függvényt adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="f6f3a-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f6f3a-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6f3a-128">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="f6f3a-128">Default</span></span>
- <span data-ttu-id="f6f3a-129">A kitakarás</span><span class="sxs-lookup"><span data-stu-id="f6f3a-129">NoMasking</span></span>
- <span data-ttu-id="f6f3a-130">Szöveg</span><span class="sxs-lookup"><span data-stu-id="f6f3a-130">Text</span></span>
- <span data-ttu-id="f6f3a-131">Szám</span><span class="sxs-lookup"><span data-stu-id="f6f3a-131">Number</span></span>
- <span data-ttu-id="f6f3a-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="f6f3a-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="f6f3a-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="f6f3a-133">CreditCardNumber</span></span>
- <span data-ttu-id="f6f3a-134">E-mail</span><span class="sxs-lookup"><span data-stu-id="f6f3a-134">Email</span></span>

<span data-ttu-id="f6f3a-135">Az alapértelmezett érték az alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-135">The default value is Default.</span></span>

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

### <span data-ttu-id="f6f3a-136">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="f6f3a-136">-NumberFrom</span></span>
<span data-ttu-id="f6f3a-137">Annak az intervallumnak az alsó határát adja meg, amelyből egy véletlenszerű érték van kijelölve.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="f6f3a-138">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="f6f3a-139">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-139">The default value is 0.</span></span>

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

### <span data-ttu-id="f6f3a-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="f6f3a-140">-NumberTo</span></span>
<span data-ttu-id="f6f3a-141">Annak az intervallumnak a felső határát adja meg, amelyből egy véletlenszerű érték van kijelölve.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="f6f3a-142">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="f6f3a-143">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-143">The default value is 0.</span></span>

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

### <span data-ttu-id="f6f3a-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6f3a-144">-PassThru</span></span>
<span data-ttu-id="f6f3a-145">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f6f3a-146">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f6f3a-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="f6f3a-147">-PrefixSize</span></span>
<span data-ttu-id="f6f3a-148">Itt adhatja meg, hogy a program hány karaktert tartalmaz a nem maszkolt szöveg elején.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="f6f3a-149">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="f6f3a-150">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-150">The default value is 0.</span></span>

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

### <span data-ttu-id="f6f3a-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="f6f3a-151">-ReplacementString</span></span>
<span data-ttu-id="f6f3a-152">A nem maszkolt szöveg végén található karakterek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-152">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="f6f3a-153">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="f6f3a-154">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-154">The default value is 0.</span></span>

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

### <span data-ttu-id="f6f3a-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6f3a-155">-ResourceGroupName</span></span>
<span data-ttu-id="f6f3a-156">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f6f3a-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f6f3a-157">-SchemaName</span></span>
<span data-ttu-id="f6f3a-158">A séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="f6f3a-159">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f6f3a-159">-ServerName</span></span>
<span data-ttu-id="f6f3a-160">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="f6f3a-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="f6f3a-161">-SuffixSize</span></span>
<span data-ttu-id="f6f3a-162">A nem maszkolt szöveg végén található karakterek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="f6f3a-163">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="f6f3a-164">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-164">The default value is 0.</span></span>

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

### <span data-ttu-id="f6f3a-165">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="f6f3a-165">-TableName</span></span>
<span data-ttu-id="f6f3a-166">A maszkolt oszlopot tartalmazó adatbázis-tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="f6f3a-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6f3a-167">-Confirm</span></span>
<span data-ttu-id="f6f3a-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6f3a-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6f3a-169">-WhatIf</span></span>
<span data-ttu-id="f6f3a-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6f3a-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6f3a-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f3a-172">-DefaultProfile</span></span>
<span data-ttu-id="f6f3a-173">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6f3a-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6f3a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f3a-174">CommonParameters</span></span>
<span data-ttu-id="f6f3a-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6f3a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f3a-176">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6f3a-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f3a-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6f3a-177">INPUTS</span></span>

###  
<span data-ttu-id="f6f3a-178">Nincs</span><span class="sxs-lookup"><span data-stu-id="f6f3a-178">None</span></span>

## <span data-ttu-id="f6f3a-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6f3a-179">OUTPUTS</span></span>

### <span data-ttu-id="f6f3a-180">Microsoft. Azure. Command. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="f6f3a-180">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="f6f3a-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6f3a-181">NOTES</span></span>

## <span data-ttu-id="f6f3a-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6f3a-182">RELATED LINKS</span></span>

[<span data-ttu-id="f6f3a-183">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f6f3a-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f6f3a-184">Új – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f6f3a-184">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f6f3a-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f6f3a-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f6f3a-186">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f6f3a-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


