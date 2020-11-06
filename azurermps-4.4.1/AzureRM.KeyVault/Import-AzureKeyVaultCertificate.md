---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: b97dc509ad6508c2cbec79d6ba1db27508f94c34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493490"
---
# <span data-ttu-id="1cc07-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1cc07-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="1cc07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1cc07-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc07-103">Tanúsítványt importál egy kulcsos boltozatba.</span><span class="sxs-lookup"><span data-stu-id="1cc07-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cc07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1cc07-104">SYNTAX</span></span>

### <span data-ttu-id="1cc07-105">ImportCertificateFromFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1cc07-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc07-106">ImportWithPrivateKeyFromFile</span><span class="sxs-lookup"><span data-stu-id="1cc07-106">ImportWithPrivateKeyFromFile</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cc07-107">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="1cc07-107">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cc07-108">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="1cc07-108">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 -CertificateCollection <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cc07-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="1cc07-109">DESCRIPTION</span></span>
<span data-ttu-id="1cc07-110">Az **import-AzureKeyVaultCertificate** parancsmag a tanúsítványt egy fő boltozatba importálja.</span><span class="sxs-lookup"><span data-stu-id="1cc07-110">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="1cc07-111">Az importálandó tanúsítványt az alábbi módszerek egyikével hozhatja létre:</span><span class="sxs-lookup"><span data-stu-id="1cc07-111">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="1cc07-112">A New-AzureKeyVaultCertificateSigningRequest parancsmaggal tanúsítvány-aláírási kérést hozhat létre, és elküldheti a tanúsítvány-szolgáltatónak.</span><span class="sxs-lookup"><span data-stu-id="1cc07-112">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="1cc07-113">Használjon meglévő tanúsítványfájl-fájlt, például. pfx vagy. P12 fájlt, amely mind a tanúsítványt, mind a titkos kulcsot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1cc07-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="1cc07-114">Példák</span><span class="sxs-lookup"><span data-stu-id="1cc07-114">EXAMPLES</span></span>

### <span data-ttu-id="1cc07-115">1. példa: Key Vault-tanúsítvány importálása</span><span class="sxs-lookup"><span data-stu-id="1cc07-115">Example 1: Import a key vault certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password
Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="1cc07-116">Az első parancs az ConvertTo-SecureString parancsmagot használja a biztonságos jelszó létrehozására, majd a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1cc07-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="1cc07-117">A második parancs importálja a ImportCert01 nevű tanúsítványt a CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="1cc07-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="1cc07-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1cc07-118">PARAMETERS</span></span>

### <span data-ttu-id="1cc07-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="1cc07-119">-CertificateCollection</span></span>
<span data-ttu-id="1cc07-120">Azt a gyűjteményt adja meg, amelyet egy kulcs boltozatához szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="1cc07-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc07-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="1cc07-121">-CertificateString</span></span>
<span data-ttu-id="1cc07-122">A tanúsítvány karakterláncát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1cc07-122">Specifies a certificate string.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc07-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1cc07-123">-Confirm</span></span>
<span data-ttu-id="1cc07-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1cc07-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc07-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="1cc07-125">-FilePath</span></span>
<span data-ttu-id="1cc07-126">A parancsmag által importált tanúsítványfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1cc07-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc07-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1cc07-127">-Name</span></span>
<span data-ttu-id="1cc07-128">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1cc07-128">Specifies the certificate name.</span></span> <span data-ttu-id="1cc07-129">Ez a parancsmag a tanúsítvány teljes tartománynevét (FQDN) építi fel a kulcsfájl nevéből, a jelenleg kijelölt környezetből és a tanúsítvány nevéből.</span><span class="sxs-lookup"><span data-stu-id="1cc07-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cc07-130">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="1cc07-130">-Password</span></span>
<span data-ttu-id="1cc07-131">A tanúsítványfájl jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1cc07-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportWithPrivateKeyFromFile, ImportWithPrivateKeyFromString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc07-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="1cc07-132">-Tag</span></span>
<span data-ttu-id="1cc07-133">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="1cc07-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1cc07-134">Példa:</span><span class="sxs-lookup"><span data-stu-id="1cc07-134">For example:</span></span>

<span data-ttu-id="1cc07-135">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="1cc07-135">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cc07-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1cc07-136">-VaultName</span></span>
<span data-ttu-id="1cc07-137">Annak a kulcsnak a boltozatát adja meg, amelybe a parancsmag importálja a tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="1cc07-137">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="1cc07-138">Ez a parancsmag a kulcsfájl teljes tartománynevét (FQDN) építi fel a név és a jelenleg kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="1cc07-138">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1cc07-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc07-139">-WhatIf</span></span>
<span data-ttu-id="1cc07-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1cc07-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc07-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1cc07-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc07-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc07-142">-DefaultProfile</span></span>
<span data-ttu-id="1cc07-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1cc07-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cc07-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc07-144">CommonParameters</span></span>
<span data-ttu-id="1cc07-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1cc07-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc07-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cc07-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc07-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cc07-147">INPUTS</span></span>

## <span data-ttu-id="1cc07-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cc07-148">OUTPUTS</span></span>

### <span data-ttu-id="1cc07-149">Microsoft. Azure. Command. CertificateBundle. models.</span><span class="sxs-lookup"><span data-stu-id="1cc07-149">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="1cc07-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1cc07-150">NOTES</span></span>

## <span data-ttu-id="1cc07-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cc07-151">RELATED LINKS</span></span>

[<span data-ttu-id="1cc07-152">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1cc07-152">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
