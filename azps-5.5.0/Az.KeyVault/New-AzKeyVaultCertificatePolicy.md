---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152794"
---
# <span data-ttu-id="0c10b-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0c10b-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0c10b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c10b-102">SYNOPSIS</span></span>
<span data-ttu-id="0c10b-103">Memóriában létrehozott tanúsítvány-házirendobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0c10b-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="0c10b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0c10b-104">SYNTAX</span></span>

### <span data-ttu-id="0c10b-105">SubjectName (Default)</span><span class="sxs-lookup"><span data-stu-id="0c10b-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c10b-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="0c10b-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c10b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0c10b-107">DESCRIPTION</span></span>
<span data-ttu-id="0c10b-108">A **New-AzKeyVaultCertificatePolicy parancsmag** létrehoz egy memóriabeli tanúsítványházi házirendobjektumot az Azure-kulcstárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="0c10b-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="0c10b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0c10b-109">EXAMPLES</span></span>

### <span data-ttu-id="0c10b-110">1. példa: Tanúsítvány-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c10b-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        :
KeyUsage                        :
Ekus                            :
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="0c10b-111">Ez a parancs egy hat hónapig érvényes tanúsítvány-házirendet hoz létre, és a kulcsot újra felhasználja a tanúsítvány megújítására.</span><span class="sxs-lookup"><span data-stu-id="0c10b-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="0c10b-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="0c10b-112">Example 2</span></span>

<span data-ttu-id="0c10b-113">Memóriában létrehozott tanúsítvány-házirendobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0c10b-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="0c10b-114">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="0c10b-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="0c10b-115">3. példa: Másodlagos tulajdonosi név (vagy SAN) tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c10b-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -DnsName "contoso.com","support.contoso.com","docs.contoso.com" -IssuerName "Self"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : False
SubjectName                     : CN=contoso.com
DnsNames                        : {contoso.com, support.contoso.com, docs.contoso.com}
KeyUsage                        :
Ekus                            :
ValidityInMonths                :
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="0c10b-116">Ebben a példában egy 3 DNS-névvel létrehozott SAN tanúsítványt hozunk létre.</span><span class="sxs-lookup"><span data-stu-id="0c10b-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="0c10b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c10b-117">PARAMETERS</span></span>

### <span data-ttu-id="0c10b-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="0c10b-118">-CertificateTransparency</span></span>
<span data-ttu-id="0c10b-119">Azt jelzi, hogy engedélyezve van-e a tanúsítvány áttetszőség ehhez a tanúsítványhoz/kibocsátóhoz; ha nincs megadva, az alapértelmezett érték "igaz"</span><span class="sxs-lookup"><span data-stu-id="0c10b-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="0c10b-120">-CertificateType</span></span>
<span data-ttu-id="0c10b-121">A kibocsátó tanúsítványának típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0c10b-121">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-122">-Curve</span><span class="sxs-lookup"><span data-stu-id="0c10b-122">-Curve</span></span>
<span data-ttu-id="0c10b-123">A tanúsítvány kulcsának három ponttal megadott görbeneve.</span><span class="sxs-lookup"><span data-stu-id="0c10b-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="0c10b-124">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="0c10b-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c10b-125">P-256</span><span class="sxs-lookup"><span data-stu-id="0c10b-125">P-256</span></span>
- <span data-ttu-id="0c10b-126">P-384</span><span class="sxs-lookup"><span data-stu-id="0c10b-126">P-384</span></span>
- <span data-ttu-id="0c10b-127">P-521</span><span class="sxs-lookup"><span data-stu-id="0c10b-127">P-521</span></span>
- <span data-ttu-id="0c10b-128">P-256K</span><span class="sxs-lookup"><span data-stu-id="0c10b-128">P-256K</span></span>
- <span data-ttu-id="0c10b-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="0c10b-129">SECP256K1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: P-256, P-384, P-521, P-256K, SECP256K1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c10b-130">-DefaultProfile</span></span>
<span data-ttu-id="0c10b-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0c10b-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c10b-132">-Disabled</span><span class="sxs-lookup"><span data-stu-id="0c10b-132">-Disabled</span></span>
<span data-ttu-id="0c10b-133">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="0c10b-133">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="0c10b-134">-DnsName</span></span>
<span data-ttu-id="0c10b-135">A tanúsítványBAN szereplő DNS-neveket adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c10b-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="0c10b-136">A tulajdonos alternatív nevei (SAN-k) DNS-nevekként is meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="0c10b-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: DNSNames
Aliases: DnsNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-137">-Ekus</span><span class="sxs-lookup"><span data-stu-id="0c10b-137">-Ekus</span></span>
<span data-ttu-id="0c10b-138">A tanúsítványban megadott továbbfejlesztett kulcshasználatot (EKUs) adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c10b-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="0c10b-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="0c10b-140">Azt adja meg, hogy az automatikus értesítési folyamat hány nappal a lejárat előtt induljon el.</span><span class="sxs-lookup"><span data-stu-id="0c10b-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="0c10b-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="0c10b-142">Meghatározza, hogy az értesítés automatikus eljárása hány százaléka után indul el.</span><span class="sxs-lookup"><span data-stu-id="0c10b-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-143">-KibocsátóNeve</span><span class="sxs-lookup"><span data-stu-id="0c10b-143">-IssuerName</span></span>
<span data-ttu-id="0c10b-144">A tanúsítvány kibocsátójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c10b-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="0c10b-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="0c10b-145">-KeyNotExportable</span></span>
<span data-ttu-id="0c10b-146">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="0c10b-146">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-147">-KeySize</span><span class="sxs-lookup"><span data-stu-id="0c10b-147">-KeySize</span></span>
<span data-ttu-id="0c10b-148">A tanúsítvány kulcsméretét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0c10b-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="0c10b-149">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="0c10b-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c10b-150">2048</span><span class="sxs-lookup"><span data-stu-id="0c10b-150">2048</span></span>
- <span data-ttu-id="0c10b-151">3072</span><span class="sxs-lookup"><span data-stu-id="0c10b-151">3072</span></span>
- <span data-ttu-id="0c10b-152">4096</span><span class="sxs-lookup"><span data-stu-id="0c10b-152">4096</span></span>
- <span data-ttu-id="0c10b-153">256</span><span class="sxs-lookup"><span data-stu-id="0c10b-153">256</span></span>
- <span data-ttu-id="0c10b-154">384</span><span class="sxs-lookup"><span data-stu-id="0c10b-154">384</span></span>
- <span data-ttu-id="0c10b-155">521</span><span class="sxs-lookup"><span data-stu-id="0c10b-155">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="0c10b-156">-KeyType</span></span>
<span data-ttu-id="0c10b-157">A tanúsítványt visszaő kulcs típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0c10b-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="0c10b-158">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="0c10b-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c10b-159">RSA</span><span class="sxs-lookup"><span data-stu-id="0c10b-159">RSA</span></span>
- <span data-ttu-id="0c10b-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="0c10b-160">RSA-HSM</span></span>
- <span data-ttu-id="0c10b-161">EC</span><span class="sxs-lookup"><span data-stu-id="0c10b-161">EC</span></span>
- <span data-ttu-id="0c10b-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="0c10b-162">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-163">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="0c10b-163">-KeyUsage</span></span>
<span data-ttu-id="0c10b-164">A tanúsítvány kulcshasználati kulcsát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0c10b-164">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: (All)
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="0c10b-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="0c10b-166">Azt adja meg, hogy hány nappal a lejárat előtt induljon el a tanúsítvány automatikus megújítási folyamata.</span><span class="sxs-lookup"><span data-stu-id="0c10b-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="0c10b-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="0c10b-168">Meghatározza, hogy a tanúsítvány megújításának automatikus folyamata hány százaléka után indul el.</span><span class="sxs-lookup"><span data-stu-id="0c10b-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="0c10b-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="0c10b-170">Azt jelzi, hogy a tanúsítvány újra felhasználja a kulcsot a megújítás során.</span><span class="sxs-lookup"><span data-stu-id="0c10b-170">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="0c10b-171">-SecretContentType</span></span>
<span data-ttu-id="0c10b-172">Az új kulcstár-titkos kulcs tartalomtípusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0c10b-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="0c10b-173">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="0c10b-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c10b-174">alkalmazás/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="0c10b-174">application/x-pkcs12</span></span>
- <span data-ttu-id="0c10b-175">application/x-pem-file</span><span class="sxs-lookup"><span data-stu-id="0c10b-175">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="0c10b-176">-SubjectName</span></span>
<span data-ttu-id="0c10b-177">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c10b-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="0c10b-178">Ha a paraméterben egy tulajdonságon belül vesszőt (,) vagy pontot (.) kell használnia, a tulajdonságmezőt idézőjelek közé `SubjectName` kell tenni.</span><span class="sxs-lookup"><span data-stu-id="0c10b-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="0c10b-179">Használhatja például az O="Contoso, Ltd" használhatja.</span><span class="sxs-lookup"><span data-stu-id="0c10b-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="0c10b-180">gombra a Szervezet neve mezőben.</span><span class="sxs-lookup"><span data-stu-id="0c10b-180">in the Organization Name field.</span></span>

```yaml
Type: System.String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="0c10b-181">-ValidityInMonths</span></span>
<span data-ttu-id="0c10b-182">Azt adja meg, hogy a tanúsítvány hány hónapig érvényes.</span><span class="sxs-lookup"><span data-stu-id="0c10b-182">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c10b-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c10b-183">-Confirm</span></span>
<span data-ttu-id="0c10b-184">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0c10b-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c10b-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c10b-185">-WhatIf</span></span>
<span data-ttu-id="0c10b-186">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0c10b-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c10b-187">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c10b-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c10b-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c10b-188">CommonParameters</span></span>
<span data-ttu-id="0c10b-189">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c10b-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c10b-190">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c10b-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c10b-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c10b-191">INPUTS</span></span>

### <span data-ttu-id="0c10b-192">System.String</span><span class="sxs-lookup"><span data-stu-id="0c10b-192">System.String</span></span>

### <span data-ttu-id="0c10b-193">System.Collections.Generic.List'1[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0c10b-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0c10b-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0c10b-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0c10b-195">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0c10b-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0c10b-196">System.Collections.Generic.List'1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="0c10b-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="0c10b-197">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c10b-197">OUTPUTS</span></span>

### <span data-ttu-id="0c10b-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0c10b-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0c10b-199">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0c10b-199">NOTES</span></span>

## <span data-ttu-id="0c10b-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c10b-200">RELATED LINKS</span></span>

[<span data-ttu-id="0c10b-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0c10b-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="0c10b-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0c10b-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

