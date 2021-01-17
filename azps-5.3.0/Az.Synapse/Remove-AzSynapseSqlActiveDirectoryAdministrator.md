---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 21d7169f18a999f84adbc568da18c90cb2aa2424
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383402"
---
# <span data-ttu-id="7914e-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7914e-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="7914e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7914e-102">SYNOPSIS</span></span>
<span data-ttu-id="7914e-103">Eltávolítja a Synapse Analytics Workspace Azure AD-rendszergazdáját.</span><span class="sxs-lookup"><span data-stu-id="7914e-103">Removes an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="7914e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7914e-104">SYNTAX</span></span>

### <span data-ttu-id="7914e-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7914e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7914e-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7914e-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7914e-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7914e-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7914e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7914e-108">DESCRIPTION</span></span>
<span data-ttu-id="7914e-109">A **Remove-AzSynapseSqlActiveDirectoryAdministrator** parancsmag eltávolítja az Azure Synapse Analytics Workspace Azure Active Directory (Azure AD) rendszergazdáját.</span><span class="sxs-lookup"><span data-stu-id="7914e-109">The **Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="7914e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7914e-110">EXAMPLES</span></span>

### <span data-ttu-id="7914e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7914e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="7914e-112">Ez a parancs eltávolítja a ContosoWorkspace nevű munkaterület Azure AD-rendszergazdáját.</span><span class="sxs-lookup"><span data-stu-id="7914e-112">This command removes the Azure AD administrator for the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="7914e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7914e-113">PARAMETERS</span></span>

### <span data-ttu-id="7914e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7914e-114">-AsJob</span></span>
<span data-ttu-id="7914e-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7914e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7914e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7914e-116">-DefaultProfile</span></span>
<span data-ttu-id="7914e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7914e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7914e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7914e-118">-Force</span></span>
<span data-ttu-id="7914e-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7914e-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7914e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7914e-120">-InputObject</span></span>
<span data-ttu-id="7914e-121">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="7914e-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7914e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7914e-122">-PassThru</span></span>
<span data-ttu-id="7914e-123">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="7914e-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7914e-124">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="7914e-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7914e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7914e-125">-ResourceGroupName</span></span>
<span data-ttu-id="7914e-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7914e-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7914e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7914e-127">-ResourceId</span></span>
<span data-ttu-id="7914e-128">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7914e-128">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7914e-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7914e-129">-WorkspaceName</span></span>
<span data-ttu-id="7914e-130">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="7914e-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7914e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7914e-131">-Confirm</span></span>
<span data-ttu-id="7914e-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7914e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7914e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7914e-133">-WhatIf</span></span>
<span data-ttu-id="7914e-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7914e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7914e-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7914e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7914e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7914e-136">CommonParameters</span></span>
<span data-ttu-id="7914e-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7914e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7914e-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7914e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7914e-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7914e-139">INPUTS</span></span>

### <span data-ttu-id="7914e-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7914e-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7914e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7914e-141">OUTPUTS</span></span>

### <span data-ttu-id="7914e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7914e-142">System.Boolean</span></span>

## <span data-ttu-id="7914e-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7914e-143">NOTES</span></span>

## <span data-ttu-id="7914e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7914e-144">RELATED LINKS</span></span>
