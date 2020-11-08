---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6a687f67741a8d4925e3253c9f787532501ad186
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025304"
---
# <span data-ttu-id="3d8f4-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3d8f4-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="3d8f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d8f4-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8f4-103">Tanúsítványt importál egy kulcsos boltozatba.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="3d8f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d8f4-104">SYNTAX</span></span>

### <span data-ttu-id="3d8f4-105">ImportCertificateFromFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3d8f4-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d8f4-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="3d8f4-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d8f4-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="3d8f4-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d8f4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d8f4-108">DESCRIPTION</span></span>
<span data-ttu-id="3d8f4-109">Az **import-AzKeyVaultCertificate** parancsmag a tanúsítványt egy fő boltozatba importálja.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="3d8f4-110">Az importálandó tanúsítványt az alábbi módszerek egyikével hozhatja létre:</span><span class="sxs-lookup"><span data-stu-id="3d8f4-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="3d8f4-111">Ezzel a paranccsal `Add-AzKeyVaultCertificate` tanúsítvány-aláírási kérést hozhat létre, és elküldheti azt egy hitelesítő szervezetnek.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-111">Use `Add-AzKeyVaultCertificate` to create a certificate signing request and submit it to a certificate authority.</span></span> <span data-ttu-id="3d8f4-112">Olvassa el https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span><span class="sxs-lookup"><span data-stu-id="3d8f4-112">See https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span></span>
- <span data-ttu-id="3d8f4-113">Használjon meglévő tanúsítványfájl-fájlt, például. pfx vagy. P12 fájlt, amely mind a tanúsítványt, mind a titkos kulcsot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="3d8f4-114">Példák</span><span class="sxs-lookup"><span data-stu-id="3d8f4-114">EXAMPLES</span></span>

### <span data-ttu-id="3d8f4-115">1. példa: Key Vault-tanúsítvány importálása</span><span class="sxs-lookup"><span data-stu-id="3d8f4-115">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

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

<span data-ttu-id="3d8f4-116">Az első parancs az ConvertTo-SecureString parancsmagot használja a biztonságos jelszó létrehozására, majd a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="3d8f4-117">A második parancs importálja a ImportCert01 nevű tanúsítványt a CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="3d8f4-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d8f4-118">PARAMETERS</span></span>

### <span data-ttu-id="3d8f4-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="3d8f4-119">-CertificateCollection</span></span>
<span data-ttu-id="3d8f4-120">Azt a gyűjteményt adja meg, amelyet egy kulcs boltozatához szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-120">Specifies the certificate collection to add to a key vault.</span></span>

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

### <span data-ttu-id="3d8f4-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="3d8f4-121">-CertificateString</span></span>
<span data-ttu-id="3d8f4-122">A tanúsítvány karakterláncát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-122">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="3d8f4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d8f4-123">-DefaultProfile</span></span>
<span data-ttu-id="3d8f4-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3d8f4-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d8f4-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="3d8f4-125">-FilePath</span></span>
<span data-ttu-id="3d8f4-126">A parancsmag által importált tanúsítványfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="3d8f4-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3d8f4-127">-Name</span></span>
<span data-ttu-id="3d8f4-128">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-128">Specifies the certificate name.</span></span> <span data-ttu-id="3d8f4-129">Ez a parancsmag a tanúsítvány teljes tartománynevét (FQDN) építi fel a kulcsfájl nevéből, a jelenleg kijelölt környezetből és a tanúsítvány nevéből.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="3d8f4-130">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="3d8f4-130">-Password</span></span>
<span data-ttu-id="3d8f4-131">A tanúsítványfájl jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-131">Specifies the password for a certificate file.</span></span>

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

### <span data-ttu-id="3d8f4-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="3d8f4-132">-Tag</span></span>
<span data-ttu-id="3d8f4-133">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3d8f4-134">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3d8f4-134">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3d8f4-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3d8f4-135">-VaultName</span></span>
<span data-ttu-id="3d8f4-136">Annak a kulcsnak a boltozatát adja meg, amelybe a parancsmag importálja a tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="3d8f4-137">Ez a parancsmag a kulcsfájl teljes tartománynevét (FQDN) építi fel a név és a jelenleg kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3d8f4-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d8f4-138">-Confirm</span></span>
<span data-ttu-id="3d8f4-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d8f4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d8f4-140">-WhatIf</span></span>
<span data-ttu-id="3d8f4-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d8f4-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d8f4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8f4-143">CommonParameters</span></span>
<span data-ttu-id="3d8f4-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d8f4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8f4-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8f4-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d8f4-146">INPUTS</span></span>

### <span data-ttu-id="3d8f4-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3d8f4-147">System.String</span></span>

### <span data-ttu-id="3d8f4-148">System. Security. kriptográfia. X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="3d8f4-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="3d8f4-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d8f4-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d8f4-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d8f4-150">OUTPUTS</span></span>

### <span data-ttu-id="3d8f4-151">Microsoft. Azure. Command. PSKeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="3d8f4-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d8f4-152">NOTES</span></span>

## <span data-ttu-id="3d8f4-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d8f4-153">RELATED LINKS</span></span>

[<span data-ttu-id="3d8f4-154">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3d8f4-154">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="3d8f4-155">A CSR létrehozása és egyesítése a Key Vault-ban</span><span class="sxs-lookup"><span data-stu-id="3d8f4-155">Creating and merging CSR in Key Vault</span></span>](https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request)