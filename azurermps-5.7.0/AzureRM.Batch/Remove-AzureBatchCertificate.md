---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: e62aebd6a03f7d5a162f141eae55e3df6c9a0a88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503092"
---
# <span data-ttu-id="b5e6e-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b5e6e-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="b5e6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e6e-103">Tanúsítvány törlése egy fiókból.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5e6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5e6e-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5e6e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5e6e-105">DESCRIPTION</span></span>
<span data-ttu-id="b5e6e-106">A **Remove-AzureBatchCertificate** parancsmag a megadott Azure-köteg fiókból távolítja el a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="b5e6e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b5e6e-107">EXAMPLES</span></span>

### <span data-ttu-id="b5e6e-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b5e6e-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="b5e6e-109">Ez a parancs eltávolítja a megadott ujjlenyomatot tartalmazó tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="b5e6e-110">2. példa: az összes aktív tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b5e6e-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="b5e6e-111">Ez a parancs minden olyan tanúsítványt beolvas, amely az Get-AzureBatchCertificate parancsmag használatával aktív.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="b5e6e-112">A parancs a csővezeték-kezelő segítségével továbbítja az aktív tanúsítványokat az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b5e6e-113">Az adott parancsmag eltávolítja az egyes tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="b5e6e-114">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b5e6e-115">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b5e6e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5e6e-116">PARAMETERS</span></span>

### <span data-ttu-id="b5e6e-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b5e6e-117">-BatchContext</span></span>
<span data-ttu-id="b5e6e-118">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b5e6e-119">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b5e6e-120">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b5e6e-121">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b5e6e-122">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b5e6e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e6e-123">-DefaultProfile</span></span>
<span data-ttu-id="b5e6e-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5e6e-125">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="b5e6e-125">-Thumbprint</span></span>
<span data-ttu-id="b5e6e-126">A parancsmag által törölt tanúsítvány ujjlenyomatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5e6e-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b5e6e-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b5e6e-128">Az *ujjlenyomat* -paraméter származtatása algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="b5e6e-129">Jelenleg az egyetlen érvényes érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-129">Currently, the only valid value is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5e6e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b5e6e-130">-Confirm</span></span>
<span data-ttu-id="b5e6e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e6e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5e6e-132">-WhatIf</span></span>
<span data-ttu-id="b5e6e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5e6e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5e6e-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e6e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e6e-135">CommonParameters</span></span>
<span data-ttu-id="b5e6e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5e6e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e6e-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5e6e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e6e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5e6e-138">INPUTS</span></span>

### <span data-ttu-id="b5e6e-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b5e6e-139">BatchAccountContext</span></span>
<span data-ttu-id="b5e6e-140">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b5e6e-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="b5e6e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5e6e-141">OUTPUTS</span></span>

## <span data-ttu-id="b5e6e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5e6e-142">NOTES</span></span>

## <span data-ttu-id="b5e6e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5e6e-143">RELATED LINKS</span></span>

[<span data-ttu-id="b5e6e-144">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b5e6e-144">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="b5e6e-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b5e6e-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b5e6e-146">Új – AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b5e6e-146">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="b5e6e-147">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="b5e6e-147">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="b5e6e-148">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b5e6e-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

