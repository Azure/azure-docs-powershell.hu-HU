---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: 80d615f5a2a26869d748f652feeaa8909aca30d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383066"
---
# <span data-ttu-id="07eb1-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="07eb1-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="07eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="07eb1-103">Ellenőrzi, hogy létezik-e Synapse Analytics SQL-készlet.</span><span class="sxs-lookup"><span data-stu-id="07eb1-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="07eb1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07eb1-104">SYNTAX</span></span>

### <span data-ttu-id="07eb1-105">TestByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07eb1-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07eb1-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07eb1-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07eb1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07eb1-107">DESCRIPTION</span></span>
<span data-ttu-id="07eb1-108">A **Test-AzSynapseSqlPool** parancsmag ellenőrzi, hogy létezik-e Synapse Analytics SQL-készlet.</span><span class="sxs-lookup"><span data-stu-id="07eb1-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="07eb1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07eb1-109">EXAMPLES</span></span>

### <span data-ttu-id="07eb1-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="07eb1-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="07eb1-111">Ez a parancs ellenőrzi a megadott SQL-készlet meglétét.</span><span class="sxs-lookup"><span data-stu-id="07eb1-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="07eb1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07eb1-112">PARAMETERS</span></span>

### <span data-ttu-id="07eb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07eb1-113">-DefaultProfile</span></span>
<span data-ttu-id="07eb1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07eb1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07eb1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="07eb1-115">-Name</span></span>
<span data-ttu-id="07eb1-116">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="07eb1-116">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07eb1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07eb1-117">-ResourceGroupName</span></span>
<span data-ttu-id="07eb1-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="07eb1-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07eb1-119">-Version</span><span class="sxs-lookup"><span data-stu-id="07eb1-119">-Version</span></span>
<span data-ttu-id="07eb1-120">A Synapse SQL-készlet verziója.</span><span class="sxs-lookup"><span data-stu-id="07eb1-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="07eb1-121">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="07eb1-121">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07eb1-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="07eb1-122">-WorkspaceName</span></span>
<span data-ttu-id="07eb1-123">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="07eb1-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07eb1-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="07eb1-124">-WorkspaceObject</span></span>
<span data-ttu-id="07eb1-125">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="07eb1-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07eb1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07eb1-126">CommonParameters</span></span>
<span data-ttu-id="07eb1-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07eb1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07eb1-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07eb1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07eb1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07eb1-129">INPUTS</span></span>

### <span data-ttu-id="07eb1-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="07eb1-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="07eb1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07eb1-131">OUTPUTS</span></span>

### <span data-ttu-id="07eb1-132">System.Object</span><span class="sxs-lookup"><span data-stu-id="07eb1-132">System.Object</span></span>
## <span data-ttu-id="07eb1-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07eb1-133">NOTES</span></span>

## <span data-ttu-id="07eb1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07eb1-134">RELATED LINKS</span></span>
