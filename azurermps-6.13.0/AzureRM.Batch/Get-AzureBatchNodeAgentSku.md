---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: 86451c1ac7ba52c9b013b3724d9c706caaa961ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492009"
---
# <span data-ttu-id="16781-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="16781-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="16781-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16781-102">SYNOPSIS</span></span>
<span data-ttu-id="16781-103">Köteg-csomópont ügynöki SKU-t kap egy köteg fiókban.</span><span class="sxs-lookup"><span data-stu-id="16781-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16781-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16781-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16781-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="16781-105">DESCRIPTION</span></span>
<span data-ttu-id="16781-106">A **Get-AzureBatchNodeAgentSku** parancsmag az Azure-alapú köteg fiókokban elérhető, csomópont-ügynököt tartalmazó SKU-t kapja.</span><span class="sxs-lookup"><span data-stu-id="16781-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="16781-107">Adja meg a fiókot a *BatchContext* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="16781-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="16781-108">Szűkítheti a keresést olyan SKU-ra, amely megfelel egy Open Data Protocol (OData) szűrőnek.</span><span class="sxs-lookup"><span data-stu-id="16781-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="16781-109">Példák</span><span class="sxs-lookup"><span data-stu-id="16781-109">EXAMPLES</span></span>

### <span data-ttu-id="16781-110">1. példa: az összes elérhető csomópont ügynöki SKU beszerzése</span><span class="sxs-lookup"><span data-stu-id="16781-110">Example 1: Get all available node agent SKUs</span></span>
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

<span data-ttu-id="16781-111">Az első parancs a **Get-AzureRmBatchAccountKeys használatával beolvassa** az előfizetéshez a hozzáférési kulcsokat tartalmazó kötegelt fiók környezetét.</span><span class="sxs-lookup"><span data-stu-id="16781-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="16781-112">A parancs a következő parancsban a $Context változó környezetét tárolja.</span><span class="sxs-lookup"><span data-stu-id="16781-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="16781-113">A második parancs beolvassa az összes elérhető Node Agent SKU-t, amelyet a köteg támogat.</span><span class="sxs-lookup"><span data-stu-id="16781-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="16781-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16781-114">PARAMETERS</span></span>

### <span data-ttu-id="16781-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="16781-115">-BatchContext</span></span>
<span data-ttu-id="16781-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="16781-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="16781-117">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="16781-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="16781-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="16781-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="16781-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="16781-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="16781-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="16781-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="16781-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16781-121">-DefaultProfile</span></span>
<span data-ttu-id="16781-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16781-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16781-123">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="16781-123">-Filter</span></span>
<span data-ttu-id="16781-124">A OData-szűrési záradékot adja meg a Node Agent SKU-hoz.</span><span class="sxs-lookup"><span data-stu-id="16781-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="16781-125">Ha nem ad meg szűrőt, a parancsmag minden olyan csomópont-ügynököt visszaad, amelyet a köteg támogat.</span><span class="sxs-lookup"><span data-stu-id="16781-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="16781-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="16781-126">-MaxCount</span></span>
<span data-ttu-id="16781-127">Azt adja meg, hogy legfeljebb hány csomópontos SKU-t szeretne visszaadni.</span><span class="sxs-lookup"><span data-stu-id="16781-127">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="16781-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16781-128">CommonParameters</span></span>
<span data-ttu-id="16781-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16781-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16781-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16781-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16781-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16781-131">INPUTS</span></span>

### <span data-ttu-id="16781-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="16781-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="16781-133">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="16781-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="16781-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16781-134">OUTPUTS</span></span>

### <span data-ttu-id="16781-135">Microsoft.Azure.Commands.BatCH. Modellek. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="16781-135">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="16781-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16781-136">NOTES</span></span>

## <span data-ttu-id="16781-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16781-137">RELATED LINKS</span></span>

[<span data-ttu-id="16781-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="16781-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


