---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
ms.openlocfilehash: 24400b7a2c882cef81d818c5f5b94fca4235ec83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835317"
---
# <span data-ttu-id="294f2-101">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="294f2-101">Get-AzMlOpCluster</span></span>

## <span data-ttu-id="294f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="294f2-102">SYNOPSIS</span></span>
<span data-ttu-id="294f2-103">Kap egy operationalization-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="294f2-103">Gets an operationalization cluster object.</span></span>

## <span data-ttu-id="294f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="294f2-104">SYNTAX</span></span>

### <span data-ttu-id="294f2-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="294f2-105">GetByName</span></span>
```
Get-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="294f2-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="294f2-106">GetByResourceGroup</span></span>
```
Get-AzMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="294f2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="294f2-107">DESCRIPTION</span></span>
<span data-ttu-id="294f2-108">Egy operationalization-fürt objektumát név, vagy erőforráscsoport szerint, illetve előfizetéssel kapja meg.</span><span class="sxs-lookup"><span data-stu-id="294f2-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="294f2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="294f2-109">EXAMPLES</span></span>

### <span data-ttu-id="294f2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="294f2-110">Example 1</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="294f2-111">Adott operationalization-fürtöt kap név szerint.</span><span class="sxs-lookup"><span data-stu-id="294f2-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="294f2-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="294f2-112">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="294f2-113">Egy erőforráscsoport összes operationalization-fürtjét kapja.</span><span class="sxs-lookup"><span data-stu-id="294f2-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="294f2-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="294f2-114">Example 3</span></span>
```
PS C:\> Get-AzMlOpCluster
```

<span data-ttu-id="294f2-115">Az előfizetésben lévő összes operationalization-szektorcsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="294f2-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="294f2-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="294f2-116">PARAMETERS</span></span>

### <span data-ttu-id="294f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="294f2-117">-DefaultProfile</span></span>
<span data-ttu-id="294f2-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="294f2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="294f2-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="294f2-119">-Name</span></span>
<span data-ttu-id="294f2-120">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="294f2-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="294f2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="294f2-121">-ResourceGroupName</span></span>
<span data-ttu-id="294f2-122">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="294f2-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="294f2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294f2-123">CommonParameters</span></span>
<span data-ttu-id="294f2-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="294f2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294f2-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="294f2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294f2-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="294f2-126">INPUTS</span></span>

### <span data-ttu-id="294f2-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="294f2-127">None</span></span>

## <span data-ttu-id="294f2-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="294f2-128">OUTPUTS</span></span>

### <span data-ttu-id="294f2-129">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="294f2-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="294f2-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="294f2-130">NOTES</span></span>

## <span data-ttu-id="294f2-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="294f2-131">RELATED LINKS</span></span>
