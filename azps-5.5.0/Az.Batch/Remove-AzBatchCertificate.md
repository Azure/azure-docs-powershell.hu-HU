---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 2f751a6efcf4b798c69bb0dfd9ecd38c33a65d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162459"
---
# <span data-ttu-id="49c6c-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="49c6c-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="49c6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="49c6c-103">Törli a tanúsítványt egy fiókból.</span><span class="sxs-lookup"><span data-stu-id="49c6c-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="49c6c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49c6c-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49c6c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49c6c-105">DESCRIPTION</span></span>
<span data-ttu-id="49c6c-106">A **Remove-AzBatchCertificate** parancsmag eltávolít egy tanúsítványt a megadott Azure Batch-fiókból.</span><span class="sxs-lookup"><span data-stu-id="49c6c-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="49c6c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49c6c-107">EXAMPLES</span></span>

### <span data-ttu-id="49c6c-108">1. példa: Tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="49c6c-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="49c6c-109">Ez a parancs eltávolítja a tanúsítványt, amely a megadott thumbprint-et rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="49c6c-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="49c6c-110">2. példa:Az összes aktív tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="49c6c-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="49c6c-111">Ez a parancs az összes olyan tanúsítványt beveszi, amely aktív a Get-AzBatchCertificate parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="49c6c-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="49c6c-112">A parancs átadja az aktív tanúsítványokat az aktuális parancsmagnak a folyamat műveleti operátorával.</span><span class="sxs-lookup"><span data-stu-id="49c6c-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="49c6c-113">Ez a parancsmag minden tanúsítványt eltávolít.</span><span class="sxs-lookup"><span data-stu-id="49c6c-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="49c6c-114">A parancs a Force *paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="49c6c-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="49c6c-115">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49c6c-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="49c6c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49c6c-116">PARAMETERS</span></span>

### <span data-ttu-id="49c6c-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="49c6c-117">-BatchContext</span></span>
<span data-ttu-id="49c6c-118">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="49c6c-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="49c6c-119">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="49c6c-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="49c6c-120">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot, és töltse ki a hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="49c6c-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="49c6c-121">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="49c6c-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="49c6c-122">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="49c6c-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="49c6c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c6c-123">-DefaultProfile</span></span>
<span data-ttu-id="49c6c-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49c6c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49c6c-125">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="49c6c-125">-Thumbprint</span></span>
<span data-ttu-id="49c6c-126">Annak a tanúsítványnak a thumbprint-ját adja meg, amelyből a parancsmag töröl.</span><span class="sxs-lookup"><span data-stu-id="49c6c-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="49c6c-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="49c6c-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="49c6c-128">A Thumbprint paraméter *levezető algoritmusa.*</span><span class="sxs-lookup"><span data-stu-id="49c6c-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="49c6c-129">Jelenleg az egyetlen érvényes érték az sha1.</span><span class="sxs-lookup"><span data-stu-id="49c6c-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="49c6c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49c6c-130">-Confirm</span></span>
<span data-ttu-id="49c6c-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="49c6c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49c6c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49c6c-132">-WhatIf</span></span>
<span data-ttu-id="49c6c-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="49c6c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49c6c-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49c6c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49c6c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c6c-135">CommonParameters</span></span>
<span data-ttu-id="49c6c-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c6c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c6c-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49c6c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c6c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49c6c-138">INPUTS</span></span>

### <span data-ttu-id="49c6c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="49c6c-139">System.String</span></span>

### <span data-ttu-id="49c6c-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="49c6c-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="49c6c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49c6c-141">OUTPUTS</span></span>

### <span data-ttu-id="49c6c-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="49c6c-142">System.Void</span></span>

## <span data-ttu-id="49c6c-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49c6c-143">NOTES</span></span>

## <span data-ttu-id="49c6c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49c6c-144">RELATED LINKS</span></span>

[<span data-ttu-id="49c6c-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="49c6c-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="49c6c-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="49c6c-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="49c6c-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="49c6c-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="49c6c-148">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="49c6c-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="49c6c-149">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="49c6c-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
