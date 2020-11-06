---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: d43754e1b04dadc447de3d727769902f5454f79a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498399"
---
# <span data-ttu-id="79447-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="79447-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="79447-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79447-102">SYNOPSIS</span></span>
<span data-ttu-id="79447-103">Visszavonja egy tanúsítvány sikertelen törlését.</span><span class="sxs-lookup"><span data-stu-id="79447-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79447-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79447-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79447-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="79447-105">DESCRIPTION</span></span>
<span data-ttu-id="79447-106">A **stop-AzureBatchCertificateDeletion** parancsmag lemond egy tanúsítvány sikertelen törléséről az Azure kötegfájl-szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="79447-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="79447-107">Csak akkor állíthatja le a törlést, ha a tanúsítvány a **DeleteFailed** állapotban van.</span><span class="sxs-lookup"><span data-stu-id="79447-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="79447-108">Ez a cmldet visszaállítja a tanúsítványt az **aktív** állapotra.</span><span class="sxs-lookup"><span data-stu-id="79447-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="79447-109">Példák</span><span class="sxs-lookup"><span data-stu-id="79447-109">EXAMPLES</span></span>

### <span data-ttu-id="79447-110">Példa 1: törlés megszüntetése</span><span class="sxs-lookup"><span data-stu-id="79447-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="79447-111">Ez a parancs törli a megadott ujjlenyomatot tartalmazó tanúsítvány törlését.</span><span class="sxs-lookup"><span data-stu-id="79447-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="79447-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79447-112">PARAMETERS</span></span>

### <span data-ttu-id="79447-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="79447-113">-BatchContext</span></span>
<span data-ttu-id="79447-114">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="79447-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="79447-115">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="79447-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="79447-116">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="79447-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="79447-117">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="79447-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="79447-118">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="79447-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="79447-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79447-119">-DefaultProfile</span></span>
<span data-ttu-id="79447-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79447-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79447-121">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="79447-121">-Thumbprint</span></span>
<span data-ttu-id="79447-122">Annak a tanúsítványnak az ujjlenyomatát adja vissza, amelyre az adott parancsmag visszaállítja az **aktív** állapotot.</span><span class="sxs-lookup"><span data-stu-id="79447-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="79447-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="79447-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="79447-124">Az *ujjlenyomat* -paraméter származtatása algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="79447-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="79447-125">Jelenleg az egyetlen érvényes érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="79447-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="79447-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79447-126">CommonParameters</span></span>
<span data-ttu-id="79447-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79447-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79447-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79447-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79447-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79447-129">INPUTS</span></span>

### <span data-ttu-id="79447-130">System. String</span><span class="sxs-lookup"><span data-stu-id="79447-130">System.String</span></span>

### <span data-ttu-id="79447-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="79447-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="79447-132">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79447-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="79447-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79447-133">OUTPUTS</span></span>

### <span data-ttu-id="79447-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="79447-134">System.Void</span></span>

## <span data-ttu-id="79447-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79447-135">NOTES</span></span>

## <span data-ttu-id="79447-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79447-136">RELATED LINKS</span></span>

[<span data-ttu-id="79447-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="79447-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="79447-138">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="79447-138">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="79447-139">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="79447-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


