---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183154"
---
# <span data-ttu-id="12dd6-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="12dd6-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="12dd6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="12dd6-103">Jegyzetfüzetet hoz létre vagy frissít a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="12dd6-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="12dd6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12dd6-104">SYNTAX</span></span>

### <span data-ttu-id="12dd6-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12dd6-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12dd6-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="12dd6-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12dd6-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="12dd6-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12dd6-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="12dd6-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12dd6-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="12dd6-109">DESCRIPTION</span></span>
<span data-ttu-id="12dd6-110">A **set-AzSynapseNotebook** parancsmag egy munkaterületen lévő jegyzetfüzetet hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="12dd6-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="12dd6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="12dd6-111">EXAMPLES</span></span>

### <span data-ttu-id="12dd6-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="12dd6-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="12dd6-113">Ez a parancs jegyzetfüzetet hoz létre vagy frissít a jegyzetfüzet. ipynb nevű jegyzetfüzetből a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="12dd6-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="12dd6-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="12dd6-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="12dd6-115">Ez a parancs jegyzetfüzetet hoz létre vagy frissít a jegyzetfüzet. ipynb nevű munkaterületről a ContosoWorkspace through pipeline nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="12dd6-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="12dd6-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="12dd6-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="12dd6-117">Ez a parancs jegyzetfüzetet hoz létre vagy frissít a jegyzetfüzetből. ipynb, amely az ContosoSparkPool-ra hivatkozik, és 2 gondnokot használ a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="12dd6-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="12dd6-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12dd6-118">PARAMETERS</span></span>

### <span data-ttu-id="12dd6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12dd6-119">-AsJob</span></span>
<span data-ttu-id="12dd6-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="12dd6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12dd6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12dd6-121">-DefaultProfile</span></span>
<span data-ttu-id="12dd6-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12dd6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12dd6-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="12dd6-123">-DefinitionFile</span></span>
<span data-ttu-id="12dd6-124">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="12dd6-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12dd6-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="12dd6-125">-ExecutorCount</span></span>
<span data-ttu-id="12dd6-126">A projekthez megadott Spark-készletben kiosztani kívánt kivitelezők száma.</span><span class="sxs-lookup"><span data-stu-id="12dd6-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12dd6-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="12dd6-127">-ExecutorSize</span></span>
<span data-ttu-id="12dd6-128">A projekthez megadott Spark-készletben kiosztott végrehajtók számára használandó alapvető és memória száma.</span><span class="sxs-lookup"><span data-stu-id="12dd6-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12dd6-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="12dd6-129">-Name</span></span>
<span data-ttu-id="12dd6-130">A jegyzetfüzet neve.</span><span class="sxs-lookup"><span data-stu-id="12dd6-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12dd6-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="12dd6-131">-SparkPoolName</span></span>
<span data-ttu-id="12dd6-132">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="12dd6-132">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12dd6-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="12dd6-133">-WorkspaceName</span></span>
<span data-ttu-id="12dd6-134">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="12dd6-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12dd6-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="12dd6-135">-WorkspaceObject</span></span>
<span data-ttu-id="12dd6-136">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="12dd6-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12dd6-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="12dd6-137">-Confirm</span></span>
<span data-ttu-id="12dd6-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="12dd6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12dd6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12dd6-139">-WhatIf</span></span>
<span data-ttu-id="12dd6-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="12dd6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12dd6-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12dd6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12dd6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12dd6-142">CommonParameters</span></span>
<span data-ttu-id="12dd6-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12dd6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12dd6-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="12dd6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12dd6-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12dd6-145">INPUTS</span></span>

### <span data-ttu-id="12dd6-146">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="12dd6-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="12dd6-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12dd6-147">OUTPUTS</span></span>

### <span data-ttu-id="12dd6-148">Microsoft. Azure. commands. szinapszis. models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="12dd6-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="12dd6-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12dd6-149">NOTES</span></span>

## <span data-ttu-id="12dd6-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12dd6-150">RELATED LINKS</span></span>
