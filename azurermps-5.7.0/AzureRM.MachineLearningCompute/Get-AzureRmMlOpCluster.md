---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 0e9eecf16a26be5367df5d8ad8b45a40e0050da3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672640"
---
# <span data-ttu-id="3898d-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="3898d-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="3898d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3898d-102">SYNOPSIS</span></span>
<span data-ttu-id="3898d-103">Kap egy operationalization-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="3898d-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3898d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3898d-104">SYNTAX</span></span>

### <span data-ttu-id="3898d-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="3898d-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3898d-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3898d-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3898d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3898d-107">DESCRIPTION</span></span>
<span data-ttu-id="3898d-108">Egy operationalization-fürt objektumát név, vagy erőforráscsoport szerint, illetve előfizetéssel kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3898d-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="3898d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3898d-109">EXAMPLES</span></span>

### <span data-ttu-id="3898d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3898d-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="3898d-111">Adott operationalization-fürtöt kap név szerint.</span><span class="sxs-lookup"><span data-stu-id="3898d-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="3898d-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="3898d-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="3898d-113">Egy erőforráscsoport összes operationalization-fürtjét kapja.</span><span class="sxs-lookup"><span data-stu-id="3898d-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="3898d-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="3898d-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="3898d-115">Az előfizetésben lévő összes operationalization-szektorcsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="3898d-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="3898d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3898d-116">PARAMETERS</span></span>

### <span data-ttu-id="3898d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3898d-117">-DefaultProfile</span></span>
<span data-ttu-id="3898d-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3898d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3898d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3898d-119">-Name</span></span>
<span data-ttu-id="3898d-120">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="3898d-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3898d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3898d-121">-ResourceGroupName</span></span>
<span data-ttu-id="3898d-122">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3898d-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3898d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3898d-123">CommonParameters</span></span>
<span data-ttu-id="3898d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3898d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3898d-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3898d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3898d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3898d-126">INPUTS</span></span>

### <span data-ttu-id="3898d-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="3898d-127">None</span></span>

## <span data-ttu-id="3898d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3898d-128">OUTPUTS</span></span>

### <span data-ttu-id="3898d-129">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="3898d-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="3898d-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster, Microsoft. Azure. commands. MachineLearningCompute, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3898d-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3898d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3898d-131">NOTES</span></span>

## <span data-ttu-id="3898d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3898d-132">RELATED LINKS</span></span>

