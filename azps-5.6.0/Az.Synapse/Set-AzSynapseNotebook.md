---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: 9b960c3b671ecada8f4f24e1b5a8897de7004440
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007445"
---
# <span data-ttu-id="f8357-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="f8357-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="f8357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8357-102">SYNOPSIS</span></span>
<span data-ttu-id="f8357-103">Létrehozza vagy frissíti a jegyzetfüzetet egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="f8357-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="f8357-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f8357-104">SYNTAX</span></span>

### <span data-ttu-id="f8357-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8357-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8357-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="f8357-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8357-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="f8357-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8357-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="f8357-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8357-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f8357-109">DESCRIPTION</span></span>
<span data-ttu-id="f8357-110">A **Set-AzSynapseNotebook** parancsmag létrehoz vagy frissíti a jegyzetfüzetet egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="f8357-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="f8357-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f8357-111">EXAMPLES</span></span>

### <span data-ttu-id="f8357-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="f8357-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="f8357-113">Ez a parancs létrehozza vagy frissíti a jegyzetfüzetet a notebook.ipynb jegyzetfüzetfájlból a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="f8357-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f8357-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="f8357-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="f8357-115">Ez a parancs létrehozza vagy frissíti a Jegyzetfüzetfájl-jegyzetfüzet.ipynb jegyzetfüzetet a ContosoWorkspace nevű munkaterületen a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="f8357-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="f8357-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="f8357-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="f8357-117">Ez a parancs létrehoz vagy frissíti a jegyzetfüzetfájl jegyzetfüzet.ipynb fájlját, amely a ContosoSparkPoolhoz csatlakozik, és 2 végrehajtót használ a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="f8357-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="f8357-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8357-118">PARAMETERS</span></span>

### <span data-ttu-id="f8357-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8357-119">-AsJob</span></span>
<span data-ttu-id="f8357-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f8357-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8357-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8357-121">-DefaultProfile</span></span>
<span data-ttu-id="f8357-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8357-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8357-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="f8357-123">-DefinitionFile</span></span>
<span data-ttu-id="f8357-124">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f8357-124">The JSON file path.</span></span>

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

### <span data-ttu-id="f8357-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="f8357-125">-ExecutorCount</span></span>
<span data-ttu-id="f8357-126">A feladathoz a megadott értékgörbekészletben kiosztandó végrehajtók száma.</span><span class="sxs-lookup"><span data-stu-id="f8357-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="f8357-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="f8357-127">-ExecutorSize</span></span>
<span data-ttu-id="f8357-128">A feladathoz a megadott Értékgörbekészletben kiosztott végrehajtók számára használt alapértékek és memória száma.</span><span class="sxs-lookup"><span data-stu-id="f8357-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="f8357-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f8357-129">-Name</span></span>
<span data-ttu-id="f8357-130">A jegyzetfüzet neve.</span><span class="sxs-lookup"><span data-stu-id="f8357-130">The notebook name.</span></span>

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

### <span data-ttu-id="f8357-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="f8357-131">-SparkPoolName</span></span>
<span data-ttu-id="f8357-132">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="f8357-132">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="f8357-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f8357-133">-WorkspaceName</span></span>
<span data-ttu-id="f8357-134">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="f8357-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f8357-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f8357-135">-WorkspaceObject</span></span>
<span data-ttu-id="f8357-136">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="f8357-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f8357-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8357-137">-Confirm</span></span>
<span data-ttu-id="f8357-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f8357-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8357-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8357-139">-WhatIf</span></span>
<span data-ttu-id="f8357-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f8357-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8357-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f8357-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8357-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8357-142">CommonParameters</span></span>
<span data-ttu-id="f8357-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8357-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8357-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8357-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8357-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8357-145">INPUTS</span></span>

### <span data-ttu-id="f8357-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f8357-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f8357-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8357-147">OUTPUTS</span></span>

### <span data-ttu-id="f8357-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="f8357-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="f8357-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f8357-149">NOTES</span></span>

## <span data-ttu-id="f8357-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8357-150">RELATED LINKS</span></span>
