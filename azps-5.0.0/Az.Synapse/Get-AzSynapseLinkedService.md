---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302363"
---
# <span data-ttu-id="88cff-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="88cff-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="88cff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88cff-102">SYNOPSIS</span></span>
<span data-ttu-id="88cff-103">Információt kap a munkaterületen lévő kapcsolt szolgáltatásokról.</span><span class="sxs-lookup"><span data-stu-id="88cff-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="88cff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88cff-104">SYNTAX</span></span>

### <span data-ttu-id="88cff-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88cff-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88cff-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="88cff-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88cff-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="88cff-107">DESCRIPTION</span></span>
<span data-ttu-id="88cff-108">A **Get-AzSynapseLinkedService** parancsmag információkat kap a munkaterületen lévő kapcsolt szolgáltatásokról.</span><span class="sxs-lookup"><span data-stu-id="88cff-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="88cff-109">Ha egy kapcsolt szolgáltatás nevét adja meg, ez a parancsmag információkat kap a kapcsolt szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="88cff-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="88cff-110">Ha nem ad meg nevet, ez a parancsmag információkat kap a munkaterület összes kapcsolt szolgáltatásáról.</span><span class="sxs-lookup"><span data-stu-id="88cff-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="88cff-111">Példák</span><span class="sxs-lookup"><span data-stu-id="88cff-111">EXAMPLES</span></span>

### <span data-ttu-id="88cff-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="88cff-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="88cff-113">Ez a parancs a ContosoWorkspace nevű munkaterületen található összes kapcsolt szolgáltatásról információt kap.</span><span class="sxs-lookup"><span data-stu-id="88cff-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="88cff-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="88cff-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="88cff-115">Ez a parancs információt kap a ContosoLinkedService nevű kapcsolt szolgáltatásról a ContosoWorkspace nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="88cff-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="88cff-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="88cff-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="88cff-117">Ez a parancs információt kap a ContosoLinkedService nevű kapcsolt szolgáltatásról a ContosoWorkspace – csővezeték nevű munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="88cff-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="88cff-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88cff-118">PARAMETERS</span></span>

### <span data-ttu-id="88cff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88cff-119">-DefaultProfile</span></span>
<span data-ttu-id="88cff-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88cff-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88cff-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88cff-121">-Name</span></span>
<span data-ttu-id="88cff-122">A kapcsolt szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="88cff-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88cff-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="88cff-123">-WorkspaceName</span></span>
<span data-ttu-id="88cff-124">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="88cff-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="88cff-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="88cff-125">-WorkspaceObject</span></span>
<span data-ttu-id="88cff-126">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="88cff-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="88cff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88cff-127">CommonParameters</span></span>
<span data-ttu-id="88cff-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88cff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88cff-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88cff-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88cff-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88cff-130">INPUTS</span></span>

### <span data-ttu-id="88cff-131">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="88cff-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="88cff-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88cff-132">OUTPUTS</span></span>

### <span data-ttu-id="88cff-133">Microsoft. Azure. commands. szinapszis. models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="88cff-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="88cff-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88cff-134">NOTES</span></span>

## <span data-ttu-id="88cff-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88cff-135">RELATED LINKS</span></span>
