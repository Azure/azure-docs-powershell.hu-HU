---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: 061cd16f4a2c9099be73fa2c2bdb54ff9f089949
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008261"
---
# <span data-ttu-id="299e7-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="299e7-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="299e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="299e7-102">SYNOPSIS</span></span>
<span data-ttu-id="299e7-103">Synapse Analytics szerepkördefiníciót kap.</span><span class="sxs-lookup"><span data-stu-id="299e7-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="299e7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="299e7-104">SYNTAX</span></span>

### <span data-ttu-id="299e7-105">GetByWorkspaceNameAndIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="299e7-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="299e7-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="299e7-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="299e7-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="299e7-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="299e7-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="299e7-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="299e7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="299e7-109">DESCRIPTION</span></span>
<span data-ttu-id="299e7-110">A **Get-AzSynapseRoleDefinition** parancsmag egy Azure Synapse Analytics szerepkördefiníciót kap.</span><span class="sxs-lookup"><span data-stu-id="299e7-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="299e7-111">Ha nem ad meg szerepkörnevet vagy szerepkörazonosítót, ez a parancsmag az összes szerepkördefiníciót megkapja.</span><span class="sxs-lookup"><span data-stu-id="299e7-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="299e7-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="299e7-112">EXAMPLES</span></span>

### <span data-ttu-id="299e7-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="299e7-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="299e7-114">Ez a parancs munkaterületen kapja meg az összes szerepkördefiníciót.</span><span class="sxs-lookup"><span data-stu-id="299e7-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="299e7-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="299e7-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="299e7-116">Ez a parancs a ContosoWorkspace munkaterület szerepkör-definícióját kapja ContosoRole néven.</span><span class="sxs-lookup"><span data-stu-id="299e7-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="299e7-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="299e7-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="299e7-118">Ez a parancs a munkaterületek szerepkör-definícióit folyamaton keresztül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="299e7-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="299e7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="299e7-119">PARAMETERS</span></span>

### <span data-ttu-id="299e7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299e7-120">-DefaultProfile</span></span>
<span data-ttu-id="299e7-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="299e7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="299e7-122">-Id</span><span class="sxs-lookup"><span data-stu-id="299e7-122">-Id</span></span>
<span data-ttu-id="299e7-123">A főnévhez hozzárendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="299e7-123">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="299e7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="299e7-124">-Name</span></span>
<span data-ttu-id="299e7-125">A főnévhez hozzárendelt szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="299e7-125">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="299e7-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="299e7-126">-WorkspaceName</span></span>
<span data-ttu-id="299e7-127">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="299e7-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="299e7-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="299e7-128">-WorkspaceObject</span></span>
<span data-ttu-id="299e7-129">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="299e7-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="299e7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299e7-130">CommonParameters</span></span>
<span data-ttu-id="299e7-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="299e7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299e7-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="299e7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299e7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="299e7-133">INPUTS</span></span>

### <span data-ttu-id="299e7-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="299e7-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="299e7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="299e7-135">OUTPUTS</span></span>

### <span data-ttu-id="299e7-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="299e7-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="299e7-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="299e7-137">NOTES</span></span>

## <span data-ttu-id="299e7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="299e7-138">RELATED LINKS</span></span>
