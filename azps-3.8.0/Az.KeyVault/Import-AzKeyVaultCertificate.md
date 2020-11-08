---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 4d78e325908cf7863177b6bb3e1ebed67f4b36de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010685"
---
# <span data-ttu-id="3922f-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3922f-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="3922f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3922f-102">SYNOPSIS</span></span>
<span data-ttu-id="3922f-103">Tanúsítványt importál egy kulcsos boltozatba.</span><span class="sxs-lookup"><span data-stu-id="3922f-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="3922f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3922f-104">SYNTAX</span></span>

### <span data-ttu-id="3922f-105">ImportCertificateFromFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3922f-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3922f-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="3922f-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3922f-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="3922f-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3922f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3922f-108">DESCRIPTION</span></span>
<span data-ttu-id="3922f-109">Az **import-AzKeyVaultCertificate** parancsmag a tanúsítványt egy fő boltozatba importálja.</span><span class="sxs-lookup"><span data-stu-id="3922f-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="3922f-110">Az importálandó tanúsítványt az alábbi módszerek egyikével hozhatja létre:</span><span class="sxs-lookup"><span data-stu-id="3922f-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="3922f-111">A New-AzKeyVaultCertificateSigningRequest parancsmaggal tanúsítvány-aláírási kérést hozhat létre, és elküldheti a tanúsítvány-szolgáltatónak.</span><span class="sxs-lookup"><span data-stu-id="3922f-111">Use the New-AzKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="3922f-112">Használjon meglévő tanúsítványfájl-fájlt, például. pfx vagy. P12 fájlt, amely mind a tanúsítványt, mind a titkos kulcsot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3922f-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="3922f-113">Példák</span><span class="sxs-lookup"><span data-stu-id="3922f-113">EXAMPLES</span></span>

### <span data-ttu-id="3922f-114">1. példa: Key Vault-tanúsítvány importálása</span><span class="sxs-lookup"><span data-stu-id="3922f-114">Example 1: Import a key vault certificate</span></span>
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

<span data-ttu-id="3922f-115">Az első parancs az ConvertTo-SecureString parancsmagot használja a biztonságos jelszó létrehozására, majd a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3922f-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="3922f-116">A második parancs importálja a ImportCert01 nevű tanúsítványt a CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="3922f-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="3922f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3922f-117">PARAMETERS</span></span>

### <span data-ttu-id="3922f-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="3922f-118">-CertificateCollection</span></span>
<span data-ttu-id="3922f-119">Azt a gyűjteményt adja meg, amelyet egy kulcs boltozatához szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="3922f-119">Specifies the certificate collection to add to a key vault.</span></span>

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

### <span data-ttu-id="3922f-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="3922f-120">-CertificateString</span></span>
<span data-ttu-id="3922f-121">A tanúsítvány karakterláncát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3922f-121">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="3922f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3922f-122">-DefaultProfile</span></span>
<span data-ttu-id="3922f-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3922f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3922f-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="3922f-124">-FilePath</span></span>
<span data-ttu-id="3922f-125">A parancsmag által importált tanúsítványfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3922f-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="3922f-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3922f-126">-Name</span></span>
<span data-ttu-id="3922f-127">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3922f-127">Specifies the certificate name.</span></span> <span data-ttu-id="3922f-128">Ez a parancsmag a tanúsítvány teljes tartománynevét (FQDN) építi fel a kulcsfájl nevéből, a jelenleg kijelölt környezetből és a tanúsítvány nevéből.</span><span class="sxs-lookup"><span data-stu-id="3922f-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="3922f-129">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="3922f-129">-Password</span></span>
<span data-ttu-id="3922f-130">A tanúsítványfájl jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3922f-130">Specifies the password for a certificate file.</span></span>

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

### <span data-ttu-id="3922f-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="3922f-131">-Tag</span></span>
<span data-ttu-id="3922f-132">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="3922f-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3922f-133">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3922f-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3922f-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3922f-134">-VaultName</span></span>
<span data-ttu-id="3922f-135">Annak a kulcsnak a boltozatát adja meg, amelybe a parancsmag importálja a tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="3922f-135">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="3922f-136">Ez a parancsmag a kulcsfájl teljes tartománynevét (FQDN) építi fel a név és a jelenleg kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="3922f-136">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3922f-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3922f-137">-Confirm</span></span>
<span data-ttu-id="3922f-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3922f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3922f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3922f-139">-WhatIf</span></span>
<span data-ttu-id="3922f-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3922f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3922f-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3922f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3922f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3922f-142">CommonParameters</span></span>
<span data-ttu-id="3922f-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3922f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3922f-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3922f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3922f-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3922f-145">INPUTS</span></span>

### <span data-ttu-id="3922f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3922f-146">System.String</span></span>

### <span data-ttu-id="3922f-147">System. Security. kriptográfia. X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="3922f-147">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="3922f-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3922f-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3922f-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3922f-149">OUTPUTS</span></span>

### <span data-ttu-id="3922f-150">Microsoft. Azure. Command. PSKeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="3922f-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="3922f-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3922f-151">NOTES</span></span>

## <span data-ttu-id="3922f-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3922f-152">RELATED LINKS</span></span>

[<span data-ttu-id="3922f-153">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3922f-153">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
