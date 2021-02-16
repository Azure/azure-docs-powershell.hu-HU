---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155978"
---
# <span data-ttu-id="e9a43-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="e9a43-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="e9a43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9a43-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a43-103">Ellenőrzi, hogy létezik-e synapse Analytics Spark-készlet.</span><span class="sxs-lookup"><span data-stu-id="e9a43-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="e9a43-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e9a43-104">SYNTAX</span></span>

### <span data-ttu-id="e9a43-105">TestByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9a43-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9a43-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9a43-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9a43-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e9a43-107">DESCRIPTION</span></span>
<span data-ttu-id="e9a43-108">A **Test-AzSynapseSparkPool** parancsmag ellenőrzi, hogy létezik-e Synapse Analytics Spark-készlet.</span><span class="sxs-lookup"><span data-stu-id="e9a43-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="e9a43-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e9a43-109">EXAMPLES</span></span>

### <span data-ttu-id="e9a43-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="e9a43-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="e9a43-111">Ez a parancs ellenőrzi, hogy létezik-e a megadott értékgörbe.</span><span class="sxs-lookup"><span data-stu-id="e9a43-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="e9a43-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9a43-112">PARAMETERS</span></span>

### <span data-ttu-id="e9a43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a43-113">-DefaultProfile</span></span>
<span data-ttu-id="e9a43-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9a43-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9a43-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e9a43-115">-Name</span></span>
<span data-ttu-id="e9a43-116">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="e9a43-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="e9a43-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a43-117">-ResourceGroupName</span></span>
<span data-ttu-id="e9a43-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e9a43-118">Resource group name.</span></span>

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

### <span data-ttu-id="e9a43-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e9a43-119">-WorkspaceName</span></span>
<span data-ttu-id="e9a43-120">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="e9a43-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e9a43-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e9a43-121">-WorkspaceObject</span></span>
<span data-ttu-id="e9a43-122">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="e9a43-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e9a43-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a43-123">CommonParameters</span></span>
<span data-ttu-id="e9a43-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9a43-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a43-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9a43-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a43-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9a43-126">INPUTS</span></span>

### <span data-ttu-id="e9a43-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e9a43-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e9a43-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9a43-128">OUTPUTS</span></span>

### <span data-ttu-id="e9a43-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="e9a43-129">System.Object</span></span>
## <span data-ttu-id="e9a43-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e9a43-130">NOTES</span></span>

## <span data-ttu-id="e9a43-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9a43-131">RELATED LINKS</span></span>
