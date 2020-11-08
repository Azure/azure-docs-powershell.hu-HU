---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 53c4f4c24e0a5b1c868facd0fed8d3754fda7a41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025770"
---
# <span data-ttu-id="31d20-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="31d20-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="31d20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31d20-102">SYNOPSIS</span></span>
<span data-ttu-id="31d20-103">Visszavonja egy tanúsítvány sikertelen törlését.</span><span class="sxs-lookup"><span data-stu-id="31d20-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="31d20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31d20-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31d20-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="31d20-105">DESCRIPTION</span></span>
<span data-ttu-id="31d20-106">A **stop-AzBatchCertificateDeletion** parancsmag lemond egy tanúsítvány sikertelen törléséről az Azure kötegfájl-szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="31d20-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="31d20-107">Csak akkor állíthatja le a törlést, ha a tanúsítvány a **DeleteFailed** állapotban van.</span><span class="sxs-lookup"><span data-stu-id="31d20-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="31d20-108">Ez a parancsmag visszaállítja a tanúsítványt az **aktív** állapotra.</span><span class="sxs-lookup"><span data-stu-id="31d20-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="31d20-109">Példák</span><span class="sxs-lookup"><span data-stu-id="31d20-109">EXAMPLES</span></span>

### <span data-ttu-id="31d20-110">Példa 1: törlés megszüntetése</span><span class="sxs-lookup"><span data-stu-id="31d20-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="31d20-111">Ez a parancs törli a megadott ujjlenyomatot tartalmazó tanúsítvány törlését.</span><span class="sxs-lookup"><span data-stu-id="31d20-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="31d20-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31d20-112">PARAMETERS</span></span>

### <span data-ttu-id="31d20-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="31d20-113">-BatchContext</span></span>
<span data-ttu-id="31d20-114">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="31d20-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="31d20-115">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="31d20-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="31d20-116">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="31d20-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="31d20-117">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="31d20-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="31d20-118">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="31d20-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="31d20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d20-119">-DefaultProfile</span></span>
<span data-ttu-id="31d20-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31d20-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31d20-121">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="31d20-121">-Thumbprint</span></span>
<span data-ttu-id="31d20-122">Annak a tanúsítványnak az ujjlenyomatát adja vissza, amelyre az adott parancsmag visszaállítja az **aktív** állapotot.</span><span class="sxs-lookup"><span data-stu-id="31d20-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="31d20-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="31d20-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="31d20-124">Az *ujjlenyomat* -paraméter származtatása algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="31d20-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="31d20-125">Jelenleg az egyetlen érvényes érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="31d20-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="31d20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d20-126">CommonParameters</span></span>
<span data-ttu-id="31d20-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31d20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d20-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="31d20-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d20-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31d20-129">INPUTS</span></span>

### <span data-ttu-id="31d20-130">System. String</span><span class="sxs-lookup"><span data-stu-id="31d20-130">System.String</span></span>

### <span data-ttu-id="31d20-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="31d20-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="31d20-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31d20-132">OUTPUTS</span></span>

### <span data-ttu-id="31d20-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="31d20-133">System.Void</span></span>

## <span data-ttu-id="31d20-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31d20-134">NOTES</span></span>

## <span data-ttu-id="31d20-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31d20-135">RELATED LINKS</span></span>

[<span data-ttu-id="31d20-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="31d20-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="31d20-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="31d20-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="31d20-138">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="31d20-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
