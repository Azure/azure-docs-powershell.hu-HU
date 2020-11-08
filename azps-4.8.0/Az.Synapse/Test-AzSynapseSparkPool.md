---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017464"
---
# <span data-ttu-id="b5ca6-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="b5ca6-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="b5ca6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ca6-103">Ellenőrzi, hogy létezik-e egy szinapszis-elemző szikra medence.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="b5ca6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5ca6-104">SYNTAX</span></span>

### <span data-ttu-id="b5ca6-105">TestByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5ca6-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5ca6-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5ca6-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5ca6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5ca6-107">DESCRIPTION</span></span>
<span data-ttu-id="b5ca6-108">A **AzSynapseSparkPool-** parancsmag ellenőrzi a szinapszis-elemző Spark-készlet létezését.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="b5ca6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b5ca6-109">EXAMPLES</span></span>

### <span data-ttu-id="b5ca6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b5ca6-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="b5ca6-111">Ez a parancs ellenőrzi a megadott Spark-készlet létezését.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="b5ca6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5ca6-112">PARAMETERS</span></span>

### <span data-ttu-id="b5ca6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ca6-113">-DefaultProfile</span></span>
<span data-ttu-id="b5ca6-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ca6-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5ca6-115">-Name</span></span>
<span data-ttu-id="b5ca6-116">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="b5ca6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ca6-117">-ResourceGroupName</span></span>
<span data-ttu-id="b5ca6-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-118">Resource group name.</span></span>

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

### <span data-ttu-id="b5ca6-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b5ca6-119">-WorkspaceName</span></span>
<span data-ttu-id="b5ca6-120">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b5ca6-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b5ca6-121">-WorkspaceObject</span></span>
<span data-ttu-id="b5ca6-122">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b5ca6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ca6-123">CommonParameters</span></span>
<span data-ttu-id="b5ca6-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5ca6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ca6-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b5ca6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ca6-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5ca6-126">INPUTS</span></span>

### <span data-ttu-id="b5ca6-127">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5ca6-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b5ca6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5ca6-128">OUTPUTS</span></span>

### <span data-ttu-id="b5ca6-129">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="b5ca6-129">System.Object</span></span>
## <span data-ttu-id="b5ca6-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5ca6-130">NOTES</span></span>

## <span data-ttu-id="b5ca6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5ca6-131">RELATED LINKS</span></span>
