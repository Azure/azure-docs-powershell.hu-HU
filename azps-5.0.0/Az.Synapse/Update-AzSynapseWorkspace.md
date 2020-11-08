---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186597"
---
# <span data-ttu-id="e89e9-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e89e9-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="e89e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e89e9-102">SYNOPSIS</span></span>
<span data-ttu-id="e89e9-103">A szinapszis Analytics-munkaterületének frissítése</span><span class="sxs-lookup"><span data-stu-id="e89e9-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e89e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e89e9-104">SYNTAX</span></span>

### <span data-ttu-id="e89e9-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e89e9-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e89e9-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e89e9-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e89e9-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e89e9-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e89e9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e89e9-108">DESCRIPTION</span></span>
<span data-ttu-id="e89e9-109">Az **Update-AzSynapseWorkspace** parancsmag az Azure szinapszis Analytics-munkaterületén frissít.</span><span class="sxs-lookup"><span data-stu-id="e89e9-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e89e9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e89e9-110">EXAMPLES</span></span>

### <span data-ttu-id="e89e9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e89e9-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="e89e9-112">Ezek a parancsok a specififed Azure szinapszis Analytics-munkaterület címkéit frissítik.</span><span class="sxs-lookup"><span data-stu-id="e89e9-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="e89e9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e89e9-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="e89e9-114">Ez a parancs a specififed Azure szinapszis Analytics-munkaterülethez a csővezetéken keresztül frissíti a címkéket.</span><span class="sxs-lookup"><span data-stu-id="e89e9-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="e89e9-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="e89e9-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="e89e9-116">Ezek a parancsok a specififed Azure szinapszis Analytics-munkaterületre vonatkozó címkéket frissítik a pipeline és az erőforrás-azonosító segítségével.</span><span class="sxs-lookup"><span data-stu-id="e89e9-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="e89e9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e89e9-117">PARAMETERS</span></span>

### <span data-ttu-id="e89e9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e89e9-118">-AsJob</span></span>
<span data-ttu-id="e89e9-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e89e9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e89e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e89e9-120">-DefaultProfile</span></span>
<span data-ttu-id="e89e9-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e89e9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e89e9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e89e9-122">-InputObject</span></span>
<span data-ttu-id="e89e9-123">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="e89e9-123">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e89e9-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e89e9-124">-Name</span></span>
<span data-ttu-id="e89e9-125">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="e89e9-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e89e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e89e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="e89e9-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e89e9-127">Resource group name.</span></span>

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

### <span data-ttu-id="e89e9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e89e9-128">-ResourceId</span></span>
<span data-ttu-id="e89e9-129">A szinapszis-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e89e9-129">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="e89e9-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="e89e9-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="e89e9-131">A munkaterület új SQL-rendszergazdai jelszava.</span><span class="sxs-lookup"><span data-stu-id="e89e9-131">The new SQL administrator password for the workspace.</span></span>

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

### <span data-ttu-id="e89e9-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="e89e9-132">-Tag</span></span>
<span data-ttu-id="e89e9-133">Az erőforráshoz társított címkék karakterlánca, karakterláncok szótára</span><span class="sxs-lookup"><span data-stu-id="e89e9-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="e89e9-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e89e9-134">-Confirm</span></span>
<span data-ttu-id="e89e9-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e89e9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e89e9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e89e9-136">-WhatIf</span></span>
<span data-ttu-id="e89e9-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e89e9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e89e9-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e89e9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e89e9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e89e9-139">CommonParameters</span></span>
<span data-ttu-id="e89e9-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e89e9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e89e9-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e89e9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e89e9-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e89e9-142">INPUTS</span></span>

### <span data-ttu-id="e89e9-143">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e89e9-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e89e9-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e89e9-144">OUTPUTS</span></span>

### <span data-ttu-id="e89e9-145">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e89e9-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e89e9-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e89e9-146">NOTES</span></span>

## <span data-ttu-id="e89e9-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e89e9-147">RELATED LINKS</span></span>
