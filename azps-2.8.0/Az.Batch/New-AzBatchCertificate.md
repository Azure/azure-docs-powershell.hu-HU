---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: d0fefe06ad5392d2fe50552203a08872eea4e61f
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847994"
---
# <span data-ttu-id="d6331-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d6331-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="d6331-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6331-102">SYNOPSIS</span></span>
<span data-ttu-id="d6331-103">Tanúsítvány felvétele a megadott köteg fiókba.</span><span class="sxs-lookup"><span data-stu-id="d6331-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="d6331-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6331-104">SYNTAX</span></span>

### <span data-ttu-id="d6331-105">Fájl (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6331-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6331-106">RawData</span><span class="sxs-lookup"><span data-stu-id="d6331-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6331-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6331-107">DESCRIPTION</span></span>
<span data-ttu-id="d6331-108">A **New-AzBatchCertificate** parancsmag hozzáad egy tanúsítványt a megadott Azure-köteg fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="d6331-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="d6331-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d6331-109">EXAMPLES</span></span>

### <span data-ttu-id="d6331-110">1. példa: tanúsítvány hozzáadása fájlból</span><span class="sxs-lookup"><span data-stu-id="d6331-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="d6331-111">Ez a parancs egy tanúsítványt ad a megadott köteg fiókhoz a fájl E:\Certificates\MyCert.cer. használatával.</span><span class="sxs-lookup"><span data-stu-id="d6331-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="d6331-112">2. példa: tanúsítvány felvétele nyers adatforrásból</span><span class="sxs-lookup"><span data-stu-id="d6331-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="d6331-113">Az első parancs a MyCert. pfx fájlból az $RawData változóba olvassa be az adatot.</span><span class="sxs-lookup"><span data-stu-id="d6331-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="d6331-114">A második parancs a $RawData-ban tárolt nyers adatforrások segítségével felvesz egy tanúsítványt a megadott köteg-fiókjába.</span><span class="sxs-lookup"><span data-stu-id="d6331-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="d6331-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6331-115">PARAMETERS</span></span>

### <span data-ttu-id="d6331-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d6331-116">-BatchContext</span></span>
<span data-ttu-id="d6331-117">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="d6331-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d6331-118">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="d6331-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d6331-119">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="d6331-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d6331-120">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="d6331-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d6331-121">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="d6331-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d6331-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6331-122">-DefaultProfile</span></span>
<span data-ttu-id="d6331-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6331-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6331-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d6331-124">-FilePath</span></span>
<span data-ttu-id="d6331-125">A tanúsítványfájl elérési útjának elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6331-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="d6331-126">A tanúsítványfájl. cer vagy. pfx formátumban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d6331-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="d6331-127">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="d6331-127">-Password</span></span>
<span data-ttu-id="d6331-128">A tanúsítvány titkos kulcsának eléréséhez használt jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6331-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="d6331-129">Ezt a paramétert akkor kell megadnia, ha a. pfx formátumú tanúsítványt ad meg.</span><span class="sxs-lookup"><span data-stu-id="d6331-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="d6331-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="d6331-130">-RawData</span></span>
<span data-ttu-id="d6331-131">A nyers hitelességi tanúsítványra vonatkozó adatot. cer vagy. pfx formátumban adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6331-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="d6331-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6331-132">CommonParameters</span></span>
<span data-ttu-id="d6331-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6331-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6331-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6331-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6331-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6331-135">INPUTS</span></span>

### <span data-ttu-id="d6331-136">System. byte []</span><span class="sxs-lookup"><span data-stu-id="d6331-136">System.Byte[]</span></span>

### <span data-ttu-id="d6331-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d6331-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d6331-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6331-138">OUTPUTS</span></span>

### <span data-ttu-id="d6331-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="d6331-139">System.Void</span></span>

## <span data-ttu-id="d6331-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6331-140">NOTES</span></span>

## <span data-ttu-id="d6331-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6331-141">RELATED LINKS</span></span>

[<span data-ttu-id="d6331-142">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d6331-142">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="d6331-143">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d6331-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d6331-144">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d6331-144">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="d6331-145">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d6331-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


