---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361477"
---
# <span data-ttu-id="9747f-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9747f-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="9747f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9747f-102">SYNOPSIS</span></span>
<span data-ttu-id="9747f-103">Ellenőrzi, hogy létezik-e synapse Analytics Spark-készlet.</span><span class="sxs-lookup"><span data-stu-id="9747f-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="9747f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9747f-104">SYNTAX</span></span>

### <span data-ttu-id="9747f-105">TestByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9747f-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9747f-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9747f-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9747f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9747f-107">DESCRIPTION</span></span>
<span data-ttu-id="9747f-108">A **Test-AzSynapseSparkPool** parancsmag ellenőrzi, hogy létezik-e Synapse Analytics Spark-készlet.</span><span class="sxs-lookup"><span data-stu-id="9747f-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="9747f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9747f-109">EXAMPLES</span></span>

### <span data-ttu-id="9747f-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="9747f-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="9747f-111">Ez a parancs ellenőrzi, hogy létezik-e a megadott értékgörbe.</span><span class="sxs-lookup"><span data-stu-id="9747f-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="9747f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9747f-112">PARAMETERS</span></span>

### <span data-ttu-id="9747f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9747f-113">-DefaultProfile</span></span>
<span data-ttu-id="9747f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9747f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9747f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9747f-115">-Name</span></span>
<span data-ttu-id="9747f-116">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="9747f-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="9747f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9747f-117">-ResourceGroupName</span></span>
<span data-ttu-id="9747f-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9747f-118">Resource group name.</span></span>

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

### <span data-ttu-id="9747f-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9747f-119">-WorkspaceName</span></span>
<span data-ttu-id="9747f-120">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="9747f-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9747f-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9747f-121">-WorkspaceObject</span></span>
<span data-ttu-id="9747f-122">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="9747f-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9747f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9747f-123">CommonParameters</span></span>
<span data-ttu-id="9747f-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9747f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9747f-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9747f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9747f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9747f-126">INPUTS</span></span>

### <span data-ttu-id="9747f-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9747f-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9747f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9747f-128">OUTPUTS</span></span>

### <span data-ttu-id="9747f-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="9747f-129">System.Object</span></span>
## <span data-ttu-id="9747f-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9747f-130">NOTES</span></span>

## <span data-ttu-id="9747f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9747f-131">RELATED LINKS</span></span>
