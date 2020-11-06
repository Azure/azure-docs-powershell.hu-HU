---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: 304d64e2eaff4ae1488bdde12991d22834022e93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505543"
---
# <span data-ttu-id="0d590-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="0d590-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="0d590-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d590-102">SYNOPSIS</span></span>
<span data-ttu-id="0d590-103">Tanúsítvány felvétele a megadott köteg fiókba.</span><span class="sxs-lookup"><span data-stu-id="0d590-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d590-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d590-104">SYNTAX</span></span>

### <span data-ttu-id="0d590-105">Fájl (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d590-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d590-106">RawData</span><span class="sxs-lookup"><span data-stu-id="0d590-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d590-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d590-107">DESCRIPTION</span></span>
<span data-ttu-id="0d590-108">A **New-AzureBatchCertificate** parancsmag hozzáad egy tanúsítványt a megadott Azure-köteg fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="0d590-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="0d590-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0d590-109">EXAMPLES</span></span>

### <span data-ttu-id="0d590-110">1. példa: tanúsítvány hozzáadása fájlból</span><span class="sxs-lookup"><span data-stu-id="0d590-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="0d590-111">Ez a parancs egy tanúsítványt ad a megadott köteg fiókhoz a fájl E:\Certificates\MyCert.cer. használatával.</span><span class="sxs-lookup"><span data-stu-id="0d590-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="0d590-112">2. példa: tanúsítvány felvétele nyers adatforrásból</span><span class="sxs-lookup"><span data-stu-id="0d590-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="0d590-113">Az első parancs a MyCert. pfx fájlból az $RawData változóba olvassa be az adatot.</span><span class="sxs-lookup"><span data-stu-id="0d590-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="0d590-114">A második parancs a $RawData-ban tárolt nyers adatforrások segítségével felvesz egy tanúsítványt a megadott köteg-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="0d590-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="0d590-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d590-115">PARAMETERS</span></span>

### <span data-ttu-id="0d590-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0d590-116">-BatchContext</span></span>
<span data-ttu-id="0d590-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="0d590-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0d590-118">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="0d590-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0d590-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="0d590-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0d590-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="0d590-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0d590-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="0d590-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0d590-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d590-122">-DefaultProfile</span></span>
<span data-ttu-id="0d590-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d590-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d590-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="0d590-124">-FilePath</span></span>
<span data-ttu-id="0d590-125">A tanúsítványfájl elérési útjának elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d590-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="0d590-126">A tanúsítványfájl. cer vagy. pfx formátumban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="0d590-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d590-127">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="0d590-127">-Password</span></span>
<span data-ttu-id="0d590-128">A tanúsítvány titkos kulcsának eléréséhez használt jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d590-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="0d590-129">Ezt a paramétert akkor kell megadnia, ha a. pfx formátumú tanúsítványt ad meg.</span><span class="sxs-lookup"><span data-stu-id="0d590-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d590-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="0d590-130">-RawData</span></span>
<span data-ttu-id="0d590-131">A nyers hitelességi tanúsítványra vonatkozó adatot. cer vagy. pfx formátumban adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d590-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d590-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d590-132">CommonParameters</span></span>
<span data-ttu-id="0d590-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d590-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d590-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d590-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d590-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d590-135">INPUTS</span></span>

### <span data-ttu-id="0d590-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0d590-136">BatchAccountContext</span></span>
<span data-ttu-id="0d590-137">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0d590-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0d590-138">Byte []</span><span class="sxs-lookup"><span data-stu-id="0d590-138">Byte[]</span></span>
<span data-ttu-id="0d590-139">A ' RawData ' paraméter a csővezetéken lévő "byte []" típusú értéket fogadja el.</span><span class="sxs-lookup"><span data-stu-id="0d590-139">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="0d590-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d590-140">OUTPUTS</span></span>

## <span data-ttu-id="0d590-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d590-141">NOTES</span></span>

## <span data-ttu-id="0d590-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d590-142">RELATED LINKS</span></span>

[<span data-ttu-id="0d590-143">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="0d590-143">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="0d590-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0d590-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0d590-145">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="0d590-145">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="0d590-146">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0d590-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


