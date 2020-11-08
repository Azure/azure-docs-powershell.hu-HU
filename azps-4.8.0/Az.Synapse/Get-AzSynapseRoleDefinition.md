---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180726"
---
# <span data-ttu-id="964e9-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="964e9-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="964e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="964e9-102">SYNOPSIS</span></span>
<span data-ttu-id="964e9-103">Egy szinapszis-Analytics szerepkör-definíciót kap.</span><span class="sxs-lookup"><span data-stu-id="964e9-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="964e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="964e9-104">SYNTAX</span></span>

### <span data-ttu-id="964e9-105">GetByWorkspaceNameAndIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="964e9-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="964e9-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="964e9-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="964e9-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="964e9-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="964e9-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="964e9-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="964e9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="964e9-109">DESCRIPTION</span></span>
<span data-ttu-id="964e9-110">A **Get-AzSynapseRoleDefinition** parancsmag az Azure szinapszis Analytics szerepkör-definíciót kapja.</span><span class="sxs-lookup"><span data-stu-id="964e9-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="964e9-111">Ha nem ad meg szerepkör-vagy Szerepdefiníció-azonosítót, ez a parancsmag minden szerepkör-definíciót kap.</span><span class="sxs-lookup"><span data-stu-id="964e9-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="964e9-112">Példák</span><span class="sxs-lookup"><span data-stu-id="964e9-112">EXAMPLES</span></span>

### <span data-ttu-id="964e9-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="964e9-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="964e9-114">Ez a parancs a munkaterület csoportban minden szerepkör-definíciót kap.</span><span class="sxs-lookup"><span data-stu-id="964e9-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="964e9-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="964e9-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="964e9-116">Ez a parancs beilleszti a szerepkör-definíciót a ContosoRole nevű munkaterület ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="964e9-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="964e9-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="964e9-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="964e9-118">Ez a parancs az összes szerepkör-definíciót beilleszti egy munkaterületre a csővezetékek között.</span><span class="sxs-lookup"><span data-stu-id="964e9-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="964e9-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="964e9-119">PARAMETERS</span></span>

### <span data-ttu-id="964e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="964e9-120">-DefaultProfile</span></span>
<span data-ttu-id="964e9-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="964e9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="964e9-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="964e9-122">-Id</span></span>
<span data-ttu-id="964e9-123">A megbízóhoz rendelt szerepkör azonosítója.</span><span class="sxs-lookup"><span data-stu-id="964e9-123">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="964e9-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="964e9-124">-Name</span></span>
<span data-ttu-id="964e9-125">A megbízóhoz rendelt szerepkör neve.</span><span class="sxs-lookup"><span data-stu-id="964e9-125">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="964e9-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="964e9-126">-WorkspaceName</span></span>
<span data-ttu-id="964e9-127">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="964e9-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="964e9-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="964e9-128">-WorkspaceObject</span></span>
<span data-ttu-id="964e9-129">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="964e9-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="964e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964e9-130">CommonParameters</span></span>
<span data-ttu-id="964e9-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="964e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964e9-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="964e9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964e9-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="964e9-133">INPUTS</span></span>

### <span data-ttu-id="964e9-134">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="964e9-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="964e9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="964e9-135">OUTPUTS</span></span>

### <span data-ttu-id="964e9-136">Microsoft. Azure. commands. szinapszis. models. PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="964e9-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="964e9-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="964e9-137">NOTES</span></span>

## <span data-ttu-id="964e9-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="964e9-138">RELATED LINKS</span></span>
