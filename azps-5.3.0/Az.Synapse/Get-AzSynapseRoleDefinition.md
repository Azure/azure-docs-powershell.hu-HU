---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384004"
---
# <span data-ttu-id="93bed-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="93bed-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="93bed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93bed-102">SYNOPSIS</span></span>
<span data-ttu-id="93bed-103">Synapse Analytics szerepkördefiníciót kap.</span><span class="sxs-lookup"><span data-stu-id="93bed-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="93bed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93bed-104">SYNTAX</span></span>

### <span data-ttu-id="93bed-105">GetByWorkspaceNameAndIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93bed-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93bed-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="93bed-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93bed-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93bed-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93bed-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="93bed-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93bed-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93bed-109">DESCRIPTION</span></span>
<span data-ttu-id="93bed-110">A **Get-AzSynapseRoleDefinition** parancsmag egy Azure Synapse Analytics szerepkördefiníciót kap.</span><span class="sxs-lookup"><span data-stu-id="93bed-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="93bed-111">Ha nem ad meg szerepkörnevet vagy szerepkörazonosítót, ez a parancsmag az összes szerepkördefiníciót megkapja.</span><span class="sxs-lookup"><span data-stu-id="93bed-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="93bed-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93bed-112">EXAMPLES</span></span>

### <span data-ttu-id="93bed-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="93bed-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="93bed-114">Ez a parancs munkaterület alatt kapja meg az összes szerepkördefiníciót.</span><span class="sxs-lookup"><span data-stu-id="93bed-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="93bed-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="93bed-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="93bed-116">Ez a parancs a ContosoWorkspace munkaterület szerepkör-definícióját kapja ContosoRole néven.</span><span class="sxs-lookup"><span data-stu-id="93bed-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="93bed-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="93bed-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="93bed-118">Ez a parancs a munkaterületek szerepkör-definícióit folyamaton keresztül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="93bed-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="93bed-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93bed-119">PARAMETERS</span></span>

### <span data-ttu-id="93bed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93bed-120">-DefaultProfile</span></span>
<span data-ttu-id="93bed-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93bed-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93bed-122">-Id</span><span class="sxs-lookup"><span data-stu-id="93bed-122">-Id</span></span>
<span data-ttu-id="93bed-123">A főnévhez hozzárendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="93bed-123">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bed-124">-Name</span><span class="sxs-lookup"><span data-stu-id="93bed-124">-Name</span></span>
<span data-ttu-id="93bed-125">A főnévhez hozzárendelt szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="93bed-125">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bed-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="93bed-126">-WorkspaceName</span></span>
<span data-ttu-id="93bed-127">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="93bed-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bed-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="93bed-128">-WorkspaceObject</span></span>
<span data-ttu-id="93bed-129">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="93bed-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93bed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93bed-130">CommonParameters</span></span>
<span data-ttu-id="93bed-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93bed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93bed-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93bed-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93bed-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93bed-133">INPUTS</span></span>

### <span data-ttu-id="93bed-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="93bed-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="93bed-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93bed-135">OUTPUTS</span></span>

### <span data-ttu-id="93bed-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="93bed-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="93bed-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93bed-137">NOTES</span></span>

## <span data-ttu-id="93bed-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93bed-138">RELATED LINKS</span></span>
