---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 72ee99f3d62470c4a3a62719006152a5f52cd8d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466821"
---
# <span data-ttu-id="91323-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="91323-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="91323-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91323-102">SYNOPSIS</span></span>
<span data-ttu-id="91323-103">Letiltja (mellőzi) a bizalmasságra vonatkozó javaslatokat az SQL-készlet oszlopainál.</span><span class="sxs-lookup"><span data-stu-id="91323-103">Disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="91323-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="91323-104">SYNTAX</span></span>

### <span data-ttu-id="91323-105">InputObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91323-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91323-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="91323-106">ColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91323-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="91323-107">SqlPoolObjectColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91323-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="91323-108">DESCRIPTION</span></span>
<span data-ttu-id="91323-109">A Disable-AzSynapseSqlPoolSensitivityRecommendation parancsmag letiltja (mellőzi) a bizalmasságra vonatkozó javaslatokat az SQL-készlet oszlopainál.</span><span class="sxs-lookup"><span data-stu-id="91323-109">The Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="91323-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="91323-110">EXAMPLES</span></span>

### <span data-ttu-id="91323-111">1. példa: Tartalomra vonatkozó javaslatok letiltása egy Azure Synapse SQL-készlet adott oszlopában.</span><span class="sxs-lookup"><span data-stu-id="91323-111">Example 1: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="91323-112">2. példa: Tiltsa le a bizalmasság-javaslatokat olyan oszlopokban, amelyek bizalmasságra vonatkozó javaslatokat tartalmaznak egy Azure Synapse SQL-készletben a Piping használatával.</span><span class="sxs-lookup"><span data-stu-id="91323-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation
```

### <span data-ttu-id="91323-113">3. példa: Tiltsa le a bizalmasság-javaslatokat egy Azure Synapse SQL-készlet adott oszlopában a Piping használatával.</span><span class="sxs-lookup"><span data-stu-id="91323-113">Example 3: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="91323-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91323-114">PARAMETERS</span></span>

### <span data-ttu-id="91323-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91323-115">-AsJob</span></span>
<span data-ttu-id="91323-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="91323-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91323-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="91323-117">-ColumnName</span></span>
<span data-ttu-id="91323-118">Az oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="91323-118">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91323-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91323-119">-DefaultProfile</span></span>
<span data-ttu-id="91323-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91323-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91323-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91323-121">-InputObject</span></span>
<span data-ttu-id="91323-122">Egy SQL-készlet bizalmasság-besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="91323-122">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91323-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91323-123">-PassThru</span></span>
<span data-ttu-id="91323-124">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="91323-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="91323-125">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="91323-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="91323-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91323-126">-ResourceGroupName</span></span>
<span data-ttu-id="91323-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="91323-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91323-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="91323-128">-SchemaName</span></span>
<span data-ttu-id="91323-129">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="91323-129">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91323-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="91323-130">-SqlPoolName</span></span>
<span data-ttu-id="91323-131">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="91323-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91323-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="91323-132">-SqlPoolObject</span></span>
<span data-ttu-id="91323-133">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="91323-133">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91323-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="91323-134">-TableName</span></span>
<span data-ttu-id="91323-135">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="91323-135">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91323-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="91323-136">-WorkspaceName</span></span>
<span data-ttu-id="91323-137">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="91323-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91323-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91323-138">-Confirm</span></span>
<span data-ttu-id="91323-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="91323-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91323-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91323-140">-WhatIf</span></span>
<span data-ttu-id="91323-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="91323-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91323-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91323-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91323-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91323-143">CommonParameters</span></span>
<span data-ttu-id="91323-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91323-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91323-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91323-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91323-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91323-146">INPUTS</span></span>

### <span data-ttu-id="91323-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="91323-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="91323-148">System.String</span><span class="sxs-lookup"><span data-stu-id="91323-148">System.String</span></span>

### <span data-ttu-id="91323-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="91323-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="91323-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91323-150">OUTPUTS</span></span>

### <span data-ttu-id="91323-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="91323-151">System.Boolean</span></span>

## <span data-ttu-id="91323-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="91323-152">NOTES</span></span>

## <span data-ttu-id="91323-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91323-153">RELATED LINKS</span></span>
