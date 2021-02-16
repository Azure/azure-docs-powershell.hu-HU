---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165562"
---
# <span data-ttu-id="607e9-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="607e9-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="607e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="607e9-102">SYNOPSIS</span></span>
<span data-ttu-id="607e9-103">Frissíti a Synapse Analytics munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="607e9-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="607e9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="607e9-104">SYNTAX</span></span>

### <span data-ttu-id="607e9-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="607e9-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="607e9-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="607e9-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="607e9-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="607e9-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="607e9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="607e9-108">DESCRIPTION</span></span>
<span data-ttu-id="607e9-109">Az **Update-AzSynapseWorkspace** parancsmag frissíti az Azure Synapse Analytics munkaterületét.</span><span class="sxs-lookup"><span data-stu-id="607e9-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="607e9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="607e9-110">EXAMPLES</span></span>

### <span data-ttu-id="607e9-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="607e9-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="607e9-112">Ez a parancs frissíti a specifikációs Azure Synapse Analytics munkaterület címkéit.</span><span class="sxs-lookup"><span data-stu-id="607e9-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="607e9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="607e9-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="607e9-114">Ez a parancs a folyamaton keresztül frissíti a specifikációs Azure Synapse Analytics munkaterület címkéit.</span><span class="sxs-lookup"><span data-stu-id="607e9-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="607e9-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="607e9-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="607e9-116">Ez a parancs frissíti a specifikációs Azure Synapse Analytics munkaterület címkéit az erőforrás-azonosítót kezelő folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="607e9-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="607e9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="607e9-117">PARAMETERS</span></span>

### <span data-ttu-id="607e9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="607e9-118">-AsJob</span></span>
<span data-ttu-id="607e9-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="607e9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="607e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="607e9-120">-DefaultProfile</span></span>
<span data-ttu-id="607e9-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="607e9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="607e9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="607e9-122">-InputObject</span></span>
<span data-ttu-id="607e9-123">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="607e9-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="607e9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="607e9-124">-Name</span></span>
<span data-ttu-id="607e9-125">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="607e9-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="607e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="607e9-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="607e9-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607e9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="607e9-128">-ResourceId</span></span>
<span data-ttu-id="607e9-129">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="607e9-129">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607e9-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="607e9-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="607e9-131">A munkaterület új SQL-rendszergazdai jelszava.</span><span class="sxs-lookup"><span data-stu-id="607e9-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607e9-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="607e9-132">-Tag</span></span>
<span data-ttu-id="607e9-133">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="607e9-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607e9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="607e9-134">-Confirm</span></span>
<span data-ttu-id="607e9-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="607e9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="607e9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="607e9-136">-WhatIf</span></span>
<span data-ttu-id="607e9-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="607e9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="607e9-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="607e9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="607e9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607e9-139">CommonParameters</span></span>
<span data-ttu-id="607e9-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="607e9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607e9-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="607e9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607e9-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="607e9-142">INPUTS</span></span>

### <span data-ttu-id="607e9-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="607e9-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="607e9-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="607e9-144">OUTPUTS</span></span>

### <span data-ttu-id="607e9-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="607e9-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="607e9-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="607e9-146">NOTES</span></span>

## <span data-ttu-id="607e9-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="607e9-147">RELATED LINKS</span></span>
