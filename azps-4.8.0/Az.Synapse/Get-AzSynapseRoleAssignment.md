---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017481"
---
# <span data-ttu-id="d5f80-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d5f80-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="d5f80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5f80-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f80-103">A szinapszis-Analytics szerepkör-hozzárendelést kapja.</span><span class="sxs-lookup"><span data-stu-id="d5f80-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="d5f80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5f80-104">SYNTAX</span></span>

### <span data-ttu-id="d5f80-105">GetByWorkspaceNameAndNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5f80-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f80-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f80-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f80-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f80-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f80-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f80-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f80-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f80-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f80-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f80-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f80-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f80-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f80-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f80-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f80-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f80-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f80-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5f80-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5f80-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5f80-115">DESCRIPTION</span></span>
<span data-ttu-id="d5f80-116">A **Get-AzSynapseRoleAssignment** parancsmag az Azure szinapszis Analytics szerepkör-hozzárendelést kapja.</span><span class="sxs-lookup"><span data-stu-id="d5f80-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="d5f80-117">Ha nem ad meg szerepkör-definíciót vagy egyszerű felhasználónevet, a parancsmag minden szerepkör-hozzárendelést kap.</span><span class="sxs-lookup"><span data-stu-id="d5f80-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="d5f80-118">Példák</span><span class="sxs-lookup"><span data-stu-id="d5f80-118">EXAMPLES</span></span>

### <span data-ttu-id="d5f80-119">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d5f80-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d5f80-120">Ez a parancs a munkaterület alatti összes szerepkör-hozzárendelést beilleszti.</span><span class="sxs-lookup"><span data-stu-id="d5f80-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="d5f80-121">2. példa</span><span class="sxs-lookup"><span data-stu-id="d5f80-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="d5f80-122">Ez a parancs minden szerepkör-hozzárendelést beilleszt a munkaterület ContosoWorkspace a role Name ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="d5f80-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="d5f80-123">3. példa</span><span class="sxs-lookup"><span data-stu-id="d5f80-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="d5f80-124">Ez a parancs szerepkör-hozzárendelést kap a munkaterületi ContosoWorkspace a role Name ContosoRole és a User principal name ContosoName.</span><span class="sxs-lookup"><span data-stu-id="d5f80-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="d5f80-125">4. példa</span><span class="sxs-lookup"><span data-stu-id="d5f80-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="d5f80-126">Ez a parancs minden szerepkör-hozzárendelést beilleszt a munkaterületre a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="d5f80-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="d5f80-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5f80-127">PARAMETERS</span></span>

### <span data-ttu-id="d5f80-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f80-128">-DefaultProfile</span></span>
<span data-ttu-id="d5f80-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5f80-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5f80-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d5f80-130">-ObjectId</span></span>
<span data-ttu-id="d5f80-131">Az Azure AD ObjectId a felhasználó, a csoport vagy a szolgáltatás megbízójának</span><span class="sxs-lookup"><span data-stu-id="d5f80-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="d5f80-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="d5f80-132">-RoleAssignmentId</span></span>
<span data-ttu-id="d5f80-133">A szerepkör-hozzárendelés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d5f80-133">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="d5f80-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d5f80-134">-RoleDefinitionId</span></span>
<span data-ttu-id="d5f80-135">A megbízóhoz rendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d5f80-135">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="d5f80-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d5f80-136">-RoleDefinitionName</span></span>
<span data-ttu-id="d5f80-137">A megbízóhoz rendelt szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="d5f80-137">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="d5f80-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d5f80-138">-ServicePrincipalName</span></span>
<span data-ttu-id="d5f80-139">A ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="d5f80-139">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="d5f80-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="d5f80-140">-SignInName</span></span>
<span data-ttu-id="d5f80-141">Az e-mail-cím vagy a felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="d5f80-141">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="d5f80-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d5f80-142">-WorkspaceName</span></span>
<span data-ttu-id="d5f80-143">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="d5f80-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d5f80-144">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d5f80-144">-WorkspaceObject</span></span>
<span data-ttu-id="d5f80-145">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="d5f80-145">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d5f80-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f80-146">CommonParameters</span></span>
<span data-ttu-id="d5f80-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5f80-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f80-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d5f80-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f80-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5f80-149">INPUTS</span></span>

### <span data-ttu-id="d5f80-150">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d5f80-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d5f80-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5f80-151">OUTPUTS</span></span>

### <span data-ttu-id="d5f80-152">Microsoft. Azure. commands. szinapszis. models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="d5f80-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="d5f80-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5f80-153">NOTES</span></span>

## <span data-ttu-id="d5f80-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5f80-154">RELATED LINKS</span></span>
