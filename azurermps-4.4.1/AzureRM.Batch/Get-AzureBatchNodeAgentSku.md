---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: e29b5df4a72ff21dbacb0928b298306eb585b493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502787"
---
# <span data-ttu-id="84c3d-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="84c3d-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="84c3d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="84c3d-103">Köteg-csomópont ügynöki SKU-t kap egy köteg fiókban.</span><span class="sxs-lookup"><span data-stu-id="84c3d-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84c3d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84c3d-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84c3d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="84c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="84c3d-106">A **Get-AzureBatchNodeAgentSku** parancsmag az Azure-alapú köteg fiókokban elérhető, csomópont-ügynököt tartalmazó SKU-t kapja.</span><span class="sxs-lookup"><span data-stu-id="84c3d-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="84c3d-107">Adja meg a fiókot a *BatchContext* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="84c3d-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="84c3d-108">Szűkítheti a keresést olyan SKU-ra, amely megfelel egy Open Data Protocol (OData) szűrőnek.</span><span class="sxs-lookup"><span data-stu-id="84c3d-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="84c3d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="84c3d-109">EXAMPLES</span></span>

### <span data-ttu-id="84c3d-110">1. példa: az összes elérhető csomópont ügynöki SKU beszerzése</span><span class="sxs-lookup"><span data-stu-id="84c3d-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="84c3d-111">Az első parancs a **Get-AzureRmBatchAccountKeys használatával beolvassa** az előfizetéshez a hozzáférési kulcsokat tartalmazó kötegelt fiók környezetét.</span><span class="sxs-lookup"><span data-stu-id="84c3d-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="84c3d-112">A parancs a következő parancsban a $Context változó környezetét tárolja.</span><span class="sxs-lookup"><span data-stu-id="84c3d-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="84c3d-113">A második parancs beolvassa az összes elérhető Node Agent SKU-t, amelyet a köteg támogat.</span><span class="sxs-lookup"><span data-stu-id="84c3d-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="84c3d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84c3d-114">PARAMETERS</span></span>

### <span data-ttu-id="84c3d-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="84c3d-115">-BatchContext</span></span>
<span data-ttu-id="84c3d-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="84c3d-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="84c3d-117">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="84c3d-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84c3d-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="84c3d-118">-Filter</span></span>
<span data-ttu-id="84c3d-119">A OData-szűrési záradékot adja meg a Node Agent SKU-hoz.</span><span class="sxs-lookup"><span data-stu-id="84c3d-119">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="84c3d-120">Ha nem ad meg szűrőt, a parancsmag minden olyan csomópont-ügynököt visszaad, amelyet a köteg támogat.</span><span class="sxs-lookup"><span data-stu-id="84c3d-120">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c3d-121">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="84c3d-121">-MaxCount</span></span>
<span data-ttu-id="84c3d-122">Azt adja meg, hogy legfeljebb hány csomópontos SKU-t szeretne visszaadni.</span><span class="sxs-lookup"><span data-stu-id="84c3d-122">Specifies the maximum number of node agent SKUs to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c3d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c3d-123">-DefaultProfile</span></span>
<span data-ttu-id="84c3d-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84c3d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84c3d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c3d-125">CommonParameters</span></span>
<span data-ttu-id="84c3d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84c3d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c3d-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84c3d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c3d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84c3d-128">INPUTS</span></span>

### <span data-ttu-id="84c3d-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="84c3d-129">BatchAccountContext</span></span>
<span data-ttu-id="84c3d-130">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="84c3d-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="84c3d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84c3d-131">OUTPUTS</span></span>

### <span data-ttu-id="84c3d-132">Microsoft.Azure.Commands.BatCH. Modellek. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="84c3d-132">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="84c3d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84c3d-133">NOTES</span></span>

## <span data-ttu-id="84c3d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84c3d-134">RELATED LINKS</span></span>

[<span data-ttu-id="84c3d-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="84c3d-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

