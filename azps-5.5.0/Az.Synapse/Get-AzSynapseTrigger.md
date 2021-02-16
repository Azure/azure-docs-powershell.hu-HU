---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157858"
---
# <span data-ttu-id="e5246-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="e5246-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="e5246-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5246-102">SYNOPSIS</span></span>
<span data-ttu-id="e5246-103">Információkat kap a munkaterületen található eseményindítókról.</span><span class="sxs-lookup"><span data-stu-id="e5246-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="e5246-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5246-104">SYNTAX</span></span>

### <span data-ttu-id="e5246-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5246-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5246-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="e5246-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5246-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5246-107">DESCRIPTION</span></span>
<span data-ttu-id="e5246-108">A **Get-AzSynapseTrigger** parancsmag információt kap a munkaterületen található eseményindítókról.</span><span class="sxs-lookup"><span data-stu-id="e5246-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="e5246-109">Ha megadja egy eseményindító nevét, a parancsmag információt kap az eseményindítóról.</span><span class="sxs-lookup"><span data-stu-id="e5246-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="e5246-110">Ha nem ad meg nevet, a parancsmag információt kap a munkaterületen található összes eseményindítóról.</span><span class="sxs-lookup"><span data-stu-id="e5246-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="e5246-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5246-111">EXAMPLES</span></span>

### <span data-ttu-id="e5246-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="e5246-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e5246-113">A ContosoWorkspace munkaterületen létrehozott összes eseményindítót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e5246-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e5246-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e5246-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="e5246-115">Egyetlen ContosoTrigger nevű eseményindítót kap a ContosoWorkspace munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="e5246-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e5246-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="e5246-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="e5246-117">Egyetlen ContosoTrigger nevű eseményindítót kap a munkaterületen a ContosoWorkspace folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="e5246-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e5246-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5246-118">PARAMETERS</span></span>

### <span data-ttu-id="e5246-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5246-119">-DefaultProfile</span></span>
<span data-ttu-id="e5246-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5246-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5246-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e5246-121">-Name</span></span>
<span data-ttu-id="e5246-122">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="e5246-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5246-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e5246-123">-WorkspaceName</span></span>
<span data-ttu-id="e5246-124">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e5246-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e5246-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e5246-125">-WorkspaceObject</span></span>
<span data-ttu-id="e5246-126">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="e5246-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e5246-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5246-127">CommonParameters</span></span>
<span data-ttu-id="e5246-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5246-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5246-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5246-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5246-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5246-130">INPUTS</span></span>

### <span data-ttu-id="e5246-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e5246-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e5246-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5246-132">OUTPUTS</span></span>

### <span data-ttu-id="e5246-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="e5246-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="e5246-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5246-134">NOTES</span></span>

## <span data-ttu-id="e5246-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5246-135">RELATED LINKS</span></span>
