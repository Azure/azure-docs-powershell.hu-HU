---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: e37aff4f6f79a3aa0420c98811bc47b951bb4d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500831"
---
# <span data-ttu-id="d73aa-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d73aa-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="d73aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d73aa-102">SYNOPSIS</span></span>
<span data-ttu-id="d73aa-103">Kap egy operationalization-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="d73aa-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d73aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d73aa-104">SYNTAX</span></span>

```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d73aa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d73aa-105">DESCRIPTION</span></span>
<span data-ttu-id="d73aa-106">Egy operationalization-fürt objektumát név, vagy erőforráscsoport szerint, illetve előfizetéssel kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d73aa-106">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="d73aa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d73aa-107">EXAMPLES</span></span>

### <span data-ttu-id="d73aa-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d73aa-108">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="d73aa-109">Adott operationalization-fürtöt kap név szerint.</span><span class="sxs-lookup"><span data-stu-id="d73aa-109">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="d73aa-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="d73aa-110">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="d73aa-111">Egy erőforráscsoport összes operationalization-fürtjét kapja.</span><span class="sxs-lookup"><span data-stu-id="d73aa-111">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="d73aa-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="d73aa-112">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="d73aa-113">Az előfizetésben lévő összes operationalization-szektorcsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="d73aa-113">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="d73aa-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d73aa-114">PARAMETERS</span></span>

### <span data-ttu-id="d73aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d73aa-115">-DefaultProfile</span></span>
<span data-ttu-id="d73aa-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d73aa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d73aa-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d73aa-117">-Name</span></span>
<span data-ttu-id="d73aa-118">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="d73aa-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get an operationalization cluster by its name.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d73aa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d73aa-119">-ResourceGroupName</span></span>
<span data-ttu-id="d73aa-120">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d73aa-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d73aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d73aa-121">CommonParameters</span></span>
<span data-ttu-id="d73aa-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d73aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d73aa-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d73aa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d73aa-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d73aa-124">INPUTS</span></span>

### <span data-ttu-id="d73aa-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="d73aa-125">None</span></span>

## <span data-ttu-id="d73aa-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d73aa-126">OUTPUTS</span></span>

### <span data-ttu-id="d73aa-127">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="d73aa-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="d73aa-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster, Microsoft. Azure. commands. MachineLearningCompute, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d73aa-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d73aa-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d73aa-129">NOTES</span></span>

## <span data-ttu-id="d73aa-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d73aa-130">RELATED LINKS</span></span>

