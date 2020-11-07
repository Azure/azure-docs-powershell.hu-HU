---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/test-azmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: d05f8b746dbd212c834e3554639340fa6075c216
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665956"
---
# <span data-ttu-id="bfd3c-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="bfd3c-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="bfd3c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bfd3c-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd3c-103">Ellenőrzi, hogy vannak-e a operationalization-fürtökhöz társított rendszerszolgáltatásokhoz elérhető frissítések.</span><span class="sxs-lookup"><span data-stu-id="bfd3c-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

## <span data-ttu-id="bfd3c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bfd3c-104">SYNTAX</span></span>

### <span data-ttu-id="bfd3c-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bfd3c-105">TestByNameAndResourceGroup</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfd3c-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="bfd3c-106">TestByInputObject</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfd3c-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="bfd3c-107">TestByResourceId</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfd3c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bfd3c-108">DESCRIPTION</span></span>
<span data-ttu-id="bfd3c-109">A rendszerszolgáltatások a operationalization-fürttől függetlenül kapják meg a frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="bfd3c-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="bfd3c-110">Ezzel a parancsmaggal a felhasználó megtudhatja, hogy AzMlOpClusterSystemServicesUpdate-e.</span><span class="sxs-lookup"><span data-stu-id="bfd3c-110">Using this cmdlet will let the user know if Invoke-AzMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="bfd3c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="bfd3c-111">EXAMPLES</span></span>

### <span data-ttu-id="bfd3c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bfd3c-112">Example 1</span></span>
```
PS C:\> Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="bfd3c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="bfd3c-113">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="bfd3c-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="bfd3c-114">Example 3</span></span>
```
PS C:\> Find-AzResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="bfd3c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bfd3c-115">PARAMETERS</span></span>

### <span data-ttu-id="bfd3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd3c-116">-DefaultProfile</span></span>
<span data-ttu-id="bfd3c-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfd3c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfd3c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfd3c-118">-InputObject</span></span>
<span data-ttu-id="bfd3c-119">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="bfd3c-119">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="bfd3c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bfd3c-120">-Name</span></span>
<span data-ttu-id="bfd3c-121">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="bfd3c-121">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="bfd3c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfd3c-122">-ResourceGroupName</span></span>
<span data-ttu-id="bfd3c-123">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bfd3c-123">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="bfd3c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfd3c-124">-ResourceId</span></span>
<span data-ttu-id="bfd3c-125">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="bfd3c-125">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="bfd3c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd3c-126">CommonParameters</span></span>
<span data-ttu-id="bfd3c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bfd3c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd3c-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfd3c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd3c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfd3c-129">INPUTS</span></span>

### <span data-ttu-id="bfd3c-130">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="bfd3c-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="bfd3c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bfd3c-131">System.String</span></span>

## <span data-ttu-id="bfd3c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfd3c-132">OUTPUTS</span></span>

### <span data-ttu-id="bfd3c-133">Microsoft. Azure. Command. MachineLearningCompute. models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="bfd3c-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="bfd3c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bfd3c-134">NOTES</span></span>

## <span data-ttu-id="bfd3c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfd3c-135">RELATED LINKS</span></span>
