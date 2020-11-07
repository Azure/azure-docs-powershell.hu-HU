---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/update-azurermmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: 01f826746b92dd5aa82416e8207305b945ddb711
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673047"
---
# <span data-ttu-id="534c2-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="534c2-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="534c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="534c2-102">SYNOPSIS</span></span>
<span data-ttu-id="534c2-103">Elindítja a operationalization-fürt rendszerszolgáltatásainak frissítését.</span><span class="sxs-lookup"><span data-stu-id="534c2-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="534c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="534c2-104">SYNTAX</span></span>

### <span data-ttu-id="534c2-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="534c2-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="534c2-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="534c2-106">StartUpdateWithInputObject</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="534c2-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="534c2-107">StartUpdateWithResourceId</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="534c2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="534c2-108">DESCRIPTION</span></span>
<span data-ttu-id="534c2-109">A rendszerszolgáltatásokat a operationalization-fürttől függetlenül is frissítheti.</span><span class="sxs-lookup"><span data-stu-id="534c2-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="534c2-110">A rendszerszolgáltatások frissítésének indításához használja ezt a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="534c2-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="534c2-111">Ha nincs elérhető frissítés, a rendszer továbbra is elindít egy frissítést, és sikeresen visszaadja.</span><span class="sxs-lookup"><span data-stu-id="534c2-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="534c2-112">Miután a frissítés befejeződött, a jelentések a kezdéskor, a befejezett és a sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="534c2-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="534c2-113">Példák</span><span class="sxs-lookup"><span data-stu-id="534c2-113">EXAMPLES</span></span>

### <span data-ttu-id="534c2-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="534c2-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="534c2-115">Elindítja a rendszerszolgáltatások frissítését a megadott fürtön.</span><span class="sxs-lookup"><span data-stu-id="534c2-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="534c2-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="534c2-116">PARAMETERS</span></span>

### <span data-ttu-id="534c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534c2-117">-DefaultProfile</span></span>
<span data-ttu-id="534c2-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="534c2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="534c2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="534c2-119">-InputObject</span></span>
<span data-ttu-id="534c2-120">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="534c2-120">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="534c2-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="534c2-121">-Name</span></span>
<span data-ttu-id="534c2-122">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="534c2-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="534c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="534c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="534c2-124">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="534c2-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="534c2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="534c2-125">-ResourceId</span></span>
<span data-ttu-id="534c2-126">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="534c2-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="534c2-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="534c2-127">-Confirm</span></span>
<span data-ttu-id="534c2-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="534c2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="534c2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="534c2-129">-WhatIf</span></span>
<span data-ttu-id="534c2-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="534c2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="534c2-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="534c2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="534c2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534c2-132">CommonParameters</span></span>
<span data-ttu-id="534c2-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="534c2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534c2-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="534c2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534c2-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="534c2-135">INPUTS</span></span>

### <span data-ttu-id="534c2-136">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="534c2-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="534c2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="534c2-137">System.String</span></span>

## <span data-ttu-id="534c2-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="534c2-138">OUTPUTS</span></span>

### <span data-ttu-id="534c2-139">Microsoft. Azure. Command. MachineLearningCompute. models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="534c2-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="534c2-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="534c2-140">NOTES</span></span>

## <span data-ttu-id="534c2-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="534c2-141">RELATED LINKS</span></span>

