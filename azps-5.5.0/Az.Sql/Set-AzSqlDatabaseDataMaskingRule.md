---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155242"
---
# <span data-ttu-id="4e49b-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4e49b-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="4e49b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e49b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e49b-103">Beállítja egy adatbázis adatmaszkolási szabályának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="4e49b-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="4e49b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4e49b-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e49b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4e49b-105">DESCRIPTION</span></span>
<span data-ttu-id="4e49b-106">A **Set-AzSqlDatabaseDataMaskingRule** parancsmag adatmaszkolási szabályt állít be egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="4e49b-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="4e49b-107">A parancsmag használhatja a *ResourceGroupName,* *a ServerName,* a *DatabaseName* és a *RuleId* paramétert a szabály azonosításához.</span><span class="sxs-lookup"><span data-stu-id="4e49b-107">To use the cmdlet, provide the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="4e49b-108">A szabály újra megcélzásához meg kell adnia a *SchemaName,* *a TableName* és az *ColumnName* paraméter bármelyik paraméterét.</span><span class="sxs-lookup"><span data-stu-id="4e49b-108">You can provide any of the parameters of *SchemaName*, *TableName*, and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="4e49b-109">Adja meg *a MaskingFunction paramétert* az adatok maszkolásának módosításához.</span><span class="sxs-lookup"><span data-stu-id="4e49b-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="4e49b-110">Ha a *MaskingFunction* paraméterhez számértéket vagy szövegértéket ad meg, megadhatja a *NumberFrom* és a *NumberTo* paramétert a számmaszkoláshoz, illetve az *Előtagszi,* a *CsereString* és az *Utótagszize paramétert* a szövegmaszkoláshoz.</span><span class="sxs-lookup"><span data-stu-id="4e49b-110">If you specify a value of Number or Text for *MaskingFunction*, you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize*, *ReplacementString*, and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="4e49b-111">Ha a parancs sikerrel jár, és megadja a *PassThru* paramétert, a parancsmag egy objektumot ad vissza, amely ismerteti a szabálytulajdonságokat és a szabályazonosítókat.</span><span class="sxs-lookup"><span data-stu-id="4e49b-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="4e49b-112">A szabályazonosítók közé tartozik többek között a **ResourceGroupName,** **a ServerName,** a **DatabaseName** és a **RuleId.**</span><span class="sxs-lookup"><span data-stu-id="4e49b-112">Rule identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, **DatabaseName**, and **RuleId**.</span></span>
<span data-ttu-id="4e49b-113">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="4e49b-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4e49b-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4e49b-114">EXAMPLES</span></span>

### <span data-ttu-id="4e49b-115">1. példa: Adatbázis adatmaszkolási szabály tartományának módosítása</span><span class="sxs-lookup"><span data-stu-id="4e49b-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="4e49b-116">Ez a parancs módosít egy olyan adatmaszkoló szabályt, amely az azonosítószabály17-et is tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="4e49b-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="4e49b-117">Ez a szabály a Server Server01 kiszolgálón található Database01 nevű adatbázisban működik.</span><span class="sxs-lookup"><span data-stu-id="4e49b-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="4e49b-118">Ez a parancs módosítja annak az intervallumnak a határait, amelyben a program maszkolt értékként véletlenszerű számot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4e49b-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="4e49b-119">Az új tartomány 23 és 42 között van.</span><span class="sxs-lookup"><span data-stu-id="4e49b-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="4e49b-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="4e49b-120">Example 2</span></span>

<span data-ttu-id="4e49b-121">Beállítja egy adatbázis adatmaszkolási szabályának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="4e49b-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="4e49b-122">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="4e49b-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="4e49b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e49b-123">PARAMETERS</span></span>

### <span data-ttu-id="4e49b-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="4e49b-124">-ColumnName</span></span>
<span data-ttu-id="4e49b-125">A maszkolási szabály által megcélzott oszlop nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="4e49b-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e49b-126">-DatabaseName</span></span>
<span data-ttu-id="4e49b-127">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="4e49b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e49b-128">-DefaultProfile</span></span>
<span data-ttu-id="4e49b-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4e49b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e49b-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="4e49b-130">-MaskingFunction</span></span>
<span data-ttu-id="4e49b-131">Megadja a szabály által használt maszkolási függvényt.</span><span class="sxs-lookup"><span data-stu-id="4e49b-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="4e49b-132">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="4e49b-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e49b-133">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="4e49b-133">Default</span></span>
- <span data-ttu-id="4e49b-134">NoMasking</span><span class="sxs-lookup"><span data-stu-id="4e49b-134">NoMasking</span></span>
- <span data-ttu-id="4e49b-135">Szöveg</span><span class="sxs-lookup"><span data-stu-id="4e49b-135">Text</span></span>
- <span data-ttu-id="4e49b-136">Szám</span><span class="sxs-lookup"><span data-stu-id="4e49b-136">Number</span></span>
- <span data-ttu-id="4e49b-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="4e49b-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="4e49b-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="4e49b-138">CreditCardNumber</span></span>
- <span data-ttu-id="4e49b-139">E-mail: Az alapértelmezett érték az Alapértelmezett.</span><span class="sxs-lookup"><span data-stu-id="4e49b-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="4e49b-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="4e49b-140">-NumberFrom</span></span>
<span data-ttu-id="4e49b-141">Annak az intervallumnak az alsó határa, amelyből véletlenszerű értéket választ ki.</span><span class="sxs-lookup"><span data-stu-id="4e49b-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="4e49b-142">Ezt a paramétert csak akkor adja meg, ha a *MaskingFunction paraméterhez számértéket ad* meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="4e49b-143">Az alapértelmezett érték 0.</span><span class="sxs-lookup"><span data-stu-id="4e49b-143">The default value is 0.</span></span>

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

### <span data-ttu-id="4e49b-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="4e49b-144">-NumberTo</span></span>
<span data-ttu-id="4e49b-145">Annak az intervallumnak a felső határa, amelyből véletlenszerű értéket választ ki.</span><span class="sxs-lookup"><span data-stu-id="4e49b-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="4e49b-146">Ezt a paramétert csak akkor adja meg, ha a *MaskingFunction paraméterhez számértéket ad* meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="4e49b-147">Az alapértelmezett érték 0.</span><span class="sxs-lookup"><span data-stu-id="4e49b-147">The default value is 0.</span></span>

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

### <span data-ttu-id="4e49b-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e49b-148">-PassThru</span></span>
<span data-ttu-id="4e49b-149">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="4e49b-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4e49b-150">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4e49b-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4e49b-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="4e49b-151">-PrefixSize</span></span>
<span data-ttu-id="4e49b-152">A nem maszkolt szöveg elején szereplő karakterek számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="4e49b-153">Ezt a paramétert csak akkor adja meg, ha a *MaskingFunction paraméterhez szövegértéket ad* meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="4e49b-154">Az alapértelmezett érték 0.</span><span class="sxs-lookup"><span data-stu-id="4e49b-154">The default value is 0.</span></span>

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

### <span data-ttu-id="4e49b-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="4e49b-155">-ReplacementString</span></span>
<span data-ttu-id="4e49b-156">A nem maszkolt szöveg végének karakterszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="4e49b-157">Ezt a paramétert csak akkor adja meg, ha a *MaskingFunction paraméterhez szövegértéket ad* meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="4e49b-158">Az alapértelmezett érték 0.</span><span class="sxs-lookup"><span data-stu-id="4e49b-158">The default value is 0.</span></span>

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

### <span data-ttu-id="4e49b-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e49b-159">-ResourceGroupName</span></span>
<span data-ttu-id="4e49b-160">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="4e49b-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4e49b-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4e49b-161">-SchemaName</span></span>
<span data-ttu-id="4e49b-162">Egy séma nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="4e49b-163">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4e49b-163">-ServerName</span></span>
<span data-ttu-id="4e49b-164">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4e49b-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="4e49b-165">-SuffixSize</span></span>
<span data-ttu-id="4e49b-166">A nem maszkolt szöveg végének karakterszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="4e49b-167">Ezt a paramétert csak akkor adja meg, ha a *MaskingFunction paraméterhez szövegértéket ad* meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="4e49b-168">Az alapértelmezett érték 0.</span><span class="sxs-lookup"><span data-stu-id="4e49b-168">The default value is 0.</span></span>

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

### <span data-ttu-id="4e49b-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="4e49b-169">-TableName</span></span>
<span data-ttu-id="4e49b-170">A maszkos oszlopot tartalmazó adatbázistábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e49b-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="4e49b-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e49b-171">-Confirm</span></span>
<span data-ttu-id="4e49b-172">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4e49b-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e49b-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e49b-173">-WhatIf</span></span>
<span data-ttu-id="4e49b-174">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4e49b-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e49b-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e49b-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e49b-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e49b-176">CommonParameters</span></span>
<span data-ttu-id="4e49b-177">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e49b-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e49b-178">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e49b-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e49b-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e49b-179">INPUTS</span></span>

### <span data-ttu-id="4e49b-180">System.String</span><span class="sxs-lookup"><span data-stu-id="4e49b-180">System.String</span></span>

### <span data-ttu-id="4e49b-181">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4e49b-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4e49b-182">System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4e49b-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4e49b-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e49b-183">OUTPUTS</span></span>

### <span data-ttu-id="4e49b-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="4e49b-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="4e49b-185">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4e49b-185">NOTES</span></span>

## <span data-ttu-id="4e49b-186">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e49b-186">RELATED LINKS</span></span>

[<span data-ttu-id="4e49b-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4e49b-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="4e49b-188">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4e49b-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="4e49b-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4e49b-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="4e49b-190">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4e49b-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


