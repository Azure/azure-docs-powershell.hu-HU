---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186421"
---
# <span data-ttu-id="28ec6-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="28ec6-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="28ec6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="28ec6-103">Tanúsítvány felvétele a megadott köteg fiókba.</span><span class="sxs-lookup"><span data-stu-id="28ec6-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="28ec6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28ec6-104">SYNTAX</span></span>

### <span data-ttu-id="28ec6-105">Fájl (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28ec6-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28ec6-106">RawData</span><span class="sxs-lookup"><span data-stu-id="28ec6-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28ec6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="28ec6-107">DESCRIPTION</span></span>
<span data-ttu-id="28ec6-108">A **New-AzBatchCertificate** parancsmag hozzáad egy tanúsítványt a megadott Azure-köteg fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="28ec6-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="28ec6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="28ec6-109">EXAMPLES</span></span>

### <span data-ttu-id="28ec6-110">1. példa: tanúsítvány hozzáadása fájlból</span><span class="sxs-lookup"><span data-stu-id="28ec6-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="28ec6-111">Ez a parancs egy tanúsítványt ad a megadott köteg fiókhoz a fájl E:\Certificates\MyCert.cer. használatával.</span><span class="sxs-lookup"><span data-stu-id="28ec6-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="28ec6-112">2. példa: tanúsítvány felvétele nyers adatforrásból</span><span class="sxs-lookup"><span data-stu-id="28ec6-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="28ec6-113">Az első parancs a MyCert. pfx fájlból az $RawData változóba olvassa be az adatot.</span><span class="sxs-lookup"><span data-stu-id="28ec6-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="28ec6-114">A második parancs a $RawData-ban tárolt nyers adatforrások segítségével felvesz egy tanúsítványt a megadott köteg-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="28ec6-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="28ec6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28ec6-115">PARAMETERS</span></span>

### <span data-ttu-id="28ec6-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="28ec6-116">-BatchContext</span></span>
<span data-ttu-id="28ec6-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="28ec6-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="28ec6-118">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="28ec6-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="28ec6-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="28ec6-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="28ec6-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="28ec6-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="28ec6-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="28ec6-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="28ec6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ec6-122">-DefaultProfile</span></span>
<span data-ttu-id="28ec6-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28ec6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28ec6-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="28ec6-124">-FilePath</span></span>
<span data-ttu-id="28ec6-125">A tanúsítványfájl elérési útjának elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ec6-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="28ec6-126">A tanúsítványfájl. cer vagy. pfx formátumban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="28ec6-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="28ec6-127">-Kind</span><span class="sxs-lookup"><span data-stu-id="28ec6-127">-Kind</span></span>
<span data-ttu-id="28ec6-128">A létrehozandó tanúsítvány típusa.</span><span class="sxs-lookup"><span data-stu-id="28ec6-128">The kind of certificate to create.</span></span> <span data-ttu-id="28ec6-129">Ha ez a funkció nincs megadva, az azt feltételezi, hogy minden jelszó nélküli tanúsítvány CER, és a jelszóval rendelkező minden tanúsítvány PFX.</span><span class="sxs-lookup"><span data-stu-id="28ec6-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

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

### <span data-ttu-id="28ec6-130">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="28ec6-130">-Password</span></span>
<span data-ttu-id="28ec6-131">A tanúsítvány titkos kulcsának eléréséhez használt jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ec6-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="28ec6-132">Ezt a paramétert akkor kell megadnia, ha a. pfx formátumú tanúsítványt ad meg.</span><span class="sxs-lookup"><span data-stu-id="28ec6-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="28ec6-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="28ec6-133">-RawData</span></span>
<span data-ttu-id="28ec6-134">A nyers hitelességi tanúsítványra vonatkozó adatot. cer vagy. pfx formátumban adja meg.</span><span class="sxs-lookup"><span data-stu-id="28ec6-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="28ec6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ec6-135">CommonParameters</span></span>
<span data-ttu-id="28ec6-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28ec6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ec6-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="28ec6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ec6-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28ec6-138">INPUTS</span></span>

### <span data-ttu-id="28ec6-139">System. byte []</span><span class="sxs-lookup"><span data-stu-id="28ec6-139">System.Byte[]</span></span>

### <span data-ttu-id="28ec6-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="28ec6-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="28ec6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28ec6-141">OUTPUTS</span></span>

### <span data-ttu-id="28ec6-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="28ec6-142">System.Void</span></span>

## <span data-ttu-id="28ec6-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28ec6-143">NOTES</span></span>

## <span data-ttu-id="28ec6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28ec6-144">RELATED LINKS</span></span>

[<span data-ttu-id="28ec6-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="28ec6-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="28ec6-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="28ec6-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="28ec6-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="28ec6-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="28ec6-148">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="28ec6-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
