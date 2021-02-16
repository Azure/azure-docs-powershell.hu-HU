---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209063"
---
# <span data-ttu-id="1dcdf-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="1dcdf-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="1dcdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dcdf-102">SYNOPSIS</span></span>
<span data-ttu-id="1dcdf-103">Notbooks exportálása.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-103">Exports notbooks.</span></span>

## <span data-ttu-id="1dcdf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1dcdf-104">SYNTAX</span></span>

### <span data-ttu-id="1dcdf-105">ExportByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1dcdf-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dcdf-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="1dcdf-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dcdf-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="1dcdf-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dcdf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1dcdf-108">DESCRIPTION</span></span>
<span data-ttu-id="1dcdf-109">Az **Export-AzSynapseNotebook** parancsmag egy Azure Synapse-jegyzetfüzetet exportál egy jegyzetfüzetfájlba (.ipynb).</span><span class="sxs-lookup"><span data-stu-id="1dcdf-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="1dcdf-110">A jegyzetfüzet neve lesz az exportált fájl neve.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="1dcdf-111">Ha megadja egy jegyzetfüzet nevét, a parancsmag exportálja azt.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="1dcdf-112">Ha nem ad meg nevet, a parancsmag exportálja a munkaterület összes jegyzetfüzetét.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="1dcdf-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1dcdf-113">EXAMPLES</span></span>

### <span data-ttu-id="1dcdf-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="1dcdf-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="1dcdf-115">A ContosoWorkspace munkaterületen lévő összes jegyzetfüzet exportálása a "C:\Jegyzetfüzet" mappába.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="1dcdf-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="1dcdf-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="1dcdf-117">Exportálja a ContosoWorkspace munkaterületen található ContosoNotebook nevű jegyzetfüzetet a "C:\Notebook" mappába.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="1dcdf-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="1dcdf-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="1dcdf-119">A ContosoWorkspace munkaterületen található ContosoNotebook nevű jegyzetfüzet exportálása a "C:\Notebook" mappába folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="1dcdf-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="1dcdf-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="1dcdf-121">A ContosoWorkspace munkaterületen található ContosoNotebook nevű jegyzetfüzet exportálása a "C:\Notebook" mappába folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="1dcdf-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dcdf-122">PARAMETERS</span></span>

### <span data-ttu-id="1dcdf-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dcdf-123">-AsJob</span></span>
<span data-ttu-id="1dcdf-124">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1dcdf-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dcdf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dcdf-125">-DefaultProfile</span></span>
<span data-ttu-id="1dcdf-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dcdf-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dcdf-127">-InputObject</span></span>
<span data-ttu-id="1dcdf-128">A jegyzetfüzet-objektum.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-128">The notebook object.</span></span>

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

### <span data-ttu-id="1dcdf-129">-Name</span><span class="sxs-lookup"><span data-stu-id="1dcdf-129">-Name</span></span>
<span data-ttu-id="1dcdf-130">A jegyzetfüzet neve.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-130">The notebook name.</span></span>

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

### <span data-ttu-id="1dcdf-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="1dcdf-131">-OutputFolder</span></span>
<span data-ttu-id="1dcdf-132">Az a mappa, ahová a jegyzetfüzetet el kell helyezni.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="1dcdf-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1dcdf-133">-WorkspaceName</span></span>
<span data-ttu-id="1dcdf-134">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1dcdf-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1dcdf-135">-WorkspaceObject</span></span>
<span data-ttu-id="1dcdf-136">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1dcdf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dcdf-137">CommonParameters</span></span>
<span data-ttu-id="1dcdf-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dcdf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dcdf-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1dcdf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dcdf-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1dcdf-140">INPUTS</span></span>

### <span data-ttu-id="1dcdf-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1dcdf-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1dcdf-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="1dcdf-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="1dcdf-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1dcdf-143">OUTPUTS</span></span>

### <span data-ttu-id="1dcdf-144">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="1dcdf-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="1dcdf-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1dcdf-145">NOTES</span></span>

## <span data-ttu-id="1dcdf-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1dcdf-146">RELATED LINKS</span></span>
