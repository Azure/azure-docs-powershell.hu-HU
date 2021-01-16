---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339186"
---
# <span data-ttu-id="9ed94-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="9ed94-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="9ed94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ed94-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed94-103">Információkat kap a munkaterületen lévő jegyzetfüzetekkel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="9ed94-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="9ed94-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9ed94-104">SYNTAX</span></span>

### <span data-ttu-id="9ed94-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ed94-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ed94-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="9ed94-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ed94-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9ed94-107">DESCRIPTION</span></span>
<span data-ttu-id="9ed94-108">A **Get-AzSynapseNotebook** parancsmag információt kap a munkaterületen található jegyzetfüzetekkel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="9ed94-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="9ed94-109">Ha megadja egy jegyzetfüzet nevét, a parancsmag információt kap a jegyzetfüzetről.</span><span class="sxs-lookup"><span data-stu-id="9ed94-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="9ed94-110">Ha nem ad meg nevet, a parancsmag információt kap a munkaterületen található összes jegyzetfüzetről.</span><span class="sxs-lookup"><span data-stu-id="9ed94-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="9ed94-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9ed94-111">EXAMPLES</span></span>

### <span data-ttu-id="9ed94-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="9ed94-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="9ed94-113">A ContosoWorkspace munkaterületen lévő összes jegyzetfüzet listáját beveszi.</span><span class="sxs-lookup"><span data-stu-id="9ed94-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="9ed94-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="9ed94-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="9ed94-115">Egyetlen ContosoNotebook nevű jegyzetfüzetet kap a ContosoWorkspace munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="9ed94-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="9ed94-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="9ed94-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="9ed94-117">Egyetlen ContosoNotebook nevű jegyzetfüzetet kap a munkaterületen a ContosoWorkspace folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="9ed94-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="9ed94-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ed94-118">PARAMETERS</span></span>

### <span data-ttu-id="9ed94-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed94-119">-DefaultProfile</span></span>
<span data-ttu-id="9ed94-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ed94-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ed94-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9ed94-121">-Name</span></span>
<span data-ttu-id="9ed94-122">A jegyzetfüzet neve.</span><span class="sxs-lookup"><span data-stu-id="9ed94-122">The notebook name.</span></span>

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

### <span data-ttu-id="9ed94-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9ed94-123">-WorkspaceName</span></span>
<span data-ttu-id="9ed94-124">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="9ed94-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed94-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9ed94-125">-WorkspaceObject</span></span>
<span data-ttu-id="9ed94-126">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="9ed94-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed94-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed94-127">CommonParameters</span></span>
<span data-ttu-id="9ed94-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ed94-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed94-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ed94-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed94-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ed94-130">INPUTS</span></span>

### <span data-ttu-id="9ed94-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9ed94-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9ed94-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ed94-132">OUTPUTS</span></span>

### <span data-ttu-id="9ed94-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="9ed94-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="9ed94-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9ed94-134">NOTES</span></span>

## <span data-ttu-id="9ed94-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ed94-135">RELATED LINKS</span></span>
