---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6a687f67741a8d4925e3253c9f787532501ad186
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361687"
---
# <span data-ttu-id="3ae5a-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3ae5a-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="3ae5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ae5a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae5a-103">Tanúsítványt importál egy kulcstárolóba.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="3ae5a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3ae5a-104">SYNTAX</span></span>

### <span data-ttu-id="3ae5a-105">ImportCertificateFromFile (default)</span><span class="sxs-lookup"><span data-stu-id="3ae5a-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ae5a-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="3ae5a-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ae5a-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="3ae5a-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ae5a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3ae5a-108">DESCRIPTION</span></span>
<span data-ttu-id="3ae5a-109">Az **Import-AzKeyVaultCertificate** parancsmag egy kulcstárolóba importálja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="3ae5a-110">Az importálni szükséges tanúsítványt az alábbi módszerek egyikével hozhatja létre:</span><span class="sxs-lookup"><span data-stu-id="3ae5a-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="3ae5a-111">Segítségével `Add-AzKeyVaultCertificate` létrehozhat egy tanúsítvány-aláírási kérést, és elküldheti azt egy hitelesítésszolgáltatónak.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-111">Use `Add-AzKeyVaultCertificate` to create a certificate signing request and submit it to a certificate authority.</span></span> <span data-ttu-id="3ae5a-112">Lásd: https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span><span class="sxs-lookup"><span data-stu-id="3ae5a-112">See https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span></span>
- <span data-ttu-id="3ae5a-113">Használjon meglévő tanúsítványcsomagfájlt, például egy .pfx vagy .p12 fájlt, amely tartalmazza a tanúsítványt és a személyes kulcsot is.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="3ae5a-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3ae5a-114">EXAMPLES</span></span>

### <span data-ttu-id="3ae5a-115">1. példa: Kulcstároló tanúsítványának importálása</span><span class="sxs-lookup"><span data-stu-id="3ae5a-115">Example 1: Import a key vault certificate</span></span>
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

<span data-ttu-id="3ae5a-116">Az első parancs a ConvertTo-SecureString parancsmag használatával hoz létre egy biztonságos jelszót, majd tárolja azt a $Password változóban.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="3ae5a-117">A második parancs importálja az ImportCert01 nevű tanúsítványt a CosotosoKV01 kulcstárolóba.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="3ae5a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ae5a-118">PARAMETERS</span></span>

### <span data-ttu-id="3ae5a-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="3ae5a-119">-CertificateCollection</span></span>
<span data-ttu-id="3ae5a-120">Megadja a kulcstárolóhoz hozzáadni szükséges tanúsítványgyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-120">Specifies the certificate collection to add to a key vault.</span></span>

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

### <span data-ttu-id="3ae5a-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="3ae5a-121">-CertificateString</span></span>
<span data-ttu-id="3ae5a-122">Egy tanúsítvány-karakterláncot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-122">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="3ae5a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae5a-123">-DefaultProfile</span></span>
<span data-ttu-id="3ae5a-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3ae5a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ae5a-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="3ae5a-125">-FilePath</span></span>
<span data-ttu-id="3ae5a-126">A parancsmag által importálni kívánt tanúsítványfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="3ae5a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3ae5a-127">-Name</span></span>
<span data-ttu-id="3ae5a-128">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-128">Specifies the certificate name.</span></span> <span data-ttu-id="3ae5a-129">Ez a parancsmag egy tanúsítvány teljes tartománynevét (FQDN) építi fel a kulcstároló neve, az aktuálisan kijelölt környezet és a tanúsítvány neve alapján.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="3ae5a-130">-Password</span><span class="sxs-lookup"><span data-stu-id="3ae5a-130">-Password</span></span>
<span data-ttu-id="3ae5a-131">A tanúsítványfájl jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-131">Specifies the password for a certificate file.</span></span>

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

### <span data-ttu-id="3ae5a-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="3ae5a-132">-Tag</span></span>
<span data-ttu-id="3ae5a-133">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3ae5a-134">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="3ae5a-134">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3ae5a-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3ae5a-135">-VaultName</span></span>
<span data-ttu-id="3ae5a-136">Megadja a kulcstár nevét, amelybe ez a parancsmag importálja a tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="3ae5a-137">Ez a parancsmag egy kulcstár teljes tartománynevét (FQDN) építi fel a név és a jelenleg kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3ae5a-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ae5a-138">-Confirm</span></span>
<span data-ttu-id="3ae5a-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ae5a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ae5a-140">-WhatIf</span></span>
<span data-ttu-id="3ae5a-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ae5a-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ae5a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae5a-143">CommonParameters</span></span>
<span data-ttu-id="3ae5a-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ae5a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae5a-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ae5a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae5a-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ae5a-146">INPUTS</span></span>

### <span data-ttu-id="3ae5a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3ae5a-147">System.String</span></span>

### <span data-ttu-id="3ae5a-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="3ae5a-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="3ae5a-149">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3ae5a-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3ae5a-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ae5a-150">OUTPUTS</span></span>

### <span data-ttu-id="3ae5a-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3ae5a-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="3ae5a-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3ae5a-152">NOTES</span></span>

## <span data-ttu-id="3ae5a-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ae5a-153">RELATED LINKS</span></span>

[<span data-ttu-id="3ae5a-154">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3ae5a-154">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="3ae5a-155">A CSR létrehozása és egyesítése a kulcstárban</span><span class="sxs-lookup"><span data-stu-id="3ae5a-155">Creating and merging CSR in Key Vault</span></span>](https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request)