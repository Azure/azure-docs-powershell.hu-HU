---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504888"
---
# <span data-ttu-id="86623-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="86623-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="86623-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86623-102">SYNOPSIS</span></span>
<span data-ttu-id="86623-103">Elindítja a operationalization-fürt rendszerszolgáltatásainak frissítését.</span><span class="sxs-lookup"><span data-stu-id="86623-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86623-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86623-104">SYNTAX</span></span>

### <span data-ttu-id="86623-105">Rendszerszolgáltatások frissítésének indítása a parancsmag bemeneti paramétereinek segítségével</span><span class="sxs-lookup"><span data-stu-id="86623-105">Start a system services update from cmdlet input parameters.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="86623-106">Indítsa el a rendszerszolgáltatások frissítését egy PSOperationalizationCluster példány-definícióból.</span><span class="sxs-lookup"><span data-stu-id="86623-106">Start a system services update from an PSOperationalizationCluster instance definition.</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="86623-107">Indítsa el a rendszerszolgáltatások frissítését egy Azure Resouce-azonosítóból.</span><span class="sxs-lookup"><span data-stu-id="86623-107">Start a system services update from an Azure resouce id.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="86623-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="86623-108">DESCRIPTION</span></span>
<span data-ttu-id="86623-109">A rendszerszolgáltatásokat a operationalization-fürttől függetlenül is frissítheti.</span><span class="sxs-lookup"><span data-stu-id="86623-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="86623-110">A rendszerszolgáltatások frissítésének indításához használja ezt a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="86623-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="86623-111">Ha nincs elérhető frissítés, a rendszer továbbra is elindít egy frissítést, és sikeresen visszaadja.</span><span class="sxs-lookup"><span data-stu-id="86623-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="86623-112">Miután a frissítés befejeződött, a jelentések a kezdéskor, a befejezett és a sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="86623-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="86623-113">Példák</span><span class="sxs-lookup"><span data-stu-id="86623-113">EXAMPLES</span></span>

### <span data-ttu-id="86623-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="86623-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="86623-115">Elindítja a rendszerszolgáltatások frissítését a megadott fürtön.</span><span class="sxs-lookup"><span data-stu-id="86623-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="86623-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86623-116">PARAMETERS</span></span>

### <span data-ttu-id="86623-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86623-117">-InputObject</span></span>
<span data-ttu-id="86623-118">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="86623-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86623-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86623-119">-Confirm</span></span>
<span data-ttu-id="86623-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86623-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86623-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86623-121">-Name</span></span>
<span data-ttu-id="86623-122">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="86623-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86623-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86623-123">-ResourceGroupName</span></span>
<span data-ttu-id="86623-124">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="86623-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86623-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86623-125">-ResourceId</span></span>
<span data-ttu-id="86623-126">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="86623-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86623-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86623-127">-WhatIf</span></span>
<span data-ttu-id="86623-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86623-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86623-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86623-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="86623-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86623-130">INPUTS</span></span>

### <span data-ttu-id="86623-131">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="86623-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="86623-132">System. String</span><span class="sxs-lookup"><span data-stu-id="86623-132">System.String</span></span>


## <span data-ttu-id="86623-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86623-133">OUTPUTS</span></span>

### <span data-ttu-id="86623-134">Microsoft. Azure. Command. MachineLearningCompute. models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="86623-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>


## <span data-ttu-id="86623-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86623-135">NOTES</span></span>

## <span data-ttu-id="86623-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86623-136">RELATED LINKS</span></span>

