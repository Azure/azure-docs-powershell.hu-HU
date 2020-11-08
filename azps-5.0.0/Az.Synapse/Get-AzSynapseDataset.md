---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186500"
---
# <span data-ttu-id="47f21-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="47f21-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="47f21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47f21-102">SYNOPSIS</span></span>
<span data-ttu-id="47f21-103">Információt kap az adatkészletekről a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="47f21-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="47f21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47f21-104">SYNTAX</span></span>

### <span data-ttu-id="47f21-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47f21-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47f21-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="47f21-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47f21-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="47f21-107">DESCRIPTION</span></span>
<span data-ttu-id="47f21-108">A **Get-AzSynapseDataset** parancsmag információkat kap a munkaterületen lévő adatkészletekről.</span><span class="sxs-lookup"><span data-stu-id="47f21-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="47f21-109">Ha megadja az adatkészlet nevét, ez a parancsmag információkat kap az adatkészletről.</span><span class="sxs-lookup"><span data-stu-id="47f21-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="47f21-110">Ha nem ad meg nevet, ez a parancsmag információkat kap a munkaterület összes adatkészletéről.</span><span class="sxs-lookup"><span data-stu-id="47f21-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="47f21-111">Példák</span><span class="sxs-lookup"><span data-stu-id="47f21-111">EXAMPLES</span></span>

### <span data-ttu-id="47f21-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="47f21-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="47f21-113">Ez a parancs a ContosoWorkspace nevű munkaterületen található összes adatkészletről információt kap.</span><span class="sxs-lookup"><span data-stu-id="47f21-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="47f21-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="47f21-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="47f21-115">Ez a parancs információt kap a ContosoDataset nevű adatkészletről a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="47f21-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="47f21-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47f21-116">PARAMETERS</span></span>

### <span data-ttu-id="47f21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47f21-117">-DefaultProfile</span></span>
<span data-ttu-id="47f21-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47f21-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47f21-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47f21-119">-Name</span></span>
<span data-ttu-id="47f21-120">Az adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="47f21-120">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f21-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="47f21-121">-WorkspaceName</span></span>
<span data-ttu-id="47f21-122">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="47f21-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="47f21-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="47f21-123">-WorkspaceObject</span></span>
<span data-ttu-id="47f21-124">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="47f21-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="47f21-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f21-125">CommonParameters</span></span>
<span data-ttu-id="47f21-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47f21-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f21-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="47f21-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f21-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47f21-128">INPUTS</span></span>

### <span data-ttu-id="47f21-129">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="47f21-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="47f21-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47f21-130">OUTPUTS</span></span>

### <span data-ttu-id="47f21-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="47f21-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="47f21-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47f21-132">NOTES</span></span>

## <span data-ttu-id="47f21-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47f21-133">RELATED LINKS</span></span>