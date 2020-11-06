---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 6b5797d67b709e9c44756dad018a47eb416ed174
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495996"
---
# <span data-ttu-id="42427-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="42427-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="42427-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42427-102">SYNOPSIS</span></span>
<span data-ttu-id="42427-103">Beolvassa a operationalization-fürtökhöz társított hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="42427-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42427-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42427-104">SYNTAX</span></span>

### <span data-ttu-id="42427-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42427-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42427-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="42427-106">GetByInputObject</span></span>
```
Get-AzureRmMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42427-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="42427-107">GetByResourceId</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42427-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="42427-108">DESCRIPTION</span></span>
<span data-ttu-id="42427-109">A operationalization-fürthöz társított tárolási fiók, tároló-nyilvántartó és más szolgáltatások kulcsai nem jelennek meg a fürt tulajdonságainak beszerzése során.</span><span class="sxs-lookup"><span data-stu-id="42427-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="42427-110">A billentyűk lekérésének konkrét hívását el kell végeznie, mert bizalmas adatok.</span><span class="sxs-lookup"><span data-stu-id="42427-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="42427-111">Példák</span><span class="sxs-lookup"><span data-stu-id="42427-111">EXAMPLES</span></span>

### <span data-ttu-id="42427-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="42427-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="42427-113">A operationalization-fürthöz társított szolgáltatások titkos kulcsait számítja ki.</span><span class="sxs-lookup"><span data-stu-id="42427-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="42427-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42427-114">PARAMETERS</span></span>

### <span data-ttu-id="42427-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42427-115">-DefaultProfile</span></span>
<span data-ttu-id="42427-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42427-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42427-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42427-117">-InputObject</span></span>
<span data-ttu-id="42427-118">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="42427-118">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="42427-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="42427-119">-Name</span></span>
<span data-ttu-id="42427-120">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="42427-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="42427-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42427-121">-ResourceGroupName</span></span>
<span data-ttu-id="42427-122">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="42427-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="42427-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42427-123">-ResourceId</span></span>
<span data-ttu-id="42427-124">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="42427-124">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="42427-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42427-125">CommonParameters</span></span>
<span data-ttu-id="42427-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42427-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42427-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42427-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42427-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42427-128">INPUTS</span></span>

### <span data-ttu-id="42427-129">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="42427-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="42427-130">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="42427-130">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="42427-131">System. String</span><span class="sxs-lookup"><span data-stu-id="42427-131">System.String</span></span>

## <span data-ttu-id="42427-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42427-132">OUTPUTS</span></span>

### <span data-ttu-id="42427-133">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="42427-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="42427-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42427-134">NOTES</span></span>

## <span data-ttu-id="42427-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42427-135">RELATED LINKS</span></span>
