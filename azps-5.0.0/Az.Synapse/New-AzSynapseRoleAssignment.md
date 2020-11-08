---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 6fdb2a51354df01c308629eaedb09cba3a8d2fdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186317"
---
# <span data-ttu-id="f5d59-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f5d59-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="f5d59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5d59-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d59-103">Egy szinapszis-Analytics szerepkör-hozzárendelést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f5d59-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="f5d59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5d59-104">SYNTAX</span></span>

### <span data-ttu-id="f5d59-105">NewByWorkspaceNameAndNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5d59-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5d59-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5d59-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5d59-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5d59-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5d59-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5d59-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5d59-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5d59-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5d59-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5d59-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5d59-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5d59-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5d59-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5d59-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5d59-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5d59-113">DESCRIPTION</span></span>
<span data-ttu-id="f5d59-114">A **New-AzSynapseRoleAssignment** parancsmag létrehoz egy Azure szinapszis-Analytics szerepkör-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="f5d59-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="f5d59-115">Példák</span><span class="sxs-lookup"><span data-stu-id="f5d59-115">EXAMPLES</span></span>

### <span data-ttu-id="f5d59-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f5d59-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="f5d59-117">Ez a parancs a ContosoRole társítja a felhasználóhoz, akinek az elsődleges neve ContosoName.</span><span class="sxs-lookup"><span data-stu-id="f5d59-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="f5d59-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="f5d59-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="f5d59-119">Ez a parancs a ContosoRole társítja a felhasználóhoz, akinek az elsődleges neve ContosoName keresztül.</span><span class="sxs-lookup"><span data-stu-id="f5d59-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="f5d59-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5d59-120">PARAMETERS</span></span>

### <span data-ttu-id="f5d59-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5d59-121">-AsJob</span></span>
<span data-ttu-id="f5d59-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f5d59-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5d59-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d59-123">-DefaultProfile</span></span>
<span data-ttu-id="f5d59-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5d59-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5d59-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f5d59-125">-ObjectId</span></span>
<span data-ttu-id="f5d59-126">Az Azure AD ObjectId a felhasználó, a csoport vagy a szolgáltatás megbízójának</span><span class="sxs-lookup"><span data-stu-id="f5d59-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="f5d59-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f5d59-127">-RoleDefinitionId</span></span>
<span data-ttu-id="f5d59-128">A megbízóhoz rendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f5d59-128">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="f5d59-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f5d59-129">-RoleDefinitionName</span></span>
<span data-ttu-id="f5d59-130">A megbízóhoz rendelt szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="f5d59-130">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="f5d59-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f5d59-131">-ServicePrincipalName</span></span>
<span data-ttu-id="f5d59-132">A ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="f5d59-132">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="f5d59-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="f5d59-133">-SignInName</span></span>
<span data-ttu-id="f5d59-134">Az e-mail-cím vagy a felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="f5d59-134">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="f5d59-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5d59-135">-WorkspaceName</span></span>
<span data-ttu-id="f5d59-136">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="f5d59-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f5d59-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f5d59-137">-WorkspaceObject</span></span>
<span data-ttu-id="f5d59-138">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="f5d59-138">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f5d59-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5d59-139">-Confirm</span></span>
<span data-ttu-id="f5d59-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5d59-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5d59-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5d59-141">-WhatIf</span></span>
<span data-ttu-id="f5d59-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5d59-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5d59-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5d59-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5d59-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d59-144">CommonParameters</span></span>
<span data-ttu-id="f5d59-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5d59-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d59-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f5d59-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d59-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5d59-147">INPUTS</span></span>

### <span data-ttu-id="f5d59-148">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f5d59-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f5d59-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5d59-149">OUTPUTS</span></span>

### <span data-ttu-id="f5d59-150">Microsoft. Azure. commands. szinapszis. models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="f5d59-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="f5d59-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5d59-151">NOTES</span></span>

## <span data-ttu-id="f5d59-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5d59-152">RELATED LINKS</span></span>
