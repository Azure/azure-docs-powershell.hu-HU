---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
ms.openlocfilehash: d8b8a333b4d009ee1b40a8b4ddc6ed49850f1a11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835310"
---
# <span data-ttu-id="08cb8-101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="08cb8-101">Get-AzMlOpClusterKey</span></span>

## <span data-ttu-id="08cb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="08cb8-103">Beolvassa a operationalization-fürtökhöz társított hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="08cb8-103">Gets the access keys associated with an operationalization cluster.</span></span>

## <span data-ttu-id="08cb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08cb8-104">SYNTAX</span></span>

### <span data-ttu-id="08cb8-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="08cb8-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08cb8-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="08cb8-106">GetByInputObject</span></span>
```
Get-AzMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08cb8-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="08cb8-107">GetByResourceId</span></span>
```
Get-AzMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08cb8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="08cb8-108">DESCRIPTION</span></span>
<span data-ttu-id="08cb8-109">A operationalization-fürthöz társított tárolási fiók, tároló-nyilvántartó és más szolgáltatások kulcsai nem jelennek meg a fürt tulajdonságainak beszerzése során.</span><span class="sxs-lookup"><span data-stu-id="08cb8-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="08cb8-110">A billentyűk lekérésének konkrét hívását el kell végeznie, mert bizalmas adatok.</span><span class="sxs-lookup"><span data-stu-id="08cb8-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="08cb8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="08cb8-111">EXAMPLES</span></span>

### <span data-ttu-id="08cb8-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08cb8-112">Example 1</span></span>
```
PS C:\> Get-AzMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="08cb8-113">A operationalization-fürthöz társított szolgáltatások titkos kulcsait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="08cb8-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="08cb8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08cb8-114">PARAMETERS</span></span>

### <span data-ttu-id="08cb8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08cb8-115">-DefaultProfile</span></span>
<span data-ttu-id="08cb8-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08cb8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08cb8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08cb8-117">-InputObject</span></span>
<span data-ttu-id="08cb8-118">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="08cb8-118">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08cb8-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08cb8-119">-Name</span></span>
<span data-ttu-id="08cb8-120">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="08cb8-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08cb8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08cb8-121">-ResourceGroupName</span></span>
<span data-ttu-id="08cb8-122">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="08cb8-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08cb8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08cb8-123">-ResourceId</span></span>
<span data-ttu-id="08cb8-124">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="08cb8-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08cb8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08cb8-125">CommonParameters</span></span>
<span data-ttu-id="08cb8-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08cb8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08cb8-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08cb8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08cb8-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08cb8-128">INPUTS</span></span>

### <span data-ttu-id="08cb8-129">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="08cb8-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="08cb8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="08cb8-130">System.String</span></span>

## <span data-ttu-id="08cb8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08cb8-131">OUTPUTS</span></span>

### <span data-ttu-id="08cb8-132">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="08cb8-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="08cb8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08cb8-133">NOTES</span></span>

## <span data-ttu-id="08cb8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08cb8-134">RELATED LINKS</span></span>
