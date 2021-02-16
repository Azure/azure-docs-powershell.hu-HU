---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 6fdb2a51354df01c308629eaedb09cba3a8d2fdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157827"
---
# <span data-ttu-id="62dcf-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="62dcf-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="62dcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="62dcf-103">Synapse Analytics szerepkör-hozzárendelést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="62dcf-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="62dcf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="62dcf-104">SYNTAX</span></span>

### <span data-ttu-id="62dcf-105">NewByWorkspaceNameAndNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="62dcf-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62dcf-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62dcf-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62dcf-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62dcf-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62dcf-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="62dcf-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62dcf-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="62dcf-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62dcf-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62dcf-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62dcf-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62dcf-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62dcf-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="62dcf-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62dcf-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="62dcf-113">DESCRIPTION</span></span>
<span data-ttu-id="62dcf-114">A **New-AzSynapseRoleAssignment** parancsmag létrehoz egy Azure Synapse Analytics szerepkör-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="62dcf-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="62dcf-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="62dcf-115">EXAMPLES</span></span>

### <span data-ttu-id="62dcf-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="62dcf-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="62dcf-117">Ez a parancs hozzárendeli a ContosoRole nevet ahhoz a felhasználóhoz, akinek a neve ContosoName.</span><span class="sxs-lookup"><span data-stu-id="62dcf-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="62dcf-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="62dcf-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="62dcf-119">Ez a parancs hozzárendeli a ContosoRole-t ahhoz a felhasználóhoz, akinek a fő neve ContosoName a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="62dcf-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="62dcf-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62dcf-120">PARAMETERS</span></span>

### <span data-ttu-id="62dcf-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62dcf-121">-AsJob</span></span>
<span data-ttu-id="62dcf-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="62dcf-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62dcf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62dcf-123">-DefaultProfile</span></span>
<span data-ttu-id="62dcf-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62dcf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62dcf-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="62dcf-125">-ObjectId</span></span>
<span data-ttu-id="62dcf-126">A felhasználó, csoport vagy szolgáltatásnév Azure AD-objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="62dcf-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62dcf-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="62dcf-127">-RoleDefinitionId</span></span>
<span data-ttu-id="62dcf-128">A főnévhez hozzárendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="62dcf-128">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62dcf-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="62dcf-129">-RoleDefinitionName</span></span>
<span data-ttu-id="62dcf-130">A főnévhez hozzárendelt szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="62dcf-130">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62dcf-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="62dcf-131">-ServicePrincipalName</span></span>
<span data-ttu-id="62dcf-132">A szolgáltatásnév ServicePrincipalName tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="62dcf-132">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62dcf-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="62dcf-133">-SignInName</span></span>
<span data-ttu-id="62dcf-134">A felhasználó e-mail-címe vagy egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="62dcf-134">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62dcf-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="62dcf-135">-WorkspaceName</span></span>
<span data-ttu-id="62dcf-136">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="62dcf-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62dcf-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="62dcf-137">-WorkspaceObject</span></span>
<span data-ttu-id="62dcf-138">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="62dcf-138">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62dcf-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62dcf-139">-Confirm</span></span>
<span data-ttu-id="62dcf-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="62dcf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62dcf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62dcf-141">-WhatIf</span></span>
<span data-ttu-id="62dcf-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="62dcf-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62dcf-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62dcf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62dcf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62dcf-144">CommonParameters</span></span>
<span data-ttu-id="62dcf-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62dcf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62dcf-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62dcf-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62dcf-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62dcf-147">INPUTS</span></span>

### <span data-ttu-id="62dcf-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="62dcf-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="62dcf-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62dcf-149">OUTPUTS</span></span>

### <span data-ttu-id="62dcf-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="62dcf-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="62dcf-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="62dcf-151">NOTES</span></span>

## <span data-ttu-id="62dcf-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62dcf-152">RELATED LINKS</span></span>
