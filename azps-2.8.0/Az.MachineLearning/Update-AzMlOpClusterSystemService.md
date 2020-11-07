---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
ms.openlocfilehash: 0e673cd74d87cee990130c1fd58b9049eec9ff15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665951"
---
# <span data-ttu-id="3ebe1-101">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="3ebe1-101">Update-AzMlOpClusterSystemService</span></span>

## <span data-ttu-id="3ebe1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ebe1-102">SYNOPSIS</span></span>
<span data-ttu-id="3ebe1-103">Elindítja a operationalization-fürt rendszerszolgáltatásainak frissítését.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-103">Starts an update on the operationalization cluster's system services.</span></span>

## <span data-ttu-id="3ebe1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ebe1-104">SYNTAX</span></span>

### <span data-ttu-id="3ebe1-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3ebe1-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ebe1-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="3ebe1-106">StartUpdateWithInputObject</span></span>
```
Update-AzMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ebe1-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="3ebe1-107">StartUpdateWithResourceId</span></span>
```
Update-AzMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ebe1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ebe1-108">DESCRIPTION</span></span>
<span data-ttu-id="3ebe1-109">A rendszerszolgáltatásokat a operationalization-fürttől függetlenül is frissítheti.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="3ebe1-110">A rendszerszolgáltatások frissítésének indításához használja ezt a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="3ebe1-111">Ha nincs elérhető frissítés, a rendszer továbbra is elindít egy frissítést, és sikeresen visszaadja.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="3ebe1-112">Miután a frissítés befejeződött, a jelentések a kezdéskor, a befejezett és a sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="3ebe1-113">Példák</span><span class="sxs-lookup"><span data-stu-id="3ebe1-113">EXAMPLES</span></span>

### <span data-ttu-id="3ebe1-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3ebe1-114">Example 1</span></span>
```
PS C:\> Update-AzMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="3ebe1-115">Elindítja a rendszerszolgáltatások frissítését a megadott fürtön.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="3ebe1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ebe1-116">PARAMETERS</span></span>

### <span data-ttu-id="3ebe1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ebe1-117">-DefaultProfile</span></span>
<span data-ttu-id="3ebe1-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ebe1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ebe1-119">-InputObject</span></span>
<span data-ttu-id="3ebe1-120">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="3ebe1-120">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe1-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ebe1-121">-Name</span></span>
<span data-ttu-id="3ebe1-122">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-122">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ebe1-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ebe1-124">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ebe1-125">-ResourceId</span></span>
<span data-ttu-id="3ebe1-126">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe1-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ebe1-127">-Confirm</span></span>
<span data-ttu-id="3ebe1-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ebe1-129">-WhatIf</span></span>
<span data-ttu-id="3ebe1-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ebe1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ebe1-132">CommonParameters</span></span>
<span data-ttu-id="3ebe1-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ebe1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ebe1-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ebe1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ebe1-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ebe1-135">INPUTS</span></span>

### <span data-ttu-id="3ebe1-136">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="3ebe1-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="3ebe1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3ebe1-137">System.String</span></span>

## <span data-ttu-id="3ebe1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ebe1-138">OUTPUTS</span></span>

### <span data-ttu-id="3ebe1-139">Microsoft. Azure. Command. MachineLearningCompute. models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="3ebe1-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="3ebe1-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ebe1-140">NOTES</span></span>

## <span data-ttu-id="3ebe1-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ebe1-141">RELATED LINKS</span></span>
