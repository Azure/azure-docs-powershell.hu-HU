---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 53c4f4c24e0a5b1c868facd0fed8d3754fda7a41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352218"
---
# <span data-ttu-id="82fd0-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="82fd0-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="82fd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="82fd0-103">Visszavonja egy tanúsítvány sikertelen törlését.</span><span class="sxs-lookup"><span data-stu-id="82fd0-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="82fd0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="82fd0-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82fd0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="82fd0-105">DESCRIPTION</span></span>
<span data-ttu-id="82fd0-106">A **Stop-AzBatchCertificateDeletion** parancsmag megszakítja egy tanúsítvány sikertelen törlését az Azure Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="82fd0-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="82fd0-107">A törlést csak akkor állíthatja le, ha a tanúsítvány **DeleteFailed állapotban** van.</span><span class="sxs-lookup"><span data-stu-id="82fd0-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="82fd0-108">Ez a parancsmag visszaállítja a tanúsítványt aktív **állapotba.**</span><span class="sxs-lookup"><span data-stu-id="82fd0-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="82fd0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="82fd0-109">EXAMPLES</span></span>

### <span data-ttu-id="82fd0-110">1. példa: Törlés megszakítása</span><span class="sxs-lookup"><span data-stu-id="82fd0-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="82fd0-111">Ez a parancs megszakítja a megadott thumbprint tanúsítvány törlését.</span><span class="sxs-lookup"><span data-stu-id="82fd0-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="82fd0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82fd0-112">PARAMETERS</span></span>

### <span data-ttu-id="82fd0-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="82fd0-113">-BatchContext</span></span>
<span data-ttu-id="82fd0-114">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="82fd0-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="82fd0-115">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="82fd0-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="82fd0-116">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="82fd0-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="82fd0-117">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="82fd0-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="82fd0-118">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="82fd0-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="82fd0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82fd0-119">-DefaultProfile</span></span>
<span data-ttu-id="82fd0-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82fd0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82fd0-121">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="82fd0-121">-Thumbprint</span></span>
<span data-ttu-id="82fd0-122">Annak a tanúsítványnak a thumbprint-ját adja meg, amely a parancsmag aktív állapotába **áll** vissza.</span><span class="sxs-lookup"><span data-stu-id="82fd0-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="82fd0-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="82fd0-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="82fd0-124">A Thumbprint paraméter származtatására *használt algoritmus.*</span><span class="sxs-lookup"><span data-stu-id="82fd0-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="82fd0-125">Jelenleg az egyetlen érvényes érték az sha1.</span><span class="sxs-lookup"><span data-stu-id="82fd0-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="82fd0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82fd0-126">CommonParameters</span></span>
<span data-ttu-id="82fd0-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82fd0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82fd0-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82fd0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82fd0-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82fd0-129">INPUTS</span></span>

### <span data-ttu-id="82fd0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="82fd0-130">System.String</span></span>

### <span data-ttu-id="82fd0-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="82fd0-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="82fd0-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82fd0-132">OUTPUTS</span></span>

### <span data-ttu-id="82fd0-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="82fd0-133">System.Void</span></span>

## <span data-ttu-id="82fd0-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="82fd0-134">NOTES</span></span>

## <span data-ttu-id="82fd0-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82fd0-135">RELATED LINKS</span></span>

[<span data-ttu-id="82fd0-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="82fd0-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="82fd0-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="82fd0-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="82fd0-138">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="82fd0-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
