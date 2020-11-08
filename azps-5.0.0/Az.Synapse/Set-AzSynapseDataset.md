---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195457"
---
# <span data-ttu-id="70b83-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="70b83-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="70b83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70b83-102">SYNOPSIS</span></span>
<span data-ttu-id="70b83-103">Adatkészletet hoz létre vagy frissít a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="70b83-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="70b83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70b83-104">SYNTAX</span></span>

### <span data-ttu-id="70b83-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70b83-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70b83-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="70b83-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70b83-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="70b83-107">DESCRIPTION</span></span>
<span data-ttu-id="70b83-108">A **set-AzSynapseDataset** parancsmag létrehoz egy adatkészletet, vagy frissít egy meglévő adatkészletet a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="70b83-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="70b83-109">Példák</span><span class="sxs-lookup"><span data-stu-id="70b83-109">EXAMPLES</span></span>

### <span data-ttu-id="70b83-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="70b83-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="70b83-111">A parancs létrehoz egy ContosoDataset nevű adatkészletet a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="70b83-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="70b83-112">A parancs az adatkészletet az Dataset.jsfájlon lévő adatokra alapozja.</span><span class="sxs-lookup"><span data-stu-id="70b83-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="70b83-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70b83-113">PARAMETERS</span></span>

### <span data-ttu-id="70b83-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70b83-114">-AsJob</span></span>
<span data-ttu-id="70b83-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="70b83-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70b83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70b83-116">-DefaultProfile</span></span>
<span data-ttu-id="70b83-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70b83-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70b83-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="70b83-118">-DefinitionFile</span></span>
<span data-ttu-id="70b83-119">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="70b83-119">The JSON file path.</span></span>

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

### <span data-ttu-id="70b83-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70b83-120">-Name</span></span>
<span data-ttu-id="70b83-121">Az adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="70b83-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70b83-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="70b83-122">-WorkspaceName</span></span>
<span data-ttu-id="70b83-123">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="70b83-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="70b83-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="70b83-124">-WorkspaceObject</span></span>
<span data-ttu-id="70b83-125">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="70b83-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="70b83-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70b83-126">-Confirm</span></span>
<span data-ttu-id="70b83-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70b83-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70b83-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70b83-128">-WhatIf</span></span>
<span data-ttu-id="70b83-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70b83-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70b83-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70b83-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70b83-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b83-131">CommonParameters</span></span>
<span data-ttu-id="70b83-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70b83-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b83-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="70b83-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b83-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70b83-134">INPUTS</span></span>

### <span data-ttu-id="70b83-135">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="70b83-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="70b83-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70b83-136">OUTPUTS</span></span>

### <span data-ttu-id="70b83-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="70b83-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="70b83-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70b83-138">NOTES</span></span>

## <span data-ttu-id="70b83-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70b83-139">RELATED LINKS</span></span>
