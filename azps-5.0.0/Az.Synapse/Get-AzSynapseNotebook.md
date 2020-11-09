---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302360"
---
# <span data-ttu-id="97e82-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="97e82-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="97e82-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97e82-102">SYNOPSIS</span></span>
<span data-ttu-id="97e82-103">Információt kap a munkaterületen lévő jegyzetfüzetekről.</span><span class="sxs-lookup"><span data-stu-id="97e82-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="97e82-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97e82-104">SYNTAX</span></span>

### <span data-ttu-id="97e82-105">GetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97e82-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97e82-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="97e82-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97e82-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="97e82-107">DESCRIPTION</span></span>
<span data-ttu-id="97e82-108">A **Get-AzSynapseNotebook** parancsmag információkat kap a munkaterületen lévő jegyzetfüzetekről.</span><span class="sxs-lookup"><span data-stu-id="97e82-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="97e82-109">Ha megad egy jegyzetfüzet nevét, a parancsmag információt kap a jegyzetfüzetről.</span><span class="sxs-lookup"><span data-stu-id="97e82-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="97e82-110">Ha nem ad meg nevet, a parancsmag a munkaterületen lévő összes jegyzetfüzetre vonatkozóan információkat kap.</span><span class="sxs-lookup"><span data-stu-id="97e82-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="97e82-111">Példák</span><span class="sxs-lookup"><span data-stu-id="97e82-111">EXAMPLES</span></span>

### <span data-ttu-id="97e82-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="97e82-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="97e82-113">Beolvassa az összes jegyzetfüzet listáját a munkaterület ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="97e82-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="97e82-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="97e82-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="97e82-115">Egy ContosoNotebook nevű jegyzetfüzetet kap a munkaterület ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="97e82-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="97e82-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="97e82-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="97e82-117">Egy ContosoNotebook nevű jegyzetfüzetet kap a munkaterület ContosoWorkspace a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="97e82-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="97e82-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97e82-118">PARAMETERS</span></span>

### <span data-ttu-id="97e82-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e82-119">-DefaultProfile</span></span>
<span data-ttu-id="97e82-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97e82-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97e82-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97e82-121">-Name</span></span>
<span data-ttu-id="97e82-122">A jegyzetfüzet neve.</span><span class="sxs-lookup"><span data-stu-id="97e82-122">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e82-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="97e82-123">-WorkspaceName</span></span>
<span data-ttu-id="97e82-124">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="97e82-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="97e82-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="97e82-125">-WorkspaceObject</span></span>
<span data-ttu-id="97e82-126">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="97e82-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="97e82-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e82-127">CommonParameters</span></span>
<span data-ttu-id="97e82-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97e82-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e82-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="97e82-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e82-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97e82-130">INPUTS</span></span>

### <span data-ttu-id="97e82-131">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="97e82-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="97e82-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97e82-132">OUTPUTS</span></span>

### <span data-ttu-id="97e82-133">Microsoft. Azure. commands. szinapszis. models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="97e82-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="97e82-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97e82-134">NOTES</span></span>

## <span data-ttu-id="97e82-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97e82-135">RELATED LINKS</span></span>
