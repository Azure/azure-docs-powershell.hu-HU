---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: cb7abd3c54d263ae9516344237588ecf9a1297ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011253"
---
# <span data-ttu-id="d25d7-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="d25d7-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="d25d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d25d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d25d7-103">Ellenőrzi, hogy létezik-e synapse Analytics Spark-készlet.</span><span class="sxs-lookup"><span data-stu-id="d25d7-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="d25d7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d25d7-104">SYNTAX</span></span>

### <span data-ttu-id="d25d7-105">TestByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d25d7-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d25d7-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d25d7-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d25d7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d25d7-107">DESCRIPTION</span></span>
<span data-ttu-id="d25d7-108">A **Test-AzSynapseSparkPool** parancsmag ellenőrzi, hogy létezik-e Synapse Analytics Spark-készlet.</span><span class="sxs-lookup"><span data-stu-id="d25d7-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="d25d7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d25d7-109">EXAMPLES</span></span>

### <span data-ttu-id="d25d7-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d25d7-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="d25d7-111">Ez a parancs ellenőrzi, hogy létezik-e a megadott értékgörbe.</span><span class="sxs-lookup"><span data-stu-id="d25d7-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="d25d7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d25d7-112">PARAMETERS</span></span>

### <span data-ttu-id="d25d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25d7-113">-DefaultProfile</span></span>
<span data-ttu-id="d25d7-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d25d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d25d7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d25d7-115">-Name</span></span>
<span data-ttu-id="d25d7-116">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="d25d7-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="d25d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d25d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="d25d7-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d25d7-118">Resource group name.</span></span>

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

### <span data-ttu-id="d25d7-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d25d7-119">-WorkspaceName</span></span>
<span data-ttu-id="d25d7-120">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="d25d7-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d25d7-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d25d7-121">-WorkspaceObject</span></span>
<span data-ttu-id="d25d7-122">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="d25d7-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d25d7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25d7-123">CommonParameters</span></span>
<span data-ttu-id="d25d7-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d25d7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25d7-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d25d7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25d7-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d25d7-126">INPUTS</span></span>

### <span data-ttu-id="d25d7-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d25d7-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d25d7-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d25d7-128">OUTPUTS</span></span>

### <span data-ttu-id="d25d7-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="d25d7-129">System.Object</span></span>
## <span data-ttu-id="d25d7-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d25d7-130">NOTES</span></span>

## <span data-ttu-id="d25d7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d25d7-131">RELATED LINKS</span></span>
