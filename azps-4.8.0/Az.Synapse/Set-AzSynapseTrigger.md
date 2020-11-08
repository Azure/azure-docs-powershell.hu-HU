---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182483"
---
# <span data-ttu-id="a3328-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="a3328-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="a3328-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3328-102">SYNOPSIS</span></span>
<span data-ttu-id="a3328-103">Létrehoz egy triggert egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="a3328-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="a3328-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3328-104">SYNTAX</span></span>

### <span data-ttu-id="a3328-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3328-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3328-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="a3328-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3328-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3328-107">DESCRIPTION</span></span>
<span data-ttu-id="a3328-108">A **set-AzSynapseTrigger** parancsmag létrehoz egy triggert egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="a3328-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="a3328-109">Az eseményindítók a "leállt" állapotban jönnek létre, ami azt jelenti, hogy nem azonnal kezdenek hivatkozni a rájuk hivatkozó csővezetékekre.</span><span class="sxs-lookup"><span data-stu-id="a3328-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="a3328-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a3328-110">EXAMPLES</span></span>

### <span data-ttu-id="a3328-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a3328-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="a3328-112">Hozzon létre egy ContosoTrigger nevű új triggert a munkaterület ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a3328-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="a3328-113">Az trigger a "leállt" állapotban jön létre, ami azt jelenti, hogy az nem azonnal indul el.</span><span class="sxs-lookup"><span data-stu-id="a3328-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="a3328-114">Az indítót a parancsmag használatával indíthatja el `Start-AzDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="a3328-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="a3328-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="a3328-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="a3328-116">Hozzon létre egy ContosoTrigger nevű új triggert a munkaterület ContosoWorkspace a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="a3328-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="a3328-117">Az trigger a "leállt" állapotban jön létre, ami azt jelenti, hogy az nem azonnal indul el.</span><span class="sxs-lookup"><span data-stu-id="a3328-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="a3328-118">Az indítót a parancsmag használatával indíthatja el `Start-AzDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="a3328-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="a3328-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3328-119">PARAMETERS</span></span>

### <span data-ttu-id="a3328-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3328-120">-AsJob</span></span>
<span data-ttu-id="a3328-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a3328-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3328-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3328-122">-DefaultProfile</span></span>
<span data-ttu-id="a3328-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3328-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3328-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="a3328-124">-DefinitionFile</span></span>
<span data-ttu-id="a3328-125">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="a3328-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3328-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a3328-126">-Name</span></span>
<span data-ttu-id="a3328-127">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="a3328-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3328-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a3328-128">-WorkspaceName</span></span>
<span data-ttu-id="a3328-129">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="a3328-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3328-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a3328-130">-WorkspaceObject</span></span>
<span data-ttu-id="a3328-131">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="a3328-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3328-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a3328-132">-Confirm</span></span>
<span data-ttu-id="a3328-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3328-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3328-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3328-134">-WhatIf</span></span>
<span data-ttu-id="a3328-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a3328-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3328-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3328-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3328-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3328-137">CommonParameters</span></span>
<span data-ttu-id="a3328-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3328-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3328-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a3328-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3328-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3328-140">INPUTS</span></span>

### <span data-ttu-id="a3328-141">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3328-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a3328-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3328-142">OUTPUTS</span></span>

### <span data-ttu-id="a3328-143">Microsoft. Azure. commands. szinapszis. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="a3328-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="a3328-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3328-144">NOTES</span></span>

## <span data-ttu-id="a3328-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3328-145">RELATED LINKS</span></span>
