---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186164"
---
# <span data-ttu-id="feff8-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="feff8-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="feff8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="feff8-102">SYNOPSIS</span></span>
<span data-ttu-id="feff8-103">Exportálja a notbooks.</span><span class="sxs-lookup"><span data-stu-id="feff8-103">Exports notbooks.</span></span>

## <span data-ttu-id="feff8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="feff8-104">SYNTAX</span></span>

### <span data-ttu-id="feff8-105">ExportByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="feff8-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feff8-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="feff8-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feff8-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="feff8-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feff8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="feff8-108">DESCRIPTION</span></span>
<span data-ttu-id="feff8-109">Az **export-AzSynapseNotebook** parancsmag Azure szinapszis-jegyzetfüzetet exportál a jegyzetfüzetbe (. ipynb).</span><span class="sxs-lookup"><span data-stu-id="feff8-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="feff8-110">A jegyzetfüzet neve lesz az exportált fájl neve.</span><span class="sxs-lookup"><span data-stu-id="feff8-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="feff8-111">Ha a jegyzetfüzet nevét adja meg, a parancsmag a jegyzetfüzetet exportálja.</span><span class="sxs-lookup"><span data-stu-id="feff8-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="feff8-112">Ha nem ad meg nevet, a parancsmag az összes jegyzetfüzetet exportálja a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="feff8-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="feff8-113">Példák</span><span class="sxs-lookup"><span data-stu-id="feff8-113">EXAMPLES</span></span>

### <span data-ttu-id="feff8-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="feff8-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="feff8-115">Az összes jegyzetfüzetet exportálja a munkaterület ContosoWorkspace a "C:\Notebook" mappába.</span><span class="sxs-lookup"><span data-stu-id="feff8-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="feff8-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="feff8-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="feff8-117">A ContosoNotebook nevű egyetlen jegyzetfüzetet exportálja a munkaterület ContosoWorkspace a "C:\Notebook" mappába.</span><span class="sxs-lookup"><span data-stu-id="feff8-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="feff8-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="feff8-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="feff8-119">A ContosoNotebook nevű egyetlen jegyzetfüzetet exportálja a munkaterület ContosoWorkspace a "C:\Notebook" mappába a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="feff8-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="feff8-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="feff8-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="feff8-121">A ContosoNotebook nevű egyetlen jegyzetfüzetet exportálja a munkaterület ContosoWorkspace a "C:\Notebook" mappába a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="feff8-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="feff8-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="feff8-122">PARAMETERS</span></span>

### <span data-ttu-id="feff8-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="feff8-123">-AsJob</span></span>
<span data-ttu-id="feff8-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="feff8-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="feff8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feff8-125">-DefaultProfile</span></span>
<span data-ttu-id="feff8-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="feff8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feff8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="feff8-127">-InputObject</span></span>
<span data-ttu-id="feff8-128">A jegyzetfüzet objektuma.</span><span class="sxs-lookup"><span data-stu-id="feff8-128">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: ExportByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="feff8-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="feff8-129">-Name</span></span>
<span data-ttu-id="feff8-130">A jegyzetfüzet neve.</span><span class="sxs-lookup"><span data-stu-id="feff8-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName, ExportByObject
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feff8-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="feff8-131">-OutputFolder</span></span>
<span data-ttu-id="feff8-132">Az a mappa, ahol a jegyzetfüzetet el kell helyezni.</span><span class="sxs-lookup"><span data-stu-id="feff8-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="feff8-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="feff8-133">-WorkspaceName</span></span>
<span data-ttu-id="feff8-134">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="feff8-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feff8-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="feff8-135">-WorkspaceObject</span></span>
<span data-ttu-id="feff8-136">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="feff8-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ExportByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="feff8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feff8-137">CommonParameters</span></span>
<span data-ttu-id="feff8-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="feff8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feff8-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="feff8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feff8-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="feff8-140">INPUTS</span></span>

### <span data-ttu-id="feff8-141">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="feff8-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="feff8-142">Microsoft. Azure. commands. szinapszis. models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="feff8-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="feff8-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="feff8-143">OUTPUTS</span></span>

### <span data-ttu-id="feff8-144">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="feff8-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="feff8-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="feff8-145">NOTES</span></span>

## <span data-ttu-id="feff8-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="feff8-146">RELATED LINKS</span></span>