---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 124000fdf11b3fa5b90253fc3b9a75c040725ba8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499220"
---
# <span data-ttu-id="e44fb-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="e44fb-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="e44fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e44fb-102">SYNOPSIS</span></span>
<span data-ttu-id="e44fb-103">Letiltja a készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="e44fb-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e44fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e44fb-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e44fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e44fb-105">DESCRIPTION</span></span>
<span data-ttu-id="e44fb-106">A **disable-AzureBatchAutoScale** parancsmag letiltja a megadott készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="e44fb-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="e44fb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e44fb-107">EXAMPLES</span></span>

### <span data-ttu-id="e44fb-108">1. példa: a készlet automatikus méretezésének letiltása</span><span class="sxs-lookup"><span data-stu-id="e44fb-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="e44fb-109">Ez a parancs letiltja az automatikus méretezést a MyPool nevű alkalmazáskészlethez.</span><span class="sxs-lookup"><span data-stu-id="e44fb-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="e44fb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e44fb-110">PARAMETERS</span></span>

### <span data-ttu-id="e44fb-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e44fb-111">-BatchContext</span></span>
<span data-ttu-id="e44fb-112">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="e44fb-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e44fb-113">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e44fb-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="e44fb-114">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e44fb-114">-Id</span></span>
<span data-ttu-id="e44fb-115">A készlet objektum-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e44fb-115">Specifies the object ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e44fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44fb-116">-DefaultProfile</span></span>
<span data-ttu-id="e44fb-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e44fb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e44fb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44fb-118">CommonParameters</span></span>
<span data-ttu-id="e44fb-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e44fb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44fb-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e44fb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44fb-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e44fb-121">INPUTS</span></span>

### <span data-ttu-id="e44fb-122">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e44fb-122">BatchAccountContext</span></span>
<span data-ttu-id="e44fb-123">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e44fb-123">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="e44fb-124">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="e44fb-124">String</span></span>
<span data-ttu-id="e44fb-125">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="e44fb-125">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e44fb-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e44fb-126">OUTPUTS</span></span>

## <span data-ttu-id="e44fb-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e44fb-127">NOTES</span></span>

## <span data-ttu-id="e44fb-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e44fb-128">RELATED LINKS</span></span>

[<span data-ttu-id="e44fb-129">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="e44fb-129">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="e44fb-130">Teszt-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="e44fb-130">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="e44fb-131">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e44fb-131">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


