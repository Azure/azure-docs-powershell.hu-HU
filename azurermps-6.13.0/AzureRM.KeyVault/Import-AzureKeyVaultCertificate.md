---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: 5cc7846ae1d5eba5764c524e4edfb470a7cd562b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679552"
---
# <span data-ttu-id="41fc4-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="41fc4-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="41fc4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="41fc4-103">Tanúsítványt importál egy kulcsos boltozatba.</span><span class="sxs-lookup"><span data-stu-id="41fc4-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41fc4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41fc4-104">SYNTAX</span></span>

### <span data-ttu-id="41fc4-105">ImportCertificateFromFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41fc4-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41fc4-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="41fc4-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41fc4-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="41fc4-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41fc4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="41fc4-108">DESCRIPTION</span></span>
<span data-ttu-id="41fc4-109">Az **import-AzureKeyVaultCertificate** parancsmag a tanúsítványt egy fő boltozatba importálja.</span><span class="sxs-lookup"><span data-stu-id="41fc4-109">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="41fc4-110">Az importálandó tanúsítványt az alábbi módszerek egyikével hozhatja létre:</span><span class="sxs-lookup"><span data-stu-id="41fc4-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="41fc4-111">A New-AzureKeyVaultCertificateSigningRequest parancsmaggal tanúsítvány-aláírási kérést hozhat létre, és elküldheti a tanúsítvány-szolgáltatónak.</span><span class="sxs-lookup"><span data-stu-id="41fc4-111">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="41fc4-112">Használjon meglévő tanúsítványfájl-fájlt, például. pfx vagy. P12 fájlt, amely mind a tanúsítványt, mind a titkos kulcsot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="41fc4-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="41fc4-113">Példák</span><span class="sxs-lookup"><span data-stu-id="41fc4-113">EXAMPLES</span></span>

### <span data-ttu-id="41fc4-114">1. példa: Key Vault-tanúsítvány importálása</span><span class="sxs-lookup"><span data-stu-id="41fc4-114">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="41fc4-115">Az első parancs az ConvertTo-SecureString parancsmagot használja a biztonságos jelszó létrehozására, majd a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="41fc4-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="41fc4-116">A második parancs importálja a ImportCert01 nevű tanúsítványt a CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="41fc4-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="41fc4-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41fc4-117">PARAMETERS</span></span>

### <span data-ttu-id="41fc4-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="41fc4-118">-CertificateCollection</span></span>
<span data-ttu-id="41fc4-119">Azt a gyűjteményt adja meg, amelyet egy kulcs boltozatához szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="41fc4-119">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41fc4-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="41fc4-120">-CertificateString</span></span>
<span data-ttu-id="41fc4-121">A tanúsítvány karakterláncát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41fc4-121">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="41fc4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41fc4-122">-DefaultProfile</span></span>
<span data-ttu-id="41fc4-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="41fc4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41fc4-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="41fc4-124">-FilePath</span></span>
<span data-ttu-id="41fc4-125">A parancsmag által importált tanúsítványfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41fc4-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41fc4-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41fc4-126">-Name</span></span>
<span data-ttu-id="41fc4-127">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41fc4-127">Specifies the certificate name.</span></span> <span data-ttu-id="41fc4-128">Ez a parancsmag a tanúsítvány teljes tartománynevét (FQDN) építi fel a kulcsfájl nevéből, a jelenleg kijelölt környezetből és a tanúsítvány nevéből.</span><span class="sxs-lookup"><span data-stu-id="41fc4-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41fc4-129">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="41fc4-129">-Password</span></span>
<span data-ttu-id="41fc4-130">A tanúsítványfájl jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41fc4-130">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41fc4-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="41fc4-131">-Tag</span></span>
<span data-ttu-id="41fc4-132">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="41fc4-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="41fc4-133">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="41fc4-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="41fc4-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="41fc4-134">-VaultName</span></span>
<span data-ttu-id="41fc4-135">Annak a kulcsnak a boltozatát adja meg, amelybe a parancsmag importálja a tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="41fc4-135">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="41fc4-136">Ez a parancsmag a kulcsfájl teljes tartománynevét (FQDN) építi fel a név és a jelenleg kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="41fc4-136">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="41fc4-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="41fc4-137">-Confirm</span></span>
<span data-ttu-id="41fc4-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="41fc4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41fc4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41fc4-139">-WhatIf</span></span>
<span data-ttu-id="41fc4-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="41fc4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41fc4-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41fc4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41fc4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41fc4-142">CommonParameters</span></span>
<span data-ttu-id="41fc4-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41fc4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41fc4-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41fc4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41fc4-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41fc4-145">INPUTS</span></span>

### <span data-ttu-id="41fc4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="41fc4-146">System.String</span></span>

### <span data-ttu-id="41fc4-147">System. Security. kriptográfia. X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="41fc4-147">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>
<span data-ttu-id="41fc4-148">Paraméterek: CertificateCollection (ByValue)</span><span class="sxs-lookup"><span data-stu-id="41fc4-148">Parameters: CertificateCollection (ByValue)</span></span>

### <span data-ttu-id="41fc4-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="41fc4-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="41fc4-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41fc4-150">OUTPUTS</span></span>

### <span data-ttu-id="41fc4-151">Microsoft. Azure. Command. PSKeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="41fc4-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="41fc4-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41fc4-152">NOTES</span></span>

## <span data-ttu-id="41fc4-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41fc4-153">RELATED LINKS</span></span>

[<span data-ttu-id="41fc4-154">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="41fc4-154">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
