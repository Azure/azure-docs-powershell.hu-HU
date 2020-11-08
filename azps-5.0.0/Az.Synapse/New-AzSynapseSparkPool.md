---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186316"
---
# <span data-ttu-id="a5c13-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="a5c13-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="a5c13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5c13-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c13-103">Létrehoz egy szinapszis-elemzési szikra medencét.</span><span class="sxs-lookup"><span data-stu-id="a5c13-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="a5c13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5c13-104">SYNTAX</span></span>

### <span data-ttu-id="a5c13-105">CreateByNameAndEnableAutoScaleParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5c13-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c13-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5c13-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c13-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5c13-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c13-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5c13-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5c13-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5c13-109">DESCRIPTION</span></span>
<span data-ttu-id="a5c13-110">A **New-AzSynapseSparkPool** parancsmag létrehoz egy Azure szinapszis Analytics Spark poolt.</span><span class="sxs-lookup"><span data-stu-id="a5c13-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="a5c13-111">Példák</span><span class="sxs-lookup"><span data-stu-id="a5c13-111">EXAMPLES</span></span>

### <span data-ttu-id="a5c13-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a5c13-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="a5c13-113">Ez a parancs létrehoz egy Azure szinapszis-elemző Spark-medencét.</span><span class="sxs-lookup"><span data-stu-id="a5c13-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="a5c13-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a5c13-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="a5c13-115">Ez a parancs létrehoz egy Azure szinapszis Analytics Spark-medencét, amelyen az automatikus méretezés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="a5c13-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="a5c13-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="a5c13-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="a5c13-117">Ez a parancs létrehoz egy Azure szinapszis-elemző Spark-medencét csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="a5c13-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="a5c13-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="a5c13-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="a5c13-119">A parancs létrehoz egy Azure szinapszis Analytics Spark-medencét, amelyen az automatikus lépték engedélyezve van a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="a5c13-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="a5c13-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5c13-120">PARAMETERS</span></span>

### <span data-ttu-id="a5c13-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5c13-121">-AsJob</span></span>
<span data-ttu-id="a5c13-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a5c13-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5c13-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="a5c13-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="a5c13-124">Üresjárati percek száma.</span><span class="sxs-lookup"><span data-stu-id="a5c13-124">Number of minutes idle.</span></span> <span data-ttu-id="a5c13-125">Ezt a paramétert akkor adja meg, ha az automatikus szünet engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="a5c13-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="a5c13-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="a5c13-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="a5c13-127">A megadott Spark-készletben kiosztani kívánt csomópontok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="a5c13-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="a5c13-128">Ezt a paramétert akkor adja meg, ha az automatikus méretezés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="a5c13-128">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="a5c13-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="a5c13-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="a5c13-130">A megadott Spark-készletben kiosztani kívánt csomópontok minimális száma</span><span class="sxs-lookup"><span data-stu-id="a5c13-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="a5c13-131">Ezt a paramétert akkor adja meg, ha az automatikus méretezés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="a5c13-131">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="a5c13-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c13-132">-DefaultProfile</span></span>
<span data-ttu-id="a5c13-133">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5c13-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5c13-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="a5c13-134">-EnableAutoPause</span></span>
<span data-ttu-id="a5c13-135">Azt jelzi, hogy engedélyezve kell-e az automatikus szüneteltetést.</span><span class="sxs-lookup"><span data-stu-id="a5c13-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="a5c13-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="a5c13-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="a5c13-137">Környezet konfigurációs fájlja ("PIP rögzítése" kimenet)</span><span class="sxs-lookup"><span data-stu-id="a5c13-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="a5c13-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5c13-138">-Name</span></span>
<span data-ttu-id="a5c13-139">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="a5c13-139">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="a5c13-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="a5c13-140">-NodeCount</span></span>
<span data-ttu-id="a5c13-141">A megadott Spark-készletben kiosztani kívánt csomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="a5c13-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="a5c13-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="a5c13-142">-NodeSize</span></span>
<span data-ttu-id="a5c13-143">A megadott Spark-készletben kiosztott csomópontok számára használandó alapvető és memória száma.</span><span class="sxs-lookup"><span data-stu-id="a5c13-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="a5c13-144">Ezt a paramétert meg kell adni, ha az automatikus méretezés le van tiltva</span><span class="sxs-lookup"><span data-stu-id="a5c13-144">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="a5c13-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c13-145">-ResourceGroupName</span></span>
<span data-ttu-id="a5c13-146">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a5c13-146">Resource group name.</span></span>

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

### <span data-ttu-id="a5c13-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="a5c13-147">-SparkVersion</span></span>
<span data-ttu-id="a5c13-148">Apache Spark verzió.</span><span class="sxs-lookup"><span data-stu-id="a5c13-148">Apache Spark version.</span></span>
<span data-ttu-id="a5c13-149">Engedélyezett értékek: 2,4</span><span class="sxs-lookup"><span data-stu-id="a5c13-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="a5c13-150">-Címke</span><span class="sxs-lookup"><span data-stu-id="a5c13-150">-Tag</span></span>
<span data-ttu-id="a5c13-151">Az erőforráshoz társított címkék karakterlánca, karakterláncok szótára</span><span class="sxs-lookup"><span data-stu-id="a5c13-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="a5c13-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5c13-152">-WorkspaceName</span></span>
<span data-ttu-id="a5c13-153">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="a5c13-153">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a5c13-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a5c13-154">-WorkspaceObject</span></span>
<span data-ttu-id="a5c13-155">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="a5c13-155">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a5c13-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5c13-156">-Confirm</span></span>
<span data-ttu-id="a5c13-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5c13-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c13-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c13-158">-WhatIf</span></span>
<span data-ttu-id="a5c13-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5c13-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c13-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5c13-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c13-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c13-161">CommonParameters</span></span>
<span data-ttu-id="a5c13-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5c13-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c13-163">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a5c13-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c13-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5c13-164">INPUTS</span></span>

### <span data-ttu-id="a5c13-165">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5c13-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a5c13-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5c13-166">OUTPUTS</span></span>

### <span data-ttu-id="a5c13-167">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="a5c13-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="a5c13-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5c13-168">NOTES</span></span>

## <span data-ttu-id="a5c13-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5c13-169">RELATED LINKS</span></span>
