---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: 2171f99da156d86161773b039edeb884dee7a7e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928425"
---
# <span data-ttu-id="6b5c9-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6b5c9-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="6b5c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b5c9-102">SYNOPSIS</span></span>
<span data-ttu-id="6b5c9-103">Synapse Analytics-szerepkör-hozzárendelést kap.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="6b5c9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b5c9-104">SYNTAX</span></span>

### <span data-ttu-id="6b5c9-105">GetByWorkspaceNameAndNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b5c9-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b5c9-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b5c9-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b5c9-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b5c9-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b5c9-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b5c9-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b5c9-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b5c9-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b5c9-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b5c9-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b5c9-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b5c9-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b5c9-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b5c9-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b5c9-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b5c9-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b5c9-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b5c9-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b5c9-115">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b5c9-115">DESCRIPTION</span></span>
<span data-ttu-id="6b5c9-116">A **Get-AzSynapseRoleAssignment** parancsmag azure Synapse Analytics szerepkör-hozzárendelést kap.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="6b5c9-117">Ha nem ad meg szerepkördefiníciót vagy egyszerű felhasználónevet, ez a parancsmag kapja meg az összes szerepkör-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="6b5c9-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b5c9-118">EXAMPLES</span></span>

### <span data-ttu-id="6b5c9-119">1. példa</span><span class="sxs-lookup"><span data-stu-id="6b5c9-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="6b5c9-120">Ez a parancs munkaterületen kapja meg az összes szerepkör-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="6b5c9-121">2. példa</span><span class="sxs-lookup"><span data-stu-id="6b5c9-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="6b5c9-122">Ez a parancs az összes szerepkör-hozzárendelést a ContosoWorkspace munkaterületen kapja meg ContosoRole szerepkörnévvel.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="6b5c9-123">3. példa</span><span class="sxs-lookup"><span data-stu-id="6b5c9-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="6b5c9-124">Ez a parancs szerepkör-hozzárendelést kap a ContosoWorkspace munkaterületen ContosoRole szerepkörnévvel és ContosoName felhasználónévvel.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="6b5c9-125">4. példa</span><span class="sxs-lookup"><span data-stu-id="6b5c9-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="6b5c9-126">Ez a parancs az összes szerepkör-hozzárendelést egy munkaterületen keresztül kapja meg folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="6b5c9-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b5c9-127">PARAMETERS</span></span>

### <span data-ttu-id="6b5c9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b5c9-128">-DefaultProfile</span></span>
<span data-ttu-id="6b5c9-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b5c9-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6b5c9-130">-ObjectId</span></span>
<span data-ttu-id="6b5c9-131">A felhasználó, csoport vagy szolgáltatásnév Azure AD-objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b5c9-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="6b5c9-132">-RoleAssignmentId</span></span>
<span data-ttu-id="6b5c9-133">A szerepkör-hozzárendelés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-133">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b5c9-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6b5c9-134">-RoleDefinitionId</span></span>
<span data-ttu-id="6b5c9-135">A főnévhez hozzárendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-135">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b5c9-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6b5c9-136">-RoleDefinitionName</span></span>
<span data-ttu-id="6b5c9-137">A főnévhez hozzárendelt szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-137">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet, GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b5c9-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="6b5c9-138">-ServicePrincipalName</span></span>
<span data-ttu-id="6b5c9-139">A szolgáltatásnév ServicePrincipalName tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-139">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b5c9-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="6b5c9-140">-SignInName</span></span>
<span data-ttu-id="6b5c9-141">A felhasználó e-mail-címe vagy egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-141">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b5c9-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6b5c9-142">-WorkspaceName</span></span>
<span data-ttu-id="6b5c9-143">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-143">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b5c9-144">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6b5c9-144">-WorkspaceObject</span></span>
<span data-ttu-id="6b5c9-145">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-145">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b5c9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b5c9-146">CommonParameters</span></span>
<span data-ttu-id="6b5c9-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b5c9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b5c9-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b5c9-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b5c9-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b5c9-149">INPUTS</span></span>

### <span data-ttu-id="6b5c9-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6b5c9-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6b5c9-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b5c9-151">OUTPUTS</span></span>

### <span data-ttu-id="6b5c9-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="6b5c9-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="6b5c9-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b5c9-153">NOTES</span></span>

## <span data-ttu-id="6b5c9-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b5c9-154">RELATED LINKS</span></span>
