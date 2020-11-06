---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a53e72cd31d3ca43cf5c9a4e6a66de4bc2bd59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505803"
---
# <span data-ttu-id="d926f-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="d926f-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="d926f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d926f-102">SYNOPSIS</span></span>
<span data-ttu-id="d926f-103">Letiltja a készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="d926f-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d926f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d926f-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d926f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d926f-105">DESCRIPTION</span></span>
<span data-ttu-id="d926f-106">A **disable-AzureBatchAutoScale** parancsmag letiltja a megadott készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="d926f-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="d926f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d926f-107">EXAMPLES</span></span>

### <span data-ttu-id="d926f-108">1. példa: a készlet automatikus méretezésének letiltása</span><span class="sxs-lookup"><span data-stu-id="d926f-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="d926f-109">Ez a parancs letiltja az automatikus méretezést a MyPool nevű alkalmazáskészlethez.</span><span class="sxs-lookup"><span data-stu-id="d926f-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="d926f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d926f-110">PARAMETERS</span></span>

### <span data-ttu-id="d926f-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d926f-111">-BatchContext</span></span>
<span data-ttu-id="d926f-112">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="d926f-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d926f-113">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="d926f-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d926f-114">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="d926f-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d926f-115">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="d926f-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d926f-116">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="d926f-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d926f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d926f-117">-DefaultProfile</span></span>
<span data-ttu-id="d926f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d926f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d926f-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d926f-119">-Id</span></span>
<span data-ttu-id="d926f-120">A készlet objektum-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d926f-120">Specifies the object ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d926f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d926f-121">CommonParameters</span></span>
<span data-ttu-id="d926f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d926f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d926f-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d926f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d926f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d926f-124">INPUTS</span></span>

### <span data-ttu-id="d926f-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d926f-125">BatchAccountContext</span></span>
<span data-ttu-id="d926f-126">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d926f-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d926f-127">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="d926f-127">String</span></span>
<span data-ttu-id="d926f-128">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="d926f-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d926f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d926f-129">OUTPUTS</span></span>

## <span data-ttu-id="d926f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d926f-130">NOTES</span></span>

## <span data-ttu-id="d926f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d926f-131">RELATED LINKS</span></span>

[<span data-ttu-id="d926f-132">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="d926f-132">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="d926f-133">Teszt-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="d926f-133">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="d926f-134">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d926f-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


