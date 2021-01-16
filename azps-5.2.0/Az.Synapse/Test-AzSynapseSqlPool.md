---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d07ec757fd5ab589de6234caac23992d6ff320fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344790"
---
# <span data-ttu-id="f0374-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f0374-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="f0374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0374-102">SYNOPSIS</span></span>
<span data-ttu-id="f0374-103">Ellenőrzi, hogy létezik-e Synapse Analytics SQL-készlet.</span><span class="sxs-lookup"><span data-stu-id="f0374-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f0374-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f0374-104">SYNTAX</span></span>

### <span data-ttu-id="f0374-105">TestByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f0374-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0374-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0374-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0374-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f0374-107">DESCRIPTION</span></span>
<span data-ttu-id="f0374-108">A **Test-AzSynapseSqlPool** parancsmag ellenőrzi, hogy létezik-e Synapse Analytics SQL-készlet.</span><span class="sxs-lookup"><span data-stu-id="f0374-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f0374-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f0374-109">EXAMPLES</span></span>

### <span data-ttu-id="f0374-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="f0374-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="f0374-111">Ez a parancs ellenőrzi a megadott SQL-készlet meglétét.</span><span class="sxs-lookup"><span data-stu-id="f0374-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="f0374-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0374-112">PARAMETERS</span></span>

### <span data-ttu-id="f0374-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0374-113">-DefaultProfile</span></span>
<span data-ttu-id="f0374-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0374-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0374-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f0374-115">-Name</span></span>
<span data-ttu-id="f0374-116">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="f0374-116">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0374-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0374-117">-ResourceGroupName</span></span>
<span data-ttu-id="f0374-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f0374-118">Resource group name.</span></span>

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

### <span data-ttu-id="f0374-119">-Version</span><span class="sxs-lookup"><span data-stu-id="f0374-119">-Version</span></span>
<span data-ttu-id="f0374-120">A Synapse SQL-készlet verziója.</span><span class="sxs-lookup"><span data-stu-id="f0374-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="f0374-121">Például 2 vagy 3.</span><span class="sxs-lookup"><span data-stu-id="f0374-121">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="f0374-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f0374-122">-WorkspaceName</span></span>
<span data-ttu-id="f0374-123">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="f0374-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f0374-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f0374-124">-WorkspaceObject</span></span>
<span data-ttu-id="f0374-125">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="f0374-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f0374-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0374-126">CommonParameters</span></span>
<span data-ttu-id="f0374-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0374-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0374-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0374-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0374-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0374-129">INPUTS</span></span>

### <span data-ttu-id="f0374-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f0374-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f0374-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0374-131">OUTPUTS</span></span>

### <span data-ttu-id="f0374-132">System.Object</span><span class="sxs-lookup"><span data-stu-id="f0374-132">System.Object</span></span>
## <span data-ttu-id="f0374-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f0374-133">NOTES</span></span>

## <span data-ttu-id="f0374-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0374-134">RELATED LINKS</span></span>
