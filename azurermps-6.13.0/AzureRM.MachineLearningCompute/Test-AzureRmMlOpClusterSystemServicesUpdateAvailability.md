---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/test-azurermmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 9832faaaaf1097f53aff841f8a455680b2a40a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495988"
---
# <span data-ttu-id="2ba16-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="2ba16-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="2ba16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ba16-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba16-103">Ellenőrzi, hogy vannak-e a operationalization-fürtökhöz társított rendszerszolgáltatásokhoz elérhető frissítések.</span><span class="sxs-lookup"><span data-stu-id="2ba16-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ba16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ba16-104">SYNTAX</span></span>

### <span data-ttu-id="2ba16-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2ba16-105">TestByNameAndResourceGroup</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ba16-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="2ba16-106">TestByInputObject</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ba16-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="2ba16-107">TestByResourceId</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ba16-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ba16-108">DESCRIPTION</span></span>
<span data-ttu-id="2ba16-109">A rendszerszolgáltatások a operationalization-fürttől függetlenül kapják meg a frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="2ba16-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="2ba16-110">Ezzel a parancsmaggal a felhasználó megtudhatja, hogy AzureRmMlOpClusterSystemServicesUpdate-e.</span><span class="sxs-lookup"><span data-stu-id="2ba16-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="2ba16-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2ba16-111">EXAMPLES</span></span>

### <span data-ttu-id="2ba16-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2ba16-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="2ba16-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2ba16-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="2ba16-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="2ba16-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="2ba16-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ba16-115">PARAMETERS</span></span>

### <span data-ttu-id="2ba16-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba16-116">-DefaultProfile</span></span>
<span data-ttu-id="2ba16-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ba16-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ba16-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ba16-118">-InputObject</span></span>
<span data-ttu-id="2ba16-119">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="2ba16-119">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba16-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ba16-120">-Name</span></span>
<span data-ttu-id="2ba16-121">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="2ba16-121">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba16-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ba16-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ba16-123">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ba16-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba16-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ba16-124">-ResourceId</span></span>
<span data-ttu-id="2ba16-125">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="2ba16-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba16-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba16-126">CommonParameters</span></span>
<span data-ttu-id="2ba16-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ba16-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba16-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ba16-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba16-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ba16-129">INPUTS</span></span>

### <span data-ttu-id="2ba16-130">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="2ba16-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="2ba16-131">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ba16-131">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2ba16-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2ba16-132">System.String</span></span>

## <span data-ttu-id="2ba16-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ba16-133">OUTPUTS</span></span>

### <span data-ttu-id="2ba16-134">Microsoft. Azure. Command. MachineLearningCompute. models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="2ba16-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="2ba16-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ba16-135">NOTES</span></span>

## <span data-ttu-id="2ba16-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ba16-136">RELATED LINKS</span></span>
