---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181231"
---
# <span data-ttu-id="5b65f-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="5b65f-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="5b65f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b65f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b65f-103">Információt kap a munkaterületen lévő adatforgalomról.</span><span class="sxs-lookup"><span data-stu-id="5b65f-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="5b65f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b65f-104">SYNTAX</span></span>

### <span data-ttu-id="5b65f-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b65f-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b65f-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="5b65f-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b65f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b65f-107">DESCRIPTION</span></span>
<span data-ttu-id="5b65f-108">A **Get-AzSynapseDataFlow** parancsmag információkat kap a munkaterületen lévő adatforgalomról.</span><span class="sxs-lookup"><span data-stu-id="5b65f-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="5b65f-109">Ha megadja az adatfolyam nevét, ez a parancsmag információkat kap az adatáramlásról.</span><span class="sxs-lookup"><span data-stu-id="5b65f-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="5b65f-110">Ha nem ad meg nevet, ez a parancsmag információkat kap a munkaterületen lévő összes adatforgalomról.</span><span class="sxs-lookup"><span data-stu-id="5b65f-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="5b65f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5b65f-111">EXAMPLES</span></span>

### <span data-ttu-id="5b65f-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5b65f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="5b65f-113">Ez a parancs információt kap a ContosoWorkspace nevű munkaterületen található összes adatforgalomról.</span><span class="sxs-lookup"><span data-stu-id="5b65f-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="5b65f-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="5b65f-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="5b65f-115">Ez a parancs információt kap a ContosoDataFlow nevű adatfolyamról a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="5b65f-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="5b65f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b65f-116">PARAMETERS</span></span>

### <span data-ttu-id="5b65f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b65f-117">-DefaultProfile</span></span>
<span data-ttu-id="5b65f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b65f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b65f-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b65f-119">-Name</span></span>
<span data-ttu-id="5b65f-120">Az adatforgalom neve.</span><span class="sxs-lookup"><span data-stu-id="5b65f-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b65f-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5b65f-121">-WorkspaceName</span></span>
<span data-ttu-id="5b65f-122">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="5b65f-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5b65f-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5b65f-123">-WorkspaceObject</span></span>
<span data-ttu-id="5b65f-124">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="5b65f-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5b65f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b65f-125">CommonParameters</span></span>
<span data-ttu-id="5b65f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b65f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b65f-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5b65f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b65f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b65f-128">INPUTS</span></span>

### <span data-ttu-id="5b65f-129">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5b65f-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5b65f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b65f-130">OUTPUTS</span></span>

### <span data-ttu-id="5b65f-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="5b65f-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="5b65f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b65f-132">NOTES</span></span>

## <span data-ttu-id="5b65f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b65f-133">RELATED LINKS</span></span>
