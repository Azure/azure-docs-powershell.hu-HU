---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: a278b316a62639c6c33d4f05491e314a2b9a1e85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383346"
---
# <span data-ttu-id="1c958-101">Remove-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="1c958-101">Remove-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="1c958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c958-102">SYNOPSIS</span></span>
<span data-ttu-id="1c958-103">Eltávolítja az SQL-készlet oszlopainak adattípusait és bizalmasság-címkéit.</span><span class="sxs-lookup"><span data-stu-id="1c958-103">Removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="1c958-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1c958-104">SYNTAX</span></span>

### <span data-ttu-id="1c958-105">ClassificationObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c958-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c958-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c958-106">ColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c958-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c958-107">SqlPoolObjectColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c958-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1c958-108">DESCRIPTION</span></span>
<span data-ttu-id="1c958-109">A Remove-AzSynapseSqlPoolSensitivityClassification parancsmag eltávolítja az SQL-készlet oszlopainak adattípusait és bizalmasság-címkéit.</span><span class="sxs-lookup"><span data-stu-id="1c958-109">The Remove-AzSynapseSqlPoolSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="1c958-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1c958-110">EXAMPLES</span></span>

### <span data-ttu-id="1c958-111">1. példa: Távolítsa el egy Azure Synapse SQL-készlet oszlopának adattípusát és bizalmasság-címkéjét.</span><span class="sxs-lookup"><span data-stu-id="1c958-111">Example 1: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="1c958-112">2. példa: Az Azure Synapse SQL-készlet oszlopainak aktuális adattípusait és bizalmasság-címkéit a Piping használatával távolíthatja el.</span><span class="sxs-lookup"><span data-stu-id="1c958-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="1c958-113">3. példa: Távolítsa el egy Azure Synapse SQL-készlet oszlopának adattípusát és bizalmasság-címkéjét a Piping használatával.</span><span class="sxs-lookup"><span data-stu-id="1c958-113">Example 3: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="1c958-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c958-114">PARAMETERS</span></span>

### <span data-ttu-id="1c958-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c958-115">-AsJob</span></span>
<span data-ttu-id="1c958-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1c958-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c958-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="1c958-117">-ClassificationObject</span></span>
<span data-ttu-id="1c958-118">Egy SQL-készlet bizalmasság-besorolását képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="1c958-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="1c958-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="1c958-119">-ColumnName</span></span>
<span data-ttu-id="1c958-120">Az oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="1c958-120">Name of column.</span></span>

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

### <span data-ttu-id="1c958-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c958-121">-DefaultProfile</span></span>
<span data-ttu-id="1c958-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c958-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c958-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c958-123">-PassThru</span></span>
<span data-ttu-id="1c958-124">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="1c958-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1c958-125">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="1c958-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1c958-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c958-126">-ResourceGroupName</span></span>
<span data-ttu-id="1c958-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1c958-127">Resource group name.</span></span>

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

### <span data-ttu-id="1c958-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="1c958-128">-SchemaName</span></span>
<span data-ttu-id="1c958-129">A séma neve.</span><span class="sxs-lookup"><span data-stu-id="1c958-129">Name of schema.</span></span>

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

### <span data-ttu-id="1c958-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="1c958-130">-SqlPoolName</span></span>
<span data-ttu-id="1c958-131">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="1c958-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="1c958-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="1c958-132">-SqlPoolObject</span></span>
<span data-ttu-id="1c958-133">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="1c958-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1c958-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="1c958-134">-TableName</span></span>
<span data-ttu-id="1c958-135">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="1c958-135">Name of table.</span></span>

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

### <span data-ttu-id="1c958-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1c958-136">-WorkspaceName</span></span>
<span data-ttu-id="1c958-137">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="1c958-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1c958-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c958-138">-Confirm</span></span>
<span data-ttu-id="1c958-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1c958-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c958-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c958-140">-WhatIf</span></span>
<span data-ttu-id="1c958-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1c958-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c958-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1c958-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c958-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c958-143">CommonParameters</span></span>
<span data-ttu-id="1c958-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c958-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c958-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c958-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c958-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c958-146">INPUTS</span></span>

### <span data-ttu-id="1c958-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="1c958-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="1c958-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1c958-148">System.String</span></span>

### <span data-ttu-id="1c958-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1c958-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1c958-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c958-150">OUTPUTS</span></span>

### <span data-ttu-id="1c958-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1c958-151">System.Boolean</span></span>

## <span data-ttu-id="1c958-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1c958-152">NOTES</span></span>

## <span data-ttu-id="1c958-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c958-153">RELATED LINKS</span></span>
