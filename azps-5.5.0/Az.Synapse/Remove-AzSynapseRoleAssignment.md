---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149962"
---
# <span data-ttu-id="fcdf7-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fcdf7-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="fcdf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcdf7-102">SYNOPSIS</span></span>
<span data-ttu-id="fcdf7-103">A Synapse Analytics szerepkör-hozzárendelésének törlése.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="fcdf7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fcdf7-104">SYNTAX</span></span>

### <span data-ttu-id="fcdf7-105">RemoveByWorkspaceNameAndNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fcdf7-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcdf7-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcdf7-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcdf7-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcdf7-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcdf7-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcdf7-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcdf7-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcdf7-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcdf7-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcdf7-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcdf7-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcdf7-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcdf7-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcdf7-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcdf7-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcdf7-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcdf7-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcdf7-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcdf7-115">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fcdf7-115">DESCRIPTION</span></span>
<span data-ttu-id="fcdf7-116">A **Remove-AzSynapseRoleAssignment** parancsmag véglegesen törli az Azure Synapse Analytics szerepkör-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="fcdf7-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fcdf7-117">EXAMPLES</span></span>

### <span data-ttu-id="fcdf7-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="fcdf7-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="fcdf7-119">Ez a parancs törli az Azure Synapse Analytics szerepkör-hozzárendelést egy szerepkör-hozzárendelés-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="fcdf7-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="fcdf7-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="fcdf7-121">Ez a parancs törli az Azure Synapse Analytics szerepkör-hozzárendelést egy szerepkörnévvel és egy egyszerű felhasználónévvel.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="fcdf7-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="fcdf7-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="fcdf7-123">Ez a parancs törli az Azure Synapse Analytics szerepkör-hozzárendelést egy szerepkör-hozzárendelés-azonosítóval a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="fcdf7-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcdf7-124">PARAMETERS</span></span>

### <span data-ttu-id="fcdf7-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcdf7-125">-AsJob</span></span>
<span data-ttu-id="fcdf7-126">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fcdf7-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fcdf7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcdf7-127">-DefaultProfile</span></span>
<span data-ttu-id="fcdf7-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcdf7-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fcdf7-129">-ObjectId</span></span>
<span data-ttu-id="fcdf7-130">A felhasználó, csoport vagy szolgáltatásnév Azure AD-objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdf7-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcdf7-131">-PassThru</span></span>
<span data-ttu-id="fcdf7-132">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fcdf7-133">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fcdf7-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="fcdf7-134">-RoleAssignmentId</span></span>
<span data-ttu-id="fcdf7-135">A szerepkör-hozzárendelés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-135">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdf7-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="fcdf7-136">-RoleDefinitionId</span></span>
<span data-ttu-id="fcdf7-137">A főnévhez hozzárendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-137">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdf7-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="fcdf7-138">-RoleDefinitionName</span></span>
<span data-ttu-id="fcdf7-139">A főnévhez hozzárendelt szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-139">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdf7-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fcdf7-140">-ServicePrincipalName</span></span>
<span data-ttu-id="fcdf7-141">A szolgáltatásnév ServicePrincipalName tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-141">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdf7-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="fcdf7-142">-SignInName</span></span>
<span data-ttu-id="fcdf7-143">A felhasználó e-mail-címe vagy egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-143">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdf7-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fcdf7-144">-WorkspaceName</span></span>
<span data-ttu-id="fcdf7-145">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdf7-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fcdf7-146">-WorkspaceObject</span></span>
<span data-ttu-id="fcdf7-147">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByWorkspaceObjectAndIdParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcdf7-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcdf7-148">-Confirm</span></span>
<span data-ttu-id="fcdf7-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcdf7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcdf7-150">-WhatIf</span></span>
<span data-ttu-id="fcdf7-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcdf7-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcdf7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcdf7-153">CommonParameters</span></span>
<span data-ttu-id="fcdf7-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcdf7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcdf7-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcdf7-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcdf7-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fcdf7-156">INPUTS</span></span>

### <span data-ttu-id="fcdf7-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fcdf7-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fcdf7-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcdf7-158">OUTPUTS</span></span>

### <span data-ttu-id="fcdf7-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fcdf7-159">System.Boolean</span></span>

## <span data-ttu-id="fcdf7-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fcdf7-160">NOTES</span></span>

## <span data-ttu-id="fcdf7-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcdf7-161">RELATED LINKS</span></span>
