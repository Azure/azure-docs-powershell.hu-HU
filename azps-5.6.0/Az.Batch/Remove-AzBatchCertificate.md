---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 62858f37a7444e052c3d0a192a346a2284f232c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928706"
---
# <span data-ttu-id="7c74f-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="7c74f-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="7c74f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c74f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c74f-103">Törli a tanúsítványt egy fiókból.</span><span class="sxs-lookup"><span data-stu-id="7c74f-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="7c74f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7c74f-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c74f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7c74f-105">DESCRIPTION</span></span>
<span data-ttu-id="7c74f-106">A **Remove-AzBatchCertificate** parancsmag eltávolít egy tanúsítványt a megadott Azure Batch-fiókból.</span><span class="sxs-lookup"><span data-stu-id="7c74f-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="7c74f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7c74f-107">EXAMPLES</span></span>

### <span data-ttu-id="7c74f-108">1. példa: Tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7c74f-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="7c74f-109">Ez a parancs eltávolítja a megadott thumbprint tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="7c74f-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="7c74f-110">2. példa:Az összes aktív tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7c74f-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="7c74f-111">Ez a parancs az összes olyan tanúsítványt beveszi, amely aktív a Get-AzBatchCertificate parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="7c74f-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="7c74f-112">A parancs a folyamat műveleti operátorával átadja az aktív tanúsítványokat az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="7c74f-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7c74f-113">Ez a parancsmag eltávolítja az egyes tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="7c74f-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="7c74f-114">A parancs a Force *paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c74f-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7c74f-115">Ezért a parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c74f-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7c74f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c74f-116">PARAMETERS</span></span>

### <span data-ttu-id="7c74f-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7c74f-117">-BatchContext</span></span>
<span data-ttu-id="7c74f-118">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="7c74f-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7c74f-119">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="7c74f-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7c74f-120">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="7c74f-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7c74f-121">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="7c74f-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7c74f-122">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="7c74f-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7c74f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c74f-123">-DefaultProfile</span></span>
<span data-ttu-id="7c74f-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c74f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c74f-125">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="7c74f-125">-Thumbprint</span></span>
<span data-ttu-id="7c74f-126">A parancsmag által törölt tanúsítvány thumbprint-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c74f-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="7c74f-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="7c74f-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="7c74f-128">A Thumbprint paraméter származtatására *használt algoritmus.*</span><span class="sxs-lookup"><span data-stu-id="7c74f-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="7c74f-129">Jelenleg az egyetlen érvényes érték az sha1.</span><span class="sxs-lookup"><span data-stu-id="7c74f-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="7c74f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c74f-130">-Confirm</span></span>
<span data-ttu-id="7c74f-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7c74f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c74f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c74f-132">-WhatIf</span></span>
<span data-ttu-id="7c74f-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7c74f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c74f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c74f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c74f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c74f-135">CommonParameters</span></span>
<span data-ttu-id="7c74f-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c74f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c74f-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c74f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c74f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c74f-138">INPUTS</span></span>

### <span data-ttu-id="7c74f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7c74f-139">System.String</span></span>

### <span data-ttu-id="7c74f-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7c74f-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7c74f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c74f-141">OUTPUTS</span></span>

### <span data-ttu-id="7c74f-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="7c74f-142">System.Void</span></span>

## <span data-ttu-id="7c74f-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7c74f-143">NOTES</span></span>

## <span data-ttu-id="7c74f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c74f-144">RELATED LINKS</span></span>

[<span data-ttu-id="7c74f-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="7c74f-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="7c74f-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7c74f-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7c74f-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="7c74f-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="7c74f-148">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="7c74f-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="7c74f-149">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="7c74f-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
