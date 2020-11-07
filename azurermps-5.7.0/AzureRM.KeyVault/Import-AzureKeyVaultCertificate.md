---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: 37befa1434d18241b2f4721523de0ab48bebfd0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680708"
---
# <span data-ttu-id="b26aa-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b26aa-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="b26aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b26aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b26aa-103">Tanúsítványt importál egy kulcsos boltozatba.</span><span class="sxs-lookup"><span data-stu-id="b26aa-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b26aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b26aa-104">SYNTAX</span></span>

### <span data-ttu-id="b26aa-105">ImportCertificateFromFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b26aa-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b26aa-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="b26aa-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b26aa-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="b26aa-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b26aa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b26aa-108">DESCRIPTION</span></span>
<span data-ttu-id="b26aa-109">Az **import-AzureKeyVaultCertificate** parancsmag a tanúsítványt egy fő boltozatba importálja.</span><span class="sxs-lookup"><span data-stu-id="b26aa-109">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="b26aa-110">Az importálandó tanúsítványt az alábbi módszerek egyikével hozhatja létre:</span><span class="sxs-lookup"><span data-stu-id="b26aa-110">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="b26aa-111">A New-AzureKeyVaultCertificateSigningRequest parancsmaggal tanúsítvány-aláírási kérést hozhat létre, és elküldheti a tanúsítvány-szolgáltatónak.</span><span class="sxs-lookup"><span data-stu-id="b26aa-111">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="b26aa-112">Használjon meglévő tanúsítványfájl-fájlt, például. pfx vagy. P12 fájlt, amely mind a tanúsítványt, mind a titkos kulcsot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b26aa-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="b26aa-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b26aa-113">EXAMPLES</span></span>

### <span data-ttu-id="b26aa-114">1. példa: Key Vault-tanúsítvány importálása</span><span class="sxs-lookup"><span data-stu-id="b26aa-114">Example 1: Import a key vault certificate</span></span>
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

<span data-ttu-id="b26aa-115">Az első parancs az ConvertTo-SecureString parancsmagot használja a biztonságos jelszó létrehozására, majd a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b26aa-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="b26aa-116">A második parancs importálja a ImportCert01 nevű tanúsítványt a CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="b26aa-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="b26aa-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b26aa-117">PARAMETERS</span></span>

### <span data-ttu-id="b26aa-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="b26aa-118">-CertificateCollection</span></span>
<span data-ttu-id="b26aa-119">Azt a gyűjteményt adja meg, amelyet egy kulcs boltozatához szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="b26aa-119">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b26aa-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="b26aa-120">-CertificateString</span></span>
<span data-ttu-id="b26aa-121">A tanúsítvány karakterláncát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b26aa-121">Specifies a certificate string.</span></span>

```yaml
Type: String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26aa-122">-DefaultProfile</span></span>
<span data-ttu-id="b26aa-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b26aa-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b26aa-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b26aa-124">-FilePath</span></span>
<span data-ttu-id="b26aa-125">A parancsmag által importált tanúsítványfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b26aa-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26aa-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b26aa-126">-Name</span></span>
<span data-ttu-id="b26aa-127">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b26aa-127">Specifies the certificate name.</span></span> <span data-ttu-id="b26aa-128">Ez a parancsmag a tanúsítvány teljes tartománynevét (FQDN) építi fel a kulcsfájl nevéből, a jelenleg kijelölt környezetből és a tanúsítvány nevéből.</span><span class="sxs-lookup"><span data-stu-id="b26aa-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b26aa-129">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="b26aa-129">-Password</span></span>
<span data-ttu-id="b26aa-130">A tanúsítványfájl jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b26aa-130">Specifies the password for a certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26aa-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="b26aa-131">-Tag</span></span>
<span data-ttu-id="b26aa-132">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="b26aa-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b26aa-133">Példa:</span><span class="sxs-lookup"><span data-stu-id="b26aa-133">For example:</span></span>

<span data-ttu-id="b26aa-134">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="b26aa-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b26aa-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b26aa-135">-VaultName</span></span>
<span data-ttu-id="b26aa-136">Annak a kulcsnak a boltozatát adja meg, amelybe a parancsmag importálja a tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="b26aa-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="b26aa-137">Ez a parancsmag a kulcsfájl teljes tartománynevét (FQDN) építi fel a név és a jelenleg kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="b26aa-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b26aa-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b26aa-138">-Confirm</span></span>
<span data-ttu-id="b26aa-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b26aa-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26aa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b26aa-140">-WhatIf</span></span>
<span data-ttu-id="b26aa-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b26aa-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b26aa-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b26aa-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26aa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26aa-143">CommonParameters</span></span>
<span data-ttu-id="b26aa-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b26aa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26aa-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b26aa-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26aa-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b26aa-146">INPUTS</span></span>

### <span data-ttu-id="b26aa-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="b26aa-147">None</span></span>
<span data-ttu-id="b26aa-148">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b26aa-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b26aa-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b26aa-149">OUTPUTS</span></span>

### <span data-ttu-id="b26aa-150">Microsoft. Azure. Command. PSKeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="b26aa-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="b26aa-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b26aa-151">NOTES</span></span>

## <span data-ttu-id="b26aa-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b26aa-152">RELATED LINKS</span></span>

[<span data-ttu-id="b26aa-153">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b26aa-153">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
