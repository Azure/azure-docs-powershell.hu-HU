---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478282"
---
# <span data-ttu-id="951fd-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="951fd-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="951fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="951fd-102">SYNOPSIS</span></span>
<span data-ttu-id="951fd-103">Hozzáad egy tanúsítványt a megadott Batch-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="951fd-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="951fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="951fd-104">SYNTAX</span></span>

### <span data-ttu-id="951fd-105">Fájl (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="951fd-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="951fd-106">RawData</span><span class="sxs-lookup"><span data-stu-id="951fd-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="951fd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="951fd-107">DESCRIPTION</span></span>
<span data-ttu-id="951fd-108">A **New-AzBatchCertificate** parancsmag hozzáad egy tanúsítványt a megadott Azure Batch-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="951fd-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="951fd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="951fd-109">EXAMPLES</span></span>

### <span data-ttu-id="951fd-110">1. példa: Tanúsítvány hozzáadása fájlból</span><span class="sxs-lookup"><span data-stu-id="951fd-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="951fd-111">Ez a parancs hozzáad egy tanúsítványt a megadott Batch-fiókhoz az E:\Certificates\MyCert.cer fájl használatával.</span><span class="sxs-lookup"><span data-stu-id="951fd-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="951fd-112">2. példa: Tanúsítvány hozzáadása nyers adatokból</span><span class="sxs-lookup"><span data-stu-id="951fd-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="951fd-113">Az első parancs felolvassa a MyCert.pfx nevű fájl adatait a $RawData változóba.</span><span class="sxs-lookup"><span data-stu-id="951fd-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="951fd-114">A második parancs hozzáad egy tanúsítványt a megadott Batch-fiókhoz a $RawData.</span><span class="sxs-lookup"><span data-stu-id="951fd-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="951fd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="951fd-115">PARAMETERS</span></span>

### <span data-ttu-id="951fd-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="951fd-116">-BatchContext</span></span>
<span data-ttu-id="951fd-117">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="951fd-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="951fd-118">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="951fd-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="951fd-119">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="951fd-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="951fd-120">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="951fd-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="951fd-121">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="951fd-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="951fd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="951fd-122">-DefaultProfile</span></span>
<span data-ttu-id="951fd-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="951fd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="951fd-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="951fd-124">-FilePath</span></span>
<span data-ttu-id="951fd-125">A tanúsítványfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="951fd-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="951fd-126">A tanúsítványfájlnak .cer vagy .pfx formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="951fd-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="951fd-127">-Kind</span><span class="sxs-lookup"><span data-stu-id="951fd-127">-Kind</span></span>
<span data-ttu-id="951fd-128">A létrehozni szükséges tanúsítvány fajtája.</span><span class="sxs-lookup"><span data-stu-id="951fd-128">The kind of certificate to create.</span></span> <span data-ttu-id="951fd-129">Ha ez nincs megadva, akkor a jelszó nélküli összes tanúsítvány a CER, a jelszóval pedig a PFX.</span><span class="sxs-lookup"><span data-stu-id="951fd-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951fd-130">-Password</span><span class="sxs-lookup"><span data-stu-id="951fd-130">-Password</span></span>
<span data-ttu-id="951fd-131">Megadja a tanúsítvány titkos kulcshoz való hozzáférésének jelszavát.</span><span class="sxs-lookup"><span data-stu-id="951fd-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="951fd-132">Ezt a paramétert akkor kell megadnia, ha .pfx formátumban ad meg tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="951fd-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951fd-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="951fd-133">-RawData</span></span>
<span data-ttu-id="951fd-134">A nyers tanúsítvány adatait adja meg .cer vagy .pfx formátumban.</span><span class="sxs-lookup"><span data-stu-id="951fd-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="951fd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951fd-135">CommonParameters</span></span>
<span data-ttu-id="951fd-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="951fd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951fd-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="951fd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951fd-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="951fd-138">INPUTS</span></span>

### <span data-ttu-id="951fd-139">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="951fd-139">System.Byte[]</span></span>

### <span data-ttu-id="951fd-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="951fd-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="951fd-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="951fd-141">OUTPUTS</span></span>

### <span data-ttu-id="951fd-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="951fd-142">System.Void</span></span>

## <span data-ttu-id="951fd-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="951fd-143">NOTES</span></span>

## <span data-ttu-id="951fd-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="951fd-144">RELATED LINKS</span></span>

[<span data-ttu-id="951fd-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="951fd-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="951fd-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="951fd-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="951fd-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="951fd-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="951fd-148">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="951fd-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
