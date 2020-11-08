---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195497"
---
# <span data-ttu-id="06b6b-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="06b6b-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="06b6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="06b6b-103">Egy adatbázis adatmaszkolási szabályának tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="06b6b-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="06b6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06b6b-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06b6b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06b6b-105">DESCRIPTION</span></span>
<span data-ttu-id="06b6b-106">A **set-AzSqlDatabaseDataMaskingRule** parancsmag adatmaszkolási szabályt állít be egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="06b6b-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="06b6b-107">A parancsmag használatához adja meg a *ResourceGroupName* , a *kiszolgálónév* , a *databasename* és az *RuleId* paramétert a szabály meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="06b6b-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="06b6b-108">A *SchemaName* , az *Táblanév* és a *ColumnName* bármelyik paraméterét megadhatja a szabály átcélzásához.</span><span class="sxs-lookup"><span data-stu-id="06b6b-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="06b6b-109">Adja meg a *MaskingFunction* paramétert az adatmaszkolás módjának módosításához.</span><span class="sxs-lookup"><span data-stu-id="06b6b-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="06b6b-110">Ha megad egy szám vagy szöveg értékét a *MaskingFunction* , megadhatja a *NumberFrom* és az *NumberTo* paramétert a szám maszkolásához, illetve a szöveg maszkolásához használt *PrefixSize* , *ReplacementString* és *SuffixSize* paramétereket.</span><span class="sxs-lookup"><span data-stu-id="06b6b-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="06b6b-111">Ha a parancs sikeres, és ha a *PassThru* paramétert adja meg, a parancsmag egy olyan objektumot ad eredményül, amely leírja az adatmaszkolási szabály tulajdonságait és a szabályok azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="06b6b-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="06b6b-112">A **ResourceGroupName** , a **kiszolgálónév** , a **databasename** és a **RuleId** nem csak a szabály-azonosítókat tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="06b6b-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="06b6b-113">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="06b6b-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="06b6b-114">Példák</span><span class="sxs-lookup"><span data-stu-id="06b6b-114">EXAMPLES</span></span>

### <span data-ttu-id="06b6b-115">Példa 1: adatmaszkolási szabály tartományának módosítása az adatbázisban</span><span class="sxs-lookup"><span data-stu-id="06b6b-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="06b6b-116">Ez a parancs módosítja az adatmaszkolási szabályokat az azonosító Rule17.</span><span class="sxs-lookup"><span data-stu-id="06b6b-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="06b6b-117">Ez a szabály a kiszolgáló Server01 Database01 nevű adatbázisban működik.</span><span class="sxs-lookup"><span data-stu-id="06b6b-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="06b6b-118">Ez a parancs módosítja annak az intervallumnak a szegélyét, amelyben a véletlenszerűen kiválasztott szám a maszkolt érték lesz.</span><span class="sxs-lookup"><span data-stu-id="06b6b-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="06b6b-119">Az új címtartomány 23 és 42 között van.</span><span class="sxs-lookup"><span data-stu-id="06b6b-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="06b6b-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="06b6b-120">Example 2</span></span>

<span data-ttu-id="06b6b-121">Egy adatbázis adatmaszkolási szabályának tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="06b6b-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="06b6b-122">autogenerated</span><span class="sxs-lookup"><span data-stu-id="06b6b-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="06b6b-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06b6b-123">PARAMETERS</span></span>

### <span data-ttu-id="06b6b-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="06b6b-124">-ColumnName</span></span>
<span data-ttu-id="06b6b-125">A maszkolási szabály által célzott oszlop nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06b6b-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="06b6b-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="06b6b-126">-DatabaseName</span></span>
<span data-ttu-id="06b6b-127">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06b6b-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="06b6b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b6b-128">-DefaultProfile</span></span>
<span data-ttu-id="06b6b-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="06b6b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06b6b-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="06b6b-130">-MaskingFunction</span></span>
<span data-ttu-id="06b6b-131">A szabály által használt maszkolás függvényt adja meg.</span><span class="sxs-lookup"><span data-stu-id="06b6b-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="06b6b-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="06b6b-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06b6b-133">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="06b6b-133">Default</span></span>
- <span data-ttu-id="06b6b-134">A kitakarás</span><span class="sxs-lookup"><span data-stu-id="06b6b-134">NoMasking</span></span>
- <span data-ttu-id="06b6b-135">Szöveg</span><span class="sxs-lookup"><span data-stu-id="06b6b-135">Text</span></span>
- <span data-ttu-id="06b6b-136">Szám</span><span class="sxs-lookup"><span data-stu-id="06b6b-136">Number</span></span>
- <span data-ttu-id="06b6b-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="06b6b-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="06b6b-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="06b6b-138">CreditCardNumber</span></span>
- <span data-ttu-id="06b6b-139">E-mail: az alapértelmezett érték az alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="06b6b-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="06b6b-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="06b6b-140">-NumberFrom</span></span>
<span data-ttu-id="06b6b-141">Annak az intervallumnak az alsó határát adja meg, amelyből egy véletlenszerű érték van kijelölve.</span><span class="sxs-lookup"><span data-stu-id="06b6b-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="06b6b-142">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.</span><span class="sxs-lookup"><span data-stu-id="06b6b-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="06b6b-143">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="06b6b-143">The default value is 0.</span></span>

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

### <span data-ttu-id="06b6b-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="06b6b-144">-NumberTo</span></span>
<span data-ttu-id="06b6b-145">Annak az intervallumnak a felső határát adja meg, amelyből egy véletlenszerű érték van kijelölve.</span><span class="sxs-lookup"><span data-stu-id="06b6b-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="06b6b-146">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez megadja a szám értékét.</span><span class="sxs-lookup"><span data-stu-id="06b6b-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="06b6b-147">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="06b6b-147">The default value is 0.</span></span>

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

### <span data-ttu-id="06b6b-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06b6b-148">-PassThru</span></span>
<span data-ttu-id="06b6b-149">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="06b6b-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="06b6b-150">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="06b6b-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06b6b-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="06b6b-151">-PrefixSize</span></span>
<span data-ttu-id="06b6b-152">Itt adhatja meg, hogy a program hány karaktert tartalmaz a nem maszkolt szöveg elején.</span><span class="sxs-lookup"><span data-stu-id="06b6b-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="06b6b-153">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="06b6b-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="06b6b-154">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="06b6b-154">The default value is 0.</span></span>

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

### <span data-ttu-id="06b6b-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="06b6b-155">-ReplacementString</span></span>
<span data-ttu-id="06b6b-156">A nem maszkolt szöveg végén található karakterek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="06b6b-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="06b6b-157">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="06b6b-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="06b6b-158">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="06b6b-158">The default value is 0.</span></span>

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

### <span data-ttu-id="06b6b-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b6b-159">-ResourceGroupName</span></span>
<span data-ttu-id="06b6b-160">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="06b6b-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="06b6b-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="06b6b-161">-SchemaName</span></span>
<span data-ttu-id="06b6b-162">A séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06b6b-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="06b6b-163">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="06b6b-163">-ServerName</span></span>
<span data-ttu-id="06b6b-164">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06b6b-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="06b6b-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="06b6b-165">-SuffixSize</span></span>
<span data-ttu-id="06b6b-166">A nem maszkolt szöveg végén található karakterek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="06b6b-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="06b6b-167">Csak akkor adja meg ezt a paramétert, ha a *MaskingFunction* paraméterhez adja meg a szöveg értékét.</span><span class="sxs-lookup"><span data-stu-id="06b6b-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="06b6b-168">Az alapértelmezett érték a 0.</span><span class="sxs-lookup"><span data-stu-id="06b6b-168">The default value is 0.</span></span>

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

### <span data-ttu-id="06b6b-169">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="06b6b-169">-TableName</span></span>
<span data-ttu-id="06b6b-170">A maszkolt oszlopot tartalmazó adatbázis-tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06b6b-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="06b6b-171">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06b6b-171">-Confirm</span></span>
<span data-ttu-id="06b6b-172">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06b6b-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06b6b-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b6b-173">-WhatIf</span></span>
<span data-ttu-id="06b6b-174">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06b6b-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b6b-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06b6b-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06b6b-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b6b-176">CommonParameters</span></span>
<span data-ttu-id="06b6b-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06b6b-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b6b-178">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="06b6b-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b6b-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06b6b-179">INPUTS</span></span>

### <span data-ttu-id="06b6b-180">System. String</span><span class="sxs-lookup"><span data-stu-id="06b6b-180">System.String</span></span>

### <span data-ttu-id="06b6b-181">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="06b6b-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="06b6b-182">System. null ' 1 [[System. Double, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="06b6b-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="06b6b-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06b6b-183">OUTPUTS</span></span>

### <span data-ttu-id="06b6b-184">Microsoft. Azure. Command. SQL. DataMasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="06b6b-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="06b6b-185">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06b6b-185">NOTES</span></span>

## <span data-ttu-id="06b6b-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06b6b-186">RELATED LINKS</span></span>

[<span data-ttu-id="06b6b-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="06b6b-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="06b6b-188">Új – AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="06b6b-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="06b6b-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="06b6b-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="06b6b-190">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="06b6b-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


