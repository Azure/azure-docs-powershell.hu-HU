---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501776"
---
# <span data-ttu-id="c9430-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="c9430-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="c9430-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9430-102">SYNOPSIS</span></span>
<span data-ttu-id="c9430-103">Beolvassa a operationalization-fürtökhöz társított hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="c9430-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9430-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9430-104">SYNTAX</span></span>

### <span data-ttu-id="c9430-105">A operationalization-fürt kulcsai a parancsmag bemeneti paramétereinek beszerzése.</span><span class="sxs-lookup"><span data-stu-id="c9430-105">Get operationalization cluster's keys from cmdlet input parameters.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="c9430-106">Beolvashatja a operationalization-fürt kulcsait egy OperationalizationCluster-példányból.</span><span class="sxs-lookup"><span data-stu-id="c9430-106">Get operationalization cluster's keys from an OperationalizationCluster instance definition.</span></span>
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### <span data-ttu-id="c9430-107">Azure-erőforrás-azonosítóból szerezheti be a operationalization-fürt kulcsait.</span><span class="sxs-lookup"><span data-stu-id="c9430-107">Get operationalization cluster's keys from an Azure resource id.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## <span data-ttu-id="c9430-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9430-108">DESCRIPTION</span></span>
<span data-ttu-id="c9430-109">A operationalization-fürthöz társított tárolási fiók, tároló-nyilvántartó és más szolgáltatások kulcsai nem jelennek meg a fürt tulajdonságainak beszerzése során.</span><span class="sxs-lookup"><span data-stu-id="c9430-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="c9430-110">A billentyűk lekérésének konkrét hívását el kell végeznie, mert bizalmas adatok.</span><span class="sxs-lookup"><span data-stu-id="c9430-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="c9430-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c9430-111">EXAMPLES</span></span>

### <span data-ttu-id="c9430-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c9430-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="c9430-113">A operationalization-fürthöz társított szolgáltatások titkos kulcsait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c9430-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="c9430-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9430-114">PARAMETERS</span></span>

### <span data-ttu-id="c9430-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9430-115">-InputObject</span></span>
<span data-ttu-id="c9430-116">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="c9430-116">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9430-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c9430-117">-Name</span></span>
<span data-ttu-id="c9430-118">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c9430-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9430-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9430-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9430-120">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c9430-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9430-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9430-121">-ResourceId</span></span>
<span data-ttu-id="c9430-122">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="c9430-122">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="c9430-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9430-123">INPUTS</span></span>

### <span data-ttu-id="c9430-124">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="c9430-124">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="c9430-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c9430-125">System.String</span></span>


## <span data-ttu-id="c9430-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9430-126">OUTPUTS</span></span>

### <span data-ttu-id="c9430-127">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="c9430-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>


## <span data-ttu-id="c9430-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9430-128">NOTES</span></span>

## <span data-ttu-id="c9430-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9430-129">RELATED LINKS</span></span>

