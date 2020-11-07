---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 067fdf88b7a7b29007f81ab26590ffaa542ac7e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679070"
---
# <span data-ttu-id="c6cfa-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="c6cfa-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="c6cfa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="c6cfa-103">Ellenőrzi, hogy vannak-e a operationalization-fürtökhöz társított rendszerszolgáltatásokhoz elérhető frissítések.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6cfa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6cfa-104">SYNTAX</span></span>

### <span data-ttu-id="c6cfa-105">Tesztelés a parancsmag bemeneti paramétereinek frissítésének elérhetőségéről.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-105">Test for update availability from cmdlet input parameters.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="c6cfa-106">Tesztelés a OperationalizationCluster példány frissítésének elérhetőségéről</span><span class="sxs-lookup"><span data-stu-id="c6cfa-106">Test for update availability from an OperationalizationCluster instance definition.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
```

### <span data-ttu-id="c6cfa-107">Tesztelés az Azure Resouce-azonosítók frissítésének elérhetőségéről</span><span class="sxs-lookup"><span data-stu-id="c6cfa-107">Test for update availability from an Azure resouce id.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
```

## <span data-ttu-id="c6cfa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6cfa-108">DESCRIPTION</span></span>
<span data-ttu-id="c6cfa-109">A rendszerszolgáltatások a operationalization-fürttől függetlenül kapják meg a frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="c6cfa-110">Ezzel a parancsmaggal a felhasználó megtudhatja, hogy AzureRmMlOpClusterSystemServicesUpdate-e.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="c6cfa-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c6cfa-111">EXAMPLES</span></span>

### <span data-ttu-id="c6cfa-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c6cfa-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="c6cfa-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c6cfa-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="c6cfa-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="c6cfa-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="c6cfa-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6cfa-115">PARAMETERS</span></span>

### <span data-ttu-id="c6cfa-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6cfa-116">-InputObject</span></span>
<span data-ttu-id="c6cfa-117">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="c6cfa-117">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Test for update availability from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6cfa-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6cfa-118">-Name</span></span>
<span data-ttu-id="c6cfa-119">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-119">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6cfa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6cfa-120">-ResourceGroupName</span></span>
<span data-ttu-id="c6cfa-121">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-121">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6cfa-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6cfa-122">-ResourceId</span></span>
<span data-ttu-id="c6cfa-123">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-123">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="c6cfa-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6cfa-124">INPUTS</span></span>

### <span data-ttu-id="c6cfa-125">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="c6cfa-125">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="c6cfa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c6cfa-126">System.String</span></span>


## <span data-ttu-id="c6cfa-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6cfa-127">OUTPUTS</span></span>

### <span data-ttu-id="c6cfa-128">Microsoft. Azure. Command. MachineLearningCompute. models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="c6cfa-128">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>


## <span data-ttu-id="c6cfa-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6cfa-129">NOTES</span></span>

## <span data-ttu-id="c6cfa-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6cfa-130">RELATED LINKS</span></span>

