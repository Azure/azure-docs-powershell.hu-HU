---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 8eef0043bdacc658779bdb2fd0a1241975a6284b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847794"
---
# <span data-ttu-id="31108-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="31108-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="31108-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31108-102">SYNOPSIS</span></span>
<span data-ttu-id="31108-103">Tanúsítvány törlése egy fiókból.</span><span class="sxs-lookup"><span data-stu-id="31108-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="31108-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31108-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31108-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="31108-105">DESCRIPTION</span></span>
<span data-ttu-id="31108-106">A **Remove-AzBatchCertificate** parancsmag a megadott Azure-köteg fiókból távolítja el a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="31108-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="31108-107">Példák</span><span class="sxs-lookup"><span data-stu-id="31108-107">EXAMPLES</span></span>

### <span data-ttu-id="31108-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="31108-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="31108-109">Ez a parancs eltávolítja a megadott ujjlenyomatot tartalmazó tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="31108-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="31108-110">2. példa: az összes aktív tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="31108-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="31108-111">Ez a parancs minden olyan tanúsítványt beolvas, amely az Get-AzBatchCertificate parancsmag használatával aktív.</span><span class="sxs-lookup"><span data-stu-id="31108-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="31108-112">A parancs a csővezeték-kezelő segítségével továbbítja az aktív tanúsítványokat az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="31108-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="31108-113">Az adott parancsmag eltávolítja az egyes tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="31108-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="31108-114">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="31108-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="31108-115">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="31108-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="31108-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31108-116">PARAMETERS</span></span>

### <span data-ttu-id="31108-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="31108-117">-BatchContext</span></span>
<span data-ttu-id="31108-118">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="31108-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="31108-119">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="31108-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="31108-120">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="31108-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="31108-121">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="31108-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="31108-122">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="31108-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="31108-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31108-123">-DefaultProfile</span></span>
<span data-ttu-id="31108-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31108-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31108-125">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="31108-125">-Thumbprint</span></span>
<span data-ttu-id="31108-126">A parancsmag által törölt tanúsítvány ujjlenyomatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="31108-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="31108-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="31108-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="31108-128">Az *ujjlenyomat* -paraméter származtatása algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="31108-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="31108-129">Jelenleg az egyetlen érvényes érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="31108-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="31108-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="31108-130">-Confirm</span></span>
<span data-ttu-id="31108-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="31108-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31108-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31108-132">-WhatIf</span></span>
<span data-ttu-id="31108-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="31108-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31108-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31108-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31108-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31108-135">CommonParameters</span></span>
<span data-ttu-id="31108-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31108-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31108-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31108-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31108-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31108-138">INPUTS</span></span>

### <span data-ttu-id="31108-139">System. String</span><span class="sxs-lookup"><span data-stu-id="31108-139">System.String</span></span>

### <span data-ttu-id="31108-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="31108-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="31108-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31108-141">OUTPUTS</span></span>

### <span data-ttu-id="31108-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="31108-142">System.Void</span></span>

## <span data-ttu-id="31108-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31108-143">NOTES</span></span>

## <span data-ttu-id="31108-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31108-144">RELATED LINKS</span></span>

[<span data-ttu-id="31108-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="31108-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="31108-146">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="31108-146">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="31108-147">Új – AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="31108-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="31108-148">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="31108-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="31108-149">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="31108-149">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


