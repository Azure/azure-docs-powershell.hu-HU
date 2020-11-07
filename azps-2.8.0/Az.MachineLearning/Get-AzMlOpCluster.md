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
ms.locfileid: "93665983"
---
# <span data-ttu-id="c0ab6-101">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="c0ab6-101">Get-AzMlOpCluster</span></span>

## <span data-ttu-id="c0ab6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ab6-103">Kap egy operationalization-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="c0ab6-103">Gets an operationalization cluster object.</span></span>

## <span data-ttu-id="c0ab6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0ab6-104">SYNTAX</span></span>

### <span data-ttu-id="c0ab6-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="c0ab6-105">GetByName</span></span>
```
Get-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0ab6-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c0ab6-106">GetByResourceGroup</span></span>
```
Get-AzMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0ab6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0ab6-107">DESCRIPTION</span></span>
<span data-ttu-id="c0ab6-108">Egy operationalization-fürt objektumát név, vagy erőforráscsoport szerint, illetve előfizetéssel kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c0ab6-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="c0ab6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c0ab6-109">EXAMPLES</span></span>

### <span data-ttu-id="c0ab6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c0ab6-110">Example 1</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="c0ab6-111">Adott operationalization-fürtöt kap név szerint.</span><span class="sxs-lookup"><span data-stu-id="c0ab6-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="c0ab6-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c0ab6-112">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="c0ab6-113">Egy erőforráscsoport összes operationalization-fürtjét kapja.</span><span class="sxs-lookup"><span data-stu-id="c0ab6-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="c0ab6-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="c0ab6-114">Example 3</span></span>
```
PS C:\> Get-AzMlOpCluster
```

<span data-ttu-id="c0ab6-115">Az előfizetésben lévő összes operationalization-szektorcsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="c0ab6-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="c0ab6-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0ab6-116">PARAMETERS</span></span>

### <span data-ttu-id="c0ab6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ab6-117">-DefaultProfile</span></span>
<span data-ttu-id="c0ab6-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0ab6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0ab6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0ab6-119">-Name</span></span>
<span data-ttu-id="c0ab6-120">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c0ab6-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="c0ab6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ab6-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0ab6-122">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c0ab6-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="c0ab6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ab6-123">CommonParameters</span></span>
<span data-ttu-id="c0ab6-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0ab6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ab6-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0ab6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ab6-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0ab6-126">INPUTS</span></span>

### <span data-ttu-id="c0ab6-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="c0ab6-127">None</span></span>

## <span data-ttu-id="c0ab6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0ab6-128">OUTPUTS</span></span>

### <span data-ttu-id="c0ab6-129">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="c0ab6-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="c0ab6-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0ab6-130">NOTES</span></span>

## <span data-ttu-id="c0ab6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0ab6-131">RELATED LINKS</span></span>
