---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e5d177776e288a855c35def8d45310a6f6849c27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938282"
---
# <span data-ttu-id="b60a6-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="b60a6-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="b60a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b60a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b60a6-103">Batch-fiók támogatott képeit kapja.</span><span class="sxs-lookup"><span data-stu-id="b60a6-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="b60a6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b60a6-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b60a6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b60a6-105">DESCRIPTION</span></span>
<span data-ttu-id="b60a6-106">A **Get-AzBatchSupportedImage parancsmag** támogatott virtuális gépi képeket kap, amelyek egy Azure Batch-fiókban érhetők el.</span><span class="sxs-lookup"><span data-stu-id="b60a6-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="b60a6-107">Adja meg a fiókot a *BatchContext paraméterrel.*</span><span class="sxs-lookup"><span data-stu-id="b60a6-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="b60a6-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b60a6-108">EXAMPLES</span></span>

### <span data-ttu-id="b60a6-109">1. példa: Az összes elérhető támogatott kép lekérhetők</span><span class="sxs-lookup"><span data-stu-id="b60a6-109">Example 1: Get all available supported images</span></span>

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

<span data-ttu-id="b60a6-110">Az első parancs a **Get-AzBatchAccountKey** használatával kap egy Batch-fiók környezetet, amely az előfizetés hozzáférési kulcsait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b60a6-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="b60a6-111">A parancs a következő parancsban $Context változóban tárolja a környezetét.</span><span class="sxs-lookup"><span data-stu-id="b60a6-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="b60a6-112">A második parancs az összes támogatott képet lekérhetők az egyes Batch-fiókokhoz.</span><span class="sxs-lookup"><span data-stu-id="b60a6-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="b60a6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b60a6-113">PARAMETERS</span></span>

### <span data-ttu-id="b60a6-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b60a6-114">-BatchContext</span></span>
<span data-ttu-id="b60a6-115">A Batch-szolgáltatáshoz használt BatchAccountContext példány.</span><span class="sxs-lookup"><span data-stu-id="b60a6-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="b60a6-116">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="b60a6-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="b60a6-117">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="b60a6-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="b60a6-118">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="b60a6-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="b60a6-119">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="b60a6-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b60a6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60a6-120">-DefaultProfile</span></span>
<span data-ttu-id="b60a6-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b60a6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b60a6-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="b60a6-122">-Filter</span></span>
<span data-ttu-id="b60a6-123">OData-szűrő záradékot ad meg a támogatott képekhez.</span><span class="sxs-lookup"><span data-stu-id="b60a6-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="b60a6-124">Ha nem ad meg szűrőt, ez a parancsmag a Batch-fiók által támogatott összes képet visszaadja.</span><span class="sxs-lookup"><span data-stu-id="b60a6-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

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

### <span data-ttu-id="b60a6-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b60a6-125">-MaxCount</span></span>
<span data-ttu-id="b60a6-126">Azt adja meg, hogy legfeljebb hány támogatott képet kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="b60a6-126">Specifies the maximum number of supported images to return.</span></span>

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

### <span data-ttu-id="b60a6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60a6-127">CommonParameters</span></span>
<span data-ttu-id="b60a6-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b60a6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60a6-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b60a6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60a6-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b60a6-130">INPUTS</span></span>

### <span data-ttu-id="b60a6-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b60a6-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b60a6-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b60a6-132">OUTPUTS</span></span>

### <span data-ttu-id="b60a6-133">Microsoft.Azure.Commands.Bat. Models.PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="b60a6-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="b60a6-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b60a6-134">NOTES</span></span>

## <span data-ttu-id="b60a6-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b60a6-135">RELATED LINKS</span></span>

[<span data-ttu-id="b60a6-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b60a6-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)