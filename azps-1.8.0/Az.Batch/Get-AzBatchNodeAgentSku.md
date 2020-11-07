---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
ms.openlocfilehash: 8f7228a540456e76e4f7a22d70d00969a9ef568c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93671884"
---
# <span data-ttu-id="b32fb-101">Get-AzBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="b32fb-101">Get-AzBatchNodeAgentSku</span></span>

## <span data-ttu-id="b32fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b32fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b32fb-103">Köteg-csomópont ügynöki SKU-t kap egy köteg fiókban.</span><span class="sxs-lookup"><span data-stu-id="b32fb-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

## <span data-ttu-id="b32fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b32fb-104">SYNTAX</span></span>

```
Get-AzBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b32fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b32fb-105">DESCRIPTION</span></span>
<span data-ttu-id="b32fb-106">A **Get-AzBatchNodeAgentSku** parancsmag az Azure-alapú köteg fiókokban elérhető, csomópont-ügynököt tartalmazó SKU-t kapja.</span><span class="sxs-lookup"><span data-stu-id="b32fb-106">The **Get-AzBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="b32fb-107">Adja meg a fiókot a *BatchContext* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="b32fb-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="b32fb-108">Szűkítheti a keresést olyan SKU-ra, amely megfelel egy Open Data Protocol (OData) szűrőnek.</span><span class="sxs-lookup"><span data-stu-id="b32fb-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="b32fb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b32fb-109">EXAMPLES</span></span>

### <span data-ttu-id="b32fb-110">1. példa: az összes elérhető csomópont ügynöki SKU beszerzése</span><span class="sxs-lookup"><span data-stu-id="b32fb-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="b32fb-111">Az első parancs a **Get-AzBatchAccountKeys használatával beolvassa** az előfizetéshez a hozzáférési kulcsokat tartalmazó kötegelt fiók környezetét.</span><span class="sxs-lookup"><span data-stu-id="b32fb-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="b32fb-112">A parancs a következő parancsban a $Context változó környezetét tárolja.</span><span class="sxs-lookup"><span data-stu-id="b32fb-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="b32fb-113">A második parancs beolvassa az összes elérhető Node Agent SKU-t, amelyet a köteg támogat.</span><span class="sxs-lookup"><span data-stu-id="b32fb-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="b32fb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b32fb-114">PARAMETERS</span></span>

### <span data-ttu-id="b32fb-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b32fb-115">-BatchContext</span></span>
<span data-ttu-id="b32fb-116">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="b32fb-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b32fb-117">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="b32fb-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b32fb-118">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="b32fb-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b32fb-119">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="b32fb-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b32fb-120">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="b32fb-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b32fb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32fb-121">-DefaultProfile</span></span>
<span data-ttu-id="b32fb-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b32fb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b32fb-123">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="b32fb-123">-Filter</span></span>
<span data-ttu-id="b32fb-124">A OData-szűrési záradékot adja meg a Node Agent SKU-hoz.</span><span class="sxs-lookup"><span data-stu-id="b32fb-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="b32fb-125">Ha nem ad meg szűrőt, a parancsmag minden olyan csomópont-ügynököt visszaad, amelyet a köteg támogat.</span><span class="sxs-lookup"><span data-stu-id="b32fb-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="b32fb-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b32fb-126">-MaxCount</span></span>
<span data-ttu-id="b32fb-127">Azt adja meg, hogy legfeljebb hány csomópontos SKU-t szeretne visszaadni.</span><span class="sxs-lookup"><span data-stu-id="b32fb-127">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="b32fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32fb-128">CommonParameters</span></span>
<span data-ttu-id="b32fb-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b32fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32fb-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b32fb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32fb-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b32fb-131">INPUTS</span></span>

### <span data-ttu-id="b32fb-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b32fb-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b32fb-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b32fb-133">OUTPUTS</span></span>

### <span data-ttu-id="b32fb-134">Microsoft.Azure.Commands.BatCH. Modellek. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="b32fb-134">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="b32fb-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b32fb-135">NOTES</span></span>

## <span data-ttu-id="b32fb-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b32fb-136">RELATED LINKS</span></span>

[<span data-ttu-id="b32fb-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b32fb-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


