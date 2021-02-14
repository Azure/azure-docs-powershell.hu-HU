---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: bb47d791f23df044e5a4677835f85b6f107f2822
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149906"
---
# <span data-ttu-id="13640-101">Set-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="13640-101">Set-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="13640-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13640-102">SYNOPSIS</span></span>
<span data-ttu-id="13640-103">Beállítja az SQL-készlet oszlopainak adattípusait és bizalmasság-címkéit.</span><span class="sxs-lookup"><span data-stu-id="13640-103">Sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="13640-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13640-104">SYNTAX</span></span>

### <span data-ttu-id="13640-105">ClassificationObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13640-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13640-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="13640-106">ColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-WorkspaceName] <String> [-SqlPoolName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13640-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="13640-107">SqlPoolObjectColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13640-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13640-108">DESCRIPTION</span></span>
<span data-ttu-id="13640-109">A Set-AzSynapseSqlPoolSensitivityClassification parancsmag beállítja az SQL-készlet oszlopainak adattípusait és bizalmasság-címkéit.</span><span class="sxs-lookup"><span data-stu-id="13640-109">The Set-AzSynapseSqlPoolSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="13640-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13640-110">EXAMPLES</span></span>

### <span data-ttu-id="13640-111">1. példa: Egy Azure Synapse SQL-készlet oszlopának adattípusának és bizalmasság-címkéinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="13640-111">Example 1: Set information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="13640-112">2. példa: Az Azure Synapse SQL-készlet oszlopainak ajánlott adattípusainak és bizalmasság-címkéinek beállítása.</span><span class="sxs-lookup"><span data-stu-id="13640-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="13640-113">3. példa: Az Azure Synapse SQL-készlet oszlopának adattípusának és bizalmasság-címkéinek beállítása pipázás használatával.</span><span class="sxs-lookup"><span data-stu-id="13640-113">Example 3: Set information type and sensitivity label of a column in an Azure Synapse SQL pool, using piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="13640-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13640-114">PARAMETERS</span></span>

### <span data-ttu-id="13640-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13640-115">-AsJob</span></span>
<span data-ttu-id="13640-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="13640-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13640-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="13640-117">-ClassificationObject</span></span>
<span data-ttu-id="13640-118">Egy SQL-készlet bizalmasság-besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="13640-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13640-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="13640-119">-ColumnName</span></span>
<span data-ttu-id="13640-120">Az oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="13640-120">Name of column.</span></span>

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

### <span data-ttu-id="13640-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13640-121">-DefaultProfile</span></span>
<span data-ttu-id="13640-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13640-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13640-123">-InformationType</span><span class="sxs-lookup"><span data-stu-id="13640-123">-InformationType</span></span>
<span data-ttu-id="13640-124">Az oszlopban tárolt adatok adattípusát leíró név.</span><span class="sxs-lookup"><span data-stu-id="13640-124">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13640-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13640-125">-PassThru</span></span>
<span data-ttu-id="13640-126">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="13640-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="13640-127">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="13640-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="13640-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13640-128">-ResourceGroupName</span></span>
<span data-ttu-id="13640-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="13640-129">Resource group name.</span></span>

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

### <span data-ttu-id="13640-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="13640-130">-SchemaName</span></span>
<span data-ttu-id="13640-131">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="13640-131">Name of schema.</span></span>

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

### <span data-ttu-id="13640-132">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="13640-132">-SensitivityLabel</span></span>
<span data-ttu-id="13640-133">Az oszlopban tárolt adatok bizalmasságát leíró név.</span><span class="sxs-lookup"><span data-stu-id="13640-133">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13640-134">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="13640-134">-SqlPoolName</span></span>
<span data-ttu-id="13640-135">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="13640-135">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="13640-136">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="13640-136">-SqlPoolObject</span></span>
<span data-ttu-id="13640-137">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="13640-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="13640-138">-TableName</span><span class="sxs-lookup"><span data-stu-id="13640-138">-TableName</span></span>
<span data-ttu-id="13640-139">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="13640-139">Name of table.</span></span>

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

### <span data-ttu-id="13640-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="13640-140">-WorkspaceName</span></span>
<span data-ttu-id="13640-141">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="13640-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="13640-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13640-142">-Confirm</span></span>
<span data-ttu-id="13640-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="13640-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13640-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13640-144">-WhatIf</span></span>
<span data-ttu-id="13640-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="13640-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13640-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13640-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13640-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13640-147">CommonParameters</span></span>
<span data-ttu-id="13640-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13640-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13640-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13640-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13640-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13640-150">INPUTS</span></span>

### <span data-ttu-id="13640-151">System.String</span><span class="sxs-lookup"><span data-stu-id="13640-151">System.String</span></span>

### <span data-ttu-id="13640-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="13640-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="13640-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="13640-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="13640-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13640-154">OUTPUTS</span></span>

### <span data-ttu-id="13640-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="13640-155">System.Boolean</span></span>

## <span data-ttu-id="13640-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13640-156">NOTES</span></span>

## <span data-ttu-id="13640-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13640-157">RELATED LINKS</span></span>
