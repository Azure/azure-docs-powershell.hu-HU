---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303953"
---
# <span data-ttu-id="22fc0-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="22fc0-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="22fc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="22fc0-103">Egy szinapszis-Analytics szerepkör-hozzárendelés törlése</span><span class="sxs-lookup"><span data-stu-id="22fc0-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="22fc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22fc0-104">SYNTAX</span></span>

### <span data-ttu-id="22fc0-105">RemoveByWorkspaceNameAndNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22fc0-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22fc0-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22fc0-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22fc0-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22fc0-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22fc0-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22fc0-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22fc0-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="22fc0-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22fc0-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22fc0-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22fc0-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="22fc0-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22fc0-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22fc0-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22fc0-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22fc0-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22fc0-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="22fc0-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22fc0-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="22fc0-115">DESCRIPTION</span></span>
<span data-ttu-id="22fc0-116">A **Remove-AzSynapseRoleAssignment** parancsmag véglegesen törli az Azure szinapszis Analytics szerepkör-hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="22fc0-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="22fc0-117">Példák</span><span class="sxs-lookup"><span data-stu-id="22fc0-117">EXAMPLES</span></span>

### <span data-ttu-id="22fc0-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="22fc0-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="22fc0-119">Ez a parancs törli az Azure szinapszis-beli Analytics szerepkör-hozzárendelést egy szerepkör-hozzárendelési azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="22fc0-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="22fc0-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="22fc0-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="22fc0-121">Ez a parancs törli az Azure szinapszis-Analytics szerepkör-hozzárendelését egy szerepkör nevével és egy egyszerű felhasználó nevével.</span><span class="sxs-lookup"><span data-stu-id="22fc0-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="22fc0-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="22fc0-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="22fc0-123">Ez a parancs törli az Azure szinapszis Analytics szerepkör-hozzárendelést egy szerepkör-hozzárendelési azonosítóval a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="22fc0-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="22fc0-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22fc0-124">PARAMETERS</span></span>

### <span data-ttu-id="22fc0-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22fc0-125">-AsJob</span></span>
<span data-ttu-id="22fc0-126">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="22fc0-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22fc0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22fc0-127">-DefaultProfile</span></span>
<span data-ttu-id="22fc0-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22fc0-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22fc0-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="22fc0-129">-ObjectId</span></span>
<span data-ttu-id="22fc0-130">Az Azure AD ObjectId a felhasználó, a csoport vagy a szolgáltatás megbízójának</span><span class="sxs-lookup"><span data-stu-id="22fc0-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="22fc0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22fc0-131">-PassThru</span></span>
<span data-ttu-id="22fc0-132">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="22fc0-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="22fc0-133">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="22fc0-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="22fc0-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="22fc0-134">-RoleAssignmentId</span></span>
<span data-ttu-id="22fc0-135">A szerepkör-hozzárendelés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="22fc0-135">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="22fc0-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="22fc0-136">-RoleDefinitionId</span></span>
<span data-ttu-id="22fc0-137">A megbízóhoz rendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="22fc0-137">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="22fc0-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="22fc0-138">-RoleDefinitionName</span></span>
<span data-ttu-id="22fc0-139">A megbízóhoz rendelt szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="22fc0-139">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="22fc0-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="22fc0-140">-ServicePrincipalName</span></span>
<span data-ttu-id="22fc0-141">A ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="22fc0-141">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="22fc0-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="22fc0-142">-SignInName</span></span>
<span data-ttu-id="22fc0-143">Az e-mail-cím vagy a felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="22fc0-143">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="22fc0-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="22fc0-144">-WorkspaceName</span></span>
<span data-ttu-id="22fc0-145">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="22fc0-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="22fc0-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="22fc0-146">-WorkspaceObject</span></span>
<span data-ttu-id="22fc0-147">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="22fc0-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="22fc0-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="22fc0-148">-Confirm</span></span>
<span data-ttu-id="22fc0-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="22fc0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22fc0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22fc0-150">-WhatIf</span></span>
<span data-ttu-id="22fc0-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="22fc0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22fc0-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22fc0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22fc0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22fc0-153">CommonParameters</span></span>
<span data-ttu-id="22fc0-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22fc0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22fc0-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="22fc0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22fc0-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22fc0-156">INPUTS</span></span>

### <span data-ttu-id="22fc0-157">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="22fc0-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="22fc0-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22fc0-158">OUTPUTS</span></span>

### <span data-ttu-id="22fc0-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22fc0-159">System.Boolean</span></span>

## <span data-ttu-id="22fc0-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22fc0-160">NOTES</span></span>

## <span data-ttu-id="22fc0-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22fc0-161">RELATED LINKS</span></span>
