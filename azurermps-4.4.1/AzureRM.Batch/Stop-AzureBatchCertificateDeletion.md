---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 820e94b75c19d49f4e49ee8419f7807a839f925b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499199"
---
# <span data-ttu-id="b4b62-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="b4b62-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="b4b62-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4b62-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b62-103">Visszavonja egy tanúsítvány sikertelen törlését.</span><span class="sxs-lookup"><span data-stu-id="b4b62-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4b62-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4b62-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4b62-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4b62-105">DESCRIPTION</span></span>
<span data-ttu-id="b4b62-106">A **stop-AzureBatchCertificateDeletion** parancsmag lemond egy tanúsítvány sikertelen törléséről az Azure kötegfájl-szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="b4b62-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="b4b62-107">Csak akkor állíthatja le a törlést, ha a tanúsítvány a **DeleteFailed** állapotban van.</span><span class="sxs-lookup"><span data-stu-id="b4b62-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="b4b62-108">Ez a cmldet visszaállítja a tanúsítványt az **aktív** állapotra.</span><span class="sxs-lookup"><span data-stu-id="b4b62-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="b4b62-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b4b62-109">EXAMPLES</span></span>

### <span data-ttu-id="b4b62-110">Példa 1: törlés megszüntetése</span><span class="sxs-lookup"><span data-stu-id="b4b62-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="b4b62-111">Ez a parancs törli a megadott ujjlenyomatot tartalmazó tanúsítvány törlését.</span><span class="sxs-lookup"><span data-stu-id="b4b62-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="b4b62-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4b62-112">PARAMETERS</span></span>

### <span data-ttu-id="b4b62-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b4b62-113">-BatchContext</span></span>
<span data-ttu-id="b4b62-114">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="b4b62-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b4b62-115">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b4b62-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b4b62-116">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="b4b62-116">-Thumbprint</span></span>
<span data-ttu-id="b4b62-117">Annak a tanúsítványnak az ujjlenyomatát adja vissza, amelyre az adott parancsmag visszaállítja az **aktív** állapotot.</span><span class="sxs-lookup"><span data-stu-id="b4b62-117">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b62-118">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b4b62-118">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b4b62-119">Az *ujjlenyomat* -paraméter származtatása algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4b62-119">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="b4b62-120">Jelenleg az egyetlen érvényes érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="b4b62-120">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b62-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b62-121">-DefaultProfile</span></span>
<span data-ttu-id="b4b62-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4b62-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4b62-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b62-123">CommonParameters</span></span>
<span data-ttu-id="b4b62-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4b62-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b62-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4b62-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b62-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4b62-126">INPUTS</span></span>

### <span data-ttu-id="b4b62-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b4b62-127">BatchAccountContext</span></span>
<span data-ttu-id="b4b62-128">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b4b62-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="b4b62-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4b62-129">OUTPUTS</span></span>

## <span data-ttu-id="b4b62-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4b62-130">NOTES</span></span>

## <span data-ttu-id="b4b62-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4b62-131">RELATED LINKS</span></span>

[<span data-ttu-id="b4b62-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b4b62-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b4b62-133">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b4b62-133">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="b4b62-134">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b4b62-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


