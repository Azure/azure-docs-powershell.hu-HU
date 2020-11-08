---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: 56ec7eafcea7233697089d692b2799fa6c9b744a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013002"
---
# <span data-ttu-id="11636-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="11636-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="11636-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11636-102">SYNOPSIS</span></span>
<span data-ttu-id="11636-103">Kötegelt fiók esetén támogatott képeket kap.</span><span class="sxs-lookup"><span data-stu-id="11636-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="11636-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11636-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11636-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="11636-105">DESCRIPTION</span></span>
<span data-ttu-id="11636-106">A **Get-AzBatchSupportedImage** parancsmag az Azure-fiókokban elérhető virtuális gép képeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="11636-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="11636-107">Adja meg a fiókot a *BatchContext* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="11636-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="11636-108">Példák</span><span class="sxs-lookup"><span data-stu-id="11636-108">EXAMPLES</span></span>

### <span data-ttu-id="11636-109">1. példa: az összes elérhető támogatott kép beolvasása</span><span class="sxs-lookup"><span data-stu-id="11636-109">Example 1: Get all available supported images</span></span>

```powershell
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchSupportedImage -BatchContext $Context
BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:16.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 16.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:18.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 18.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : credativ:debian:8:latest
NodeAgentSkuId        : batch.node.debian 8
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : microsoftwindowsserver:windowsserver:2016-datacenter:latest
NodeAgentSkuId        : batch.node.windows amd64
OSType                : Windows
VerificationType      : Verified

...
```

<span data-ttu-id="11636-110">Az első parancs a **Get-AzBatchAccountKey használatával beolvassa** az előfizetéshez a hozzáférési kulcsokat tartalmazó kötegelt fiók környezetét.</span><span class="sxs-lookup"><span data-stu-id="11636-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="11636-111">A parancs a következő parancsban a $Context változó környezetét tárolja.</span><span class="sxs-lookup"><span data-stu-id="11636-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="11636-112">A második parancs az adott köteghez elérhető támogatott képeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="11636-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="11636-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11636-113">PARAMETERS</span></span>

### <span data-ttu-id="11636-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="11636-114">-BatchContext</span></span>
<span data-ttu-id="11636-115">A kötegelt szolgáltatással való interakció során használandó BatchAccountContext-példány.</span><span class="sxs-lookup"><span data-stu-id="11636-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="11636-116">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="11636-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="11636-117">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="11636-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="11636-118">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="11636-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="11636-119">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="11636-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11636-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11636-120">-DefaultProfile</span></span>
<span data-ttu-id="11636-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11636-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11636-122">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="11636-122">-Filter</span></span>
<span data-ttu-id="11636-123">A támogatott képek OData-szűrési záradékát adja meg.</span><span class="sxs-lookup"><span data-stu-id="11636-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="11636-124">Ha nem ad meg szűrőt, ez a parancsmag minden olyan képet ad eredményül, amely a kötegelt fiók által támogatott.</span><span class="sxs-lookup"><span data-stu-id="11636-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

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

### <span data-ttu-id="11636-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="11636-125">-MaxCount</span></span>
<span data-ttu-id="11636-126">A visszaadott támogatott képek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="11636-126">Specifies the maximum number of supported images to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11636-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11636-127">CommonParameters</span></span>
<span data-ttu-id="11636-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11636-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11636-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="11636-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11636-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11636-130">INPUTS</span></span>

### <span data-ttu-id="11636-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="11636-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="11636-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11636-132">OUTPUTS</span></span>

### <span data-ttu-id="11636-133">Microsoft.Azure.Commands.BatCH. Modellek. PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="11636-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="11636-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11636-134">NOTES</span></span>

## <span data-ttu-id="11636-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11636-135">RELATED LINKS</span></span>
[<span data-ttu-id="11636-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="11636-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)