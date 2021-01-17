---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383597"
---
# <span data-ttu-id="0b090-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="0b090-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="0b090-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b090-102">SYNOPSIS</span></span>
<span data-ttu-id="0b090-103">Egy Synapse Analytics spark-készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0b090-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="0b090-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b090-104">SYNTAX</span></span>

### <span data-ttu-id="0b090-105">CreateByNameAndEnableAutoScaleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0b090-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b090-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b090-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b090-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b090-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b090-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b090-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b090-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b090-109">DESCRIPTION</span></span>
<span data-ttu-id="0b090-110">A **New-AzSynapseSparkPool** parancsmag létrehoz egy Azure Synapse Analytics Spark-készletet.</span><span class="sxs-lookup"><span data-stu-id="0b090-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="0b090-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b090-111">EXAMPLES</span></span>

### <span data-ttu-id="0b090-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="0b090-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="0b090-113">Ez a parancs létrehoz egy Azure Synapse Analytics spark-készletet.</span><span class="sxs-lookup"><span data-stu-id="0b090-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="0b090-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="0b090-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="0b090-115">Ez a parancs egy Azure Synapse Analytics Spark-készletet hoz létre, amelynél engedélyezve van az automatikus méretezés.</span><span class="sxs-lookup"><span data-stu-id="0b090-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="0b090-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="0b090-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="0b090-117">Ez a parancs egy Azure Synapse Analytics spark-készletet hoz létre a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="0b090-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="0b090-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="0b090-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="0b090-119">Ez a parancs létrehoz egy Azure Synapse Analytics Spark-készletet, amelynél a folyamaton keresztül engedélyezve van az automatikus méretezés.</span><span class="sxs-lookup"><span data-stu-id="0b090-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="0b090-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b090-120">PARAMETERS</span></span>

### <span data-ttu-id="0b090-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b090-121">-AsJob</span></span>
<span data-ttu-id="0b090-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0b090-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b090-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="0b090-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="0b090-124">Az üresjárati percek száma.</span><span class="sxs-lookup"><span data-stu-id="0b090-124">Number of minutes idle.</span></span> <span data-ttu-id="0b090-125">Ezt a paramétert az automatikus szüneteltetés engedélyezésekor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="0b090-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="0b090-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="0b090-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="0b090-127">A megadott értékkészletben lefoglalandó csomópontok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="0b090-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="0b090-128">Ezt a paramétert az automatikus méretezés engedélyezésekor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="0b090-128">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="0b090-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="0b090-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="0b090-130">A megadott értékkészletben kiosztandó csomópontok minimális száma.</span><span class="sxs-lookup"><span data-stu-id="0b090-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="0b090-131">Ezt a paramétert az automatikus méretezés engedélyezésekor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="0b090-131">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="0b090-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b090-132">-DefaultProfile</span></span>
<span data-ttu-id="0b090-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b090-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b090-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="0b090-134">-EnableAutoPause</span></span>
<span data-ttu-id="0b090-135">Azt jelzi, hogy engedélyezve kell-e lennie az automatikus szüneteltetésnek.</span><span class="sxs-lookup"><span data-stu-id="0b090-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="0b090-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="0b090-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="0b090-137">Környezetkonfigurációs fájl ("PIP freeze" kimenet).</span><span class="sxs-lookup"><span data-stu-id="0b090-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="0b090-138">-Name</span><span class="sxs-lookup"><span data-stu-id="0b090-138">-Name</span></span>
<span data-ttu-id="0b090-139">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="0b090-139">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="0b090-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="0b090-140">-NodeCount</span></span>
<span data-ttu-id="0b090-141">A megadott értékkészletben kiosztandó csomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="0b090-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="0b090-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="0b090-142">-NodeSize</span></span>
<span data-ttu-id="0b090-143">A megadott értékkészletben kiosztott csomópontokhoz használt alapértékek és memória száma.</span><span class="sxs-lookup"><span data-stu-id="0b090-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="0b090-144">Ezt a paramétert az automatikus méretezés letiltása esetén kell megadni.</span><span class="sxs-lookup"><span data-stu-id="0b090-144">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="0b090-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b090-145">-ResourceGroupName</span></span>
<span data-ttu-id="0b090-146">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0b090-146">Resource group name.</span></span>

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

### <span data-ttu-id="0b090-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="0b090-147">-SparkVersion</span></span>
<span data-ttu-id="0b090-148">Spark-verzió.</span><span class="sxs-lookup"><span data-stu-id="0b090-148">Apache Spark version.</span></span>
<span data-ttu-id="0b090-149">Engedélyezett értékek: 2,4</span><span class="sxs-lookup"><span data-stu-id="0b090-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="0b090-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b090-150">-Tag</span></span>
<span data-ttu-id="0b090-151">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="0b090-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="0b090-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0b090-152">-WorkspaceName</span></span>
<span data-ttu-id="0b090-153">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="0b090-153">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0b090-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0b090-154">-WorkspaceObject</span></span>
<span data-ttu-id="0b090-155">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b090-155">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0b090-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b090-156">-Confirm</span></span>
<span data-ttu-id="0b090-157">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0b090-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b090-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b090-158">-WhatIf</span></span>
<span data-ttu-id="0b090-159">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0b090-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b090-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0b090-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b090-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b090-161">CommonParameters</span></span>
<span data-ttu-id="0b090-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b090-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b090-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b090-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b090-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b090-164">INPUTS</span></span>

### <span data-ttu-id="0b090-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0b090-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0b090-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b090-166">OUTPUTS</span></span>

### <span data-ttu-id="0b090-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="0b090-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="0b090-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b090-168">NOTES</span></span>

## <span data-ttu-id="0b090-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b090-169">RELATED LINKS</span></span>
