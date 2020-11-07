---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: d567c176580cba0659d6c88c919ffa34cad393ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680776"
---
# <span data-ttu-id="21eda-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="21eda-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="21eda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21eda-102">SYNOPSIS</span></span>
<span data-ttu-id="21eda-103">Tanúsítvány felvétele a megadott köteg fiókba.</span><span class="sxs-lookup"><span data-stu-id="21eda-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21eda-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21eda-104">SYNTAX</span></span>

### <span data-ttu-id="21eda-105">Fájl (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21eda-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21eda-106">RawData</span><span class="sxs-lookup"><span data-stu-id="21eda-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21eda-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="21eda-107">DESCRIPTION</span></span>
<span data-ttu-id="21eda-108">A **New-AzureBatchCertificate** parancsmag hozzáad egy tanúsítványt a megadott Azure-köteg fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="21eda-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="21eda-109">Példák</span><span class="sxs-lookup"><span data-stu-id="21eda-109">EXAMPLES</span></span>

### <span data-ttu-id="21eda-110">1. példa: tanúsítvány hozzáadása fájlból</span><span class="sxs-lookup"><span data-stu-id="21eda-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="21eda-111">Ez a parancs egy tanúsítványt ad a megadott köteg fiókhoz a fájl E:\Certificates\MyCert.cer. használatával.</span><span class="sxs-lookup"><span data-stu-id="21eda-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="21eda-112">2. példa: tanúsítvány felvétele nyers adatforrásból</span><span class="sxs-lookup"><span data-stu-id="21eda-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="21eda-113">Az első parancs a MyCert. pfx fájlból az $RawData változóba olvassa be az adatot.</span><span class="sxs-lookup"><span data-stu-id="21eda-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="21eda-114">A második parancs a $RawData-ban tárolt nyers adatforrások segítségével felvesz egy tanúsítványt a megadott köteg-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="21eda-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="21eda-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21eda-115">PARAMETERS</span></span>

### <span data-ttu-id="21eda-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="21eda-116">-BatchContext</span></span>
<span data-ttu-id="21eda-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="21eda-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="21eda-118">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="21eda-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="21eda-119">-FilePath</span><span class="sxs-lookup"><span data-stu-id="21eda-119">-FilePath</span></span>
<span data-ttu-id="21eda-120">A tanúsítványfájl elérési útjának elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="21eda-120">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="21eda-121">A tanúsítványfájl. cer vagy. pfx formátumban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="21eda-121">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21eda-122">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="21eda-122">-Password</span></span>
<span data-ttu-id="21eda-123">A tanúsítvány titkos kulcsának eléréséhez használt jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="21eda-123">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="21eda-124">Ezt a paramétert akkor kell megadnia, ha a. pfx formátumú tanúsítványt ad meg.</span><span class="sxs-lookup"><span data-stu-id="21eda-124">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21eda-125">-RawData</span><span class="sxs-lookup"><span data-stu-id="21eda-125">-RawData</span></span>
<span data-ttu-id="21eda-126">A nyers hitelességi tanúsítványra vonatkozó adatot. cer vagy. pfx formátumban adja meg.</span><span class="sxs-lookup"><span data-stu-id="21eda-126">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21eda-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21eda-127">-DefaultProfile</span></span>
<span data-ttu-id="21eda-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21eda-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21eda-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21eda-129">CommonParameters</span></span>
<span data-ttu-id="21eda-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21eda-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21eda-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21eda-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21eda-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21eda-132">INPUTS</span></span>

### <span data-ttu-id="21eda-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="21eda-133">BatchAccountContext</span></span>
<span data-ttu-id="21eda-134">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="21eda-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="21eda-135">Byte []</span><span class="sxs-lookup"><span data-stu-id="21eda-135">Byte[]</span></span>
<span data-ttu-id="21eda-136">A ' RawData ' paraméter a csővezetéken lévő "byte []" típusú értéket fogadja el.</span><span class="sxs-lookup"><span data-stu-id="21eda-136">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="21eda-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21eda-137">OUTPUTS</span></span>

## <span data-ttu-id="21eda-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21eda-138">NOTES</span></span>

## <span data-ttu-id="21eda-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21eda-139">RELATED LINKS</span></span>

[<span data-ttu-id="21eda-140">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="21eda-140">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="21eda-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="21eda-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="21eda-142">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="21eda-142">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="21eda-143">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="21eda-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


