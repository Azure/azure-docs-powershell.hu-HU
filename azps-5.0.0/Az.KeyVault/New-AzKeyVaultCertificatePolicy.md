---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296861"
---
# <span data-ttu-id="c321c-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c321c-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c321c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c321c-102">SYNOPSIS</span></span>
<span data-ttu-id="c321c-103">A memória tanúsítvány házirend-objektumát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c321c-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="c321c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c321c-104">SYNTAX</span></span>

### <span data-ttu-id="c321c-105">SubjectName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c321c-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="c321c-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="c321c-106">DNSNames</span></span>
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

## <span data-ttu-id="c321c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c321c-107">DESCRIPTION</span></span>
<span data-ttu-id="c321c-108">A **New-AzKeyVaultCertificatePolicy** parancsmag létrehoz egy memória-alapú tanúsítvány házirend-objektumot az Azure Key Vault-hoz.</span><span class="sxs-lookup"><span data-stu-id="c321c-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="c321c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c321c-109">EXAMPLES</span></span>

### <span data-ttu-id="c321c-110">Példa 1: tanúsítvány-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="c321c-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="c321c-111">Ez a parancs hat hónapig érvényes tanúsítvány-házirendet hoz létre, és a kulcsot újra felhasználja a tanúsítvány megújításához.</span><span class="sxs-lookup"><span data-stu-id="c321c-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="c321c-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c321c-112">Example 2</span></span>

<span data-ttu-id="c321c-113">A memória tanúsítvány házirend-objektumát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c321c-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="c321c-114">autogenerated</span><span class="sxs-lookup"><span data-stu-id="c321c-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="c321c-115">3. példa: tárgyi alternatív név (vagy SAN) tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="c321c-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

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

<span data-ttu-id="c321c-116">Ebben a példában egy 3 DNS-nevet tartalmazó SAN tanúsítvány jön létre.</span><span class="sxs-lookup"><span data-stu-id="c321c-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="c321c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c321c-117">PARAMETERS</span></span>

### <span data-ttu-id="c321c-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="c321c-118">-CertificateTransparency</span></span>
<span data-ttu-id="c321c-119">Azt jelzi, hogy engedélyezve van-e a hitelességi bizonyítvány vagy a tanúsítvány áttetszősége. Ha nincs megadva, az alapértelmezett érték az "igaz"</span><span class="sxs-lookup"><span data-stu-id="c321c-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="c321c-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="c321c-120">-CertificateType</span></span>
<span data-ttu-id="c321c-121">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c321c-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="c321c-122">-Görbe</span><span class="sxs-lookup"><span data-stu-id="c321c-122">-Curve</span></span>
<span data-ttu-id="c321c-123">A tanúsítvány kulcsának elliptikus görbe nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c321c-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="c321c-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c321c-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c321c-125">P-256</span><span class="sxs-lookup"><span data-stu-id="c321c-125">P-256</span></span>
- <span data-ttu-id="c321c-126">P-384</span><span class="sxs-lookup"><span data-stu-id="c321c-126">P-384</span></span>
- <span data-ttu-id="c321c-127">P-521</span><span class="sxs-lookup"><span data-stu-id="c321c-127">P-521</span></span>
- <span data-ttu-id="c321c-128">P-256K</span><span class="sxs-lookup"><span data-stu-id="c321c-128">P-256K</span></span>
- <span data-ttu-id="c321c-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="c321c-129">SECP256K1</span></span>

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

### <span data-ttu-id="c321c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c321c-130">-DefaultProfile</span></span>
<span data-ttu-id="c321c-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c321c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c321c-132">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="c321c-132">-Disabled</span></span>
<span data-ttu-id="c321c-133">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="c321c-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="c321c-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="c321c-134">-DnsName</span></span>
<span data-ttu-id="c321c-135">A tanúsítványban lévő DNS-neveket adja meg.</span><span class="sxs-lookup"><span data-stu-id="c321c-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="c321c-136">A tárgyas helyettesítő nevek (SANs) DNS-névként adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="c321c-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="c321c-137">-EKU</span><span class="sxs-lookup"><span data-stu-id="c321c-137">-Ekus</span></span>
<span data-ttu-id="c321c-138">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="c321c-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="c321c-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="c321c-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="c321c-140">Itt adhatja meg, hogy hány nap elteltével kezdődik az automatikus értesítési folyamat.</span><span class="sxs-lookup"><span data-stu-id="c321c-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="c321c-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="c321c-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="c321c-142">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="c321c-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="c321c-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="c321c-143">-IssuerName</span></span>
<span data-ttu-id="c321c-144">A tanúsítványt megadó tanúsítvány nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="c321c-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="c321c-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="c321c-145">-KeyNotExportable</span></span>
<span data-ttu-id="c321c-146">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="c321c-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="c321c-147">-Méret</span><span class="sxs-lookup"><span data-stu-id="c321c-147">-KeySize</span></span>
<span data-ttu-id="c321c-148">A tanúsítvány kulcsának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c321c-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="c321c-149">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c321c-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c321c-150">2048</span><span class="sxs-lookup"><span data-stu-id="c321c-150">2048</span></span>
- <span data-ttu-id="c321c-151">3072</span><span class="sxs-lookup"><span data-stu-id="c321c-151">3072</span></span>
- <span data-ttu-id="c321c-152">4096</span><span class="sxs-lookup"><span data-stu-id="c321c-152">4096</span></span>
- <span data-ttu-id="c321c-153">256</span><span class="sxs-lookup"><span data-stu-id="c321c-153">256</span></span>
- <span data-ttu-id="c321c-154">384</span><span class="sxs-lookup"><span data-stu-id="c321c-154">384</span></span>
- <span data-ttu-id="c321c-155">521</span><span class="sxs-lookup"><span data-stu-id="c321c-155">521</span></span>

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

### <span data-ttu-id="c321c-156">-Típus</span><span class="sxs-lookup"><span data-stu-id="c321c-156">-KeyType</span></span>
<span data-ttu-id="c321c-157">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="c321c-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="c321c-158">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c321c-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c321c-159">RSA</span><span class="sxs-lookup"><span data-stu-id="c321c-159">RSA</span></span>
- <span data-ttu-id="c321c-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="c321c-160">RSA-HSM</span></span>
- <span data-ttu-id="c321c-161">EK</span><span class="sxs-lookup"><span data-stu-id="c321c-161">EC</span></span>
- <span data-ttu-id="c321c-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="c321c-162">EC-HSM</span></span>

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

### <span data-ttu-id="c321c-163">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="c321c-163">-KeyUsage</span></span>
<span data-ttu-id="c321c-164">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="c321c-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="c321c-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="c321c-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="c321c-166">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="c321c-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="c321c-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="c321c-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="c321c-168">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="c321c-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="c321c-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="c321c-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="c321c-170">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="c321c-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="c321c-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="c321c-171">-SecretContentType</span></span>
<span data-ttu-id="c321c-172">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c321c-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="c321c-173">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c321c-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c321c-174">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="c321c-174">application/x-pkcs12</span></span>
- <span data-ttu-id="c321c-175">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="c321c-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="c321c-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="c321c-176">-SubjectName</span></span>
<span data-ttu-id="c321c-177">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c321c-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="c321c-178">Ha a paraméterben pontosvesszőt (,) vagy pontot (.) kell használnia `SubjectName` , a tulajdonságot idézőjelek közé kell tenni.</span><span class="sxs-lookup"><span data-stu-id="c321c-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="c321c-179">Használhatja például az O = "contoso, Ltd." függvényt.</span><span class="sxs-lookup"><span data-stu-id="c321c-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="c321c-180">a szervezet neve mezőben.</span><span class="sxs-lookup"><span data-stu-id="c321c-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="c321c-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="c321c-181">-ValidityInMonths</span></span>
<span data-ttu-id="c321c-182">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="c321c-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="c321c-183">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c321c-183">-Confirm</span></span>
<span data-ttu-id="c321c-184">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c321c-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c321c-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c321c-185">-WhatIf</span></span>
<span data-ttu-id="c321c-186">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c321c-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c321c-187">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c321c-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c321c-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c321c-188">CommonParameters</span></span>
<span data-ttu-id="c321c-189">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c321c-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c321c-190">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c321c-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c321c-191">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c321c-191">INPUTS</span></span>

### <span data-ttu-id="c321c-192">System. String</span><span class="sxs-lookup"><span data-stu-id="c321c-192">System.String</span></span>

### <span data-ttu-id="c321c-193">System. Collections. Generic. list ' 1 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c321c-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c321c-194">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c321c-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c321c-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c321c-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c321c-196">System. Collections. Generic. list ' 1 [[System. Security. kriptográfia. X509Certificates. X509KeyUsageFlags, System. Security. kriptográfia. X509Certificates, Version = 4.2.1.0, Culture = semleges, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="c321c-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="c321c-197">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c321c-197">OUTPUTS</span></span>

### <span data-ttu-id="c321c-198">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="c321c-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="c321c-199">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c321c-199">NOTES</span></span>

## <span data-ttu-id="c321c-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c321c-200">RELATED LINKS</span></span>

[<span data-ttu-id="c321c-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c321c-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="c321c-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="c321c-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

