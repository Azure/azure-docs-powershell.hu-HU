---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181220"
---
# <span data-ttu-id="22e1e-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="22e1e-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="22e1e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="22e1e-103">Információt kap a munkaterületen lévő eseményindítókkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="22e1e-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="22e1e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22e1e-104">SYNTAX</span></span>

### <span data-ttu-id="22e1e-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22e1e-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22e1e-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="22e1e-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22e1e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="22e1e-107">DESCRIPTION</span></span>
<span data-ttu-id="22e1e-108">A **Get-AzSynapseTrigger** parancsmag információkat kap a munkaterületen lévő eseményindítókkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="22e1e-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="22e1e-109">Ha megad egy trigger nevét, a parancsmag információt kap az adott triggerről.</span><span class="sxs-lookup"><span data-stu-id="22e1e-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="22e1e-110">Ha nem ad meg nevet, a parancsmag a munkaterületen lévő összes eseményindítóról információt kap.</span><span class="sxs-lookup"><span data-stu-id="22e1e-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="22e1e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="22e1e-111">EXAMPLES</span></span>

### <span data-ttu-id="22e1e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="22e1e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="22e1e-113">A munkaterület ContosoWorkspace létrehozott összes eseményindító listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="22e1e-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="22e1e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="22e1e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="22e1e-115">Az ContosoTrigger nevű egyetlen triggert kapja a munkaterület ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="22e1e-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="22e1e-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="22e1e-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="22e1e-117">Egy ContosoTrigger nevű egyetlen triggert kap a munkaterület ContosoWorkspace a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="22e1e-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="22e1e-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22e1e-118">PARAMETERS</span></span>

### <span data-ttu-id="22e1e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e1e-119">-DefaultProfile</span></span>
<span data-ttu-id="22e1e-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22e1e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22e1e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="22e1e-121">-Name</span></span>
<span data-ttu-id="22e1e-122">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="22e1e-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e1e-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="22e1e-123">-WorkspaceName</span></span>
<span data-ttu-id="22e1e-124">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="22e1e-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e1e-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="22e1e-125">-WorkspaceObject</span></span>
<span data-ttu-id="22e1e-126">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="22e1e-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22e1e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e1e-127">CommonParameters</span></span>
<span data-ttu-id="22e1e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22e1e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e1e-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="22e1e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e1e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22e1e-130">INPUTS</span></span>

### <span data-ttu-id="22e1e-131">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="22e1e-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="22e1e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22e1e-132">OUTPUTS</span></span>

### <span data-ttu-id="22e1e-133">Microsoft. Azure. commands. szinapszis. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="22e1e-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="22e1e-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22e1e-134">NOTES</span></span>

## <span data-ttu-id="22e1e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22e1e-135">RELATED LINKS</span></span>
