---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4147343b01e53050f88429424ca7a9c70aa445c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195464"
---
# <span data-ttu-id="06428-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="06428-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="06428-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06428-102">SYNOPSIS</span></span>
<span data-ttu-id="06428-103">Adatfolyamot hoz létre vagy frissít a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="06428-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="06428-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06428-104">SYNTAX</span></span>

### <span data-ttu-id="06428-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="06428-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06428-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="06428-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06428-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="06428-107">DESCRIPTION</span></span>
<span data-ttu-id="06428-108">A **set-AzSynapseDataFlow** parancsmag adatáramlást hoz létre, vagy egy meglévő adatfolyamot frissít a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="06428-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="06428-109">Példák</span><span class="sxs-lookup"><span data-stu-id="06428-109">EXAMPLES</span></span>

### <span data-ttu-id="06428-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06428-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="06428-111">Ez a parancs létrehoz egy ContosoDataFlow nevű adatfolyamot a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="06428-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="06428-112">A parancs az adatáramlást az adatokra a fájl DataFlow.js.</span><span class="sxs-lookup"><span data-stu-id="06428-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="06428-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06428-113">PARAMETERS</span></span>

### <span data-ttu-id="06428-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06428-114">-AsJob</span></span>
<span data-ttu-id="06428-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="06428-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06428-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06428-116">-DefaultProfile</span></span>
<span data-ttu-id="06428-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06428-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06428-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="06428-118">-DefinitionFile</span></span>
<span data-ttu-id="06428-119">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="06428-119">The JSON file path.</span></span>

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

### <span data-ttu-id="06428-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="06428-120">-Name</span></span>
<span data-ttu-id="06428-121">Az adatforgalom neve.</span><span class="sxs-lookup"><span data-stu-id="06428-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06428-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="06428-122">-WorkspaceName</span></span>
<span data-ttu-id="06428-123">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="06428-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="06428-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="06428-124">-WorkspaceObject</span></span>
<span data-ttu-id="06428-125">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="06428-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="06428-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06428-126">-Confirm</span></span>
<span data-ttu-id="06428-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06428-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06428-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06428-128">-WhatIf</span></span>
<span data-ttu-id="06428-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06428-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06428-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06428-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06428-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06428-131">CommonParameters</span></span>
<span data-ttu-id="06428-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06428-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06428-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="06428-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06428-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06428-134">INPUTS</span></span>

### <span data-ttu-id="06428-135">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="06428-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="06428-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06428-136">OUTPUTS</span></span>

### <span data-ttu-id="06428-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="06428-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="06428-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06428-138">NOTES</span></span>

## <span data-ttu-id="06428-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06428-139">RELATED LINKS</span></span>
