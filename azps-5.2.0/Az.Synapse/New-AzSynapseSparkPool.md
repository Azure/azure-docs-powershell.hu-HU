---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368506"
---
# <span data-ttu-id="ffcdb-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="ffcdb-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="ffcdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffcdb-102">SYNOPSIS</span></span>
<span data-ttu-id="ffcdb-103">Egy Synapse Analytics spark-készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="ffcdb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ffcdb-104">SYNTAX</span></span>

### <span data-ttu-id="ffcdb-105">CreateByNameAndEnableAutoScaleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ffcdb-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffcdb-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffcdb-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffcdb-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffcdb-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffcdb-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffcdb-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffcdb-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ffcdb-109">DESCRIPTION</span></span>
<span data-ttu-id="ffcdb-110">A **New-AzSynapseSparkPool** parancsmag létrehoz egy Azure Synapse Analytics Spark-készletet.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="ffcdb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ffcdb-111">EXAMPLES</span></span>

### <span data-ttu-id="ffcdb-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="ffcdb-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="ffcdb-113">Ez a parancs létrehoz egy Azure Synapse Analytics spark-készletet.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="ffcdb-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="ffcdb-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="ffcdb-115">Ez a parancs egy Azure Synapse Analytics Spark-készletet hoz létre, amelynél engedélyezve van az automatikus méretezés.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="ffcdb-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="ffcdb-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="ffcdb-117">Ez a parancs egy Azure Synapse Analytics spark-készletet hoz létre a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="ffcdb-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="ffcdb-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="ffcdb-119">Ez a parancs létrehoz egy Azure Synapse Analytics Spark-készletet, amelynél a folyamaton keresztül engedélyezve van az automatikus méretezés.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="ffcdb-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffcdb-120">PARAMETERS</span></span>

### <span data-ttu-id="ffcdb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffcdb-121">-AsJob</span></span>
<span data-ttu-id="ffcdb-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ffcdb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ffcdb-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="ffcdb-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="ffcdb-124">Az üresjárati percek száma.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-124">Number of minutes idle.</span></span> <span data-ttu-id="ffcdb-125">Ezt a paramétert az automatikus szüneteltetés engedélyezésekor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-125">This parameter must be specified when Auto-pause is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcdb-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="ffcdb-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="ffcdb-127">A megadott értékkészletben lefoglalandó csomópontok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="ffcdb-128">Ezt a paramétert az automatikus méretezés engedélyezésekor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-128">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcdb-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="ffcdb-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="ffcdb-130">A megadott értékkészletben kiosztandó csomópontok minimális száma.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="ffcdb-131">Ezt a paramétert az automatikus méretezés engedélyezésekor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-131">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcdb-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffcdb-132">-DefaultProfile</span></span>
<span data-ttu-id="ffcdb-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffcdb-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="ffcdb-134">-EnableAutoPause</span></span>
<span data-ttu-id="ffcdb-135">Azt jelzi, hogy engedélyezve kell-e lennie az automatikus szüneteltetésnek.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="ffcdb-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="ffcdb-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="ffcdb-137">Környezetkonfigurációs fájl ("PIP freeze" kimenet).</span><span class="sxs-lookup"><span data-stu-id="ffcdb-137">Environment configuration file ("PIP freeze" output).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcdb-138">-Name</span><span class="sxs-lookup"><span data-stu-id="ffcdb-138">-Name</span></span>
<span data-ttu-id="ffcdb-139">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-139">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcdb-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="ffcdb-140">-NodeCount</span></span>
<span data-ttu-id="ffcdb-141">A megadott értékkészletben kiosztandó csomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndDisableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcdb-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="ffcdb-142">-NodeSize</span></span>
<span data-ttu-id="ffcdb-143">A megadott értékkészletben kiosztott csomópontokhoz használt alapértékek és memória száma.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="ffcdb-144">Ezt a paramétert az automatikus méretezés letiltása esetén kell megadni.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-144">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcdb-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffcdb-145">-ResourceGroupName</span></span>
<span data-ttu-id="ffcdb-146">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcdb-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="ffcdb-147">-SparkVersion</span></span>
<span data-ttu-id="ffcdb-148">Spark-verzió.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-148">Apache Spark version.</span></span>
<span data-ttu-id="ffcdb-149">Engedélyezett értékek: 2,4</span><span class="sxs-lookup"><span data-stu-id="ffcdb-149">Allowed values: 2.4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcdb-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="ffcdb-150">-Tag</span></span>
<span data-ttu-id="ffcdb-151">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-151">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcdb-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ffcdb-152">-WorkspaceName</span></span>
<span data-ttu-id="ffcdb-153">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-153">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcdb-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ffcdb-154">-WorkspaceObject</span></span>
<span data-ttu-id="ffcdb-155">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-155">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectAndEnableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffcdb-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffcdb-156">-Confirm</span></span>
<span data-ttu-id="ffcdb-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffcdb-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffcdb-158">-WhatIf</span></span>
<span data-ttu-id="ffcdb-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffcdb-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffcdb-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffcdb-161">CommonParameters</span></span>
<span data-ttu-id="ffcdb-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffcdb-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffcdb-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffcdb-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffcdb-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffcdb-164">INPUTS</span></span>

### <span data-ttu-id="ffcdb-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ffcdb-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ffcdb-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffcdb-166">OUTPUTS</span></span>

### <span data-ttu-id="ffcdb-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="ffcdb-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="ffcdb-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ffcdb-168">NOTES</span></span>

## <span data-ttu-id="ffcdb-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffcdb-169">RELATED LINKS</span></span>
