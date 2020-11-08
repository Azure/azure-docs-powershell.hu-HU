---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: b0d690358fb5598b1a88ecb7fe169c8ef3d2718f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014881"
---
# <span data-ttu-id="7c3d6-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="7c3d6-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="7c3d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c3d6-102">SYNOPSIS</span></span>
<span data-ttu-id="7c3d6-103">A memória tanúsítvány házirend-objektumát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="7c3d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c3d6-104">SYNTAX</span></span>

### <span data-ttu-id="7c3d6-105">SubjectName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c3d6-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="7c3d6-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="7c3d6-106">DNSNames</span></span>
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

## <span data-ttu-id="7c3d6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c3d6-107">DESCRIPTION</span></span>
<span data-ttu-id="7c3d6-108">A **New-AzKeyVaultCertificatePolicy** parancsmag létrehoz egy memória-alapú tanúsítvány házirend-objektumot az Azure Key Vault-hoz.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="7c3d6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7c3d6-109">EXAMPLES</span></span>

### <span data-ttu-id="7c3d6-110">Példa 1: tanúsítvány-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="7c3d6-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="7c3d6-111">Ez a parancs hat hónapig érvényes tanúsítvány-házirendet hoz létre, és a kulcsot újra felhasználja a tanúsítvány megújításához.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="7c3d6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c3d6-112">PARAMETERS</span></span>

### <span data-ttu-id="7c3d6-113">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="7c3d6-113">-CertificateTransparency</span></span>
<span data-ttu-id="7c3d6-114">Azt jelzi, hogy engedélyezve van-e a hitelességi bizonyítvány vagy a tanúsítvány áttetszősége. Ha nincs megadva, az alapértelmezett érték az "igaz"</span><span class="sxs-lookup"><span data-stu-id="7c3d6-114">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="7c3d6-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="7c3d6-115">-CertificateType</span></span>
<span data-ttu-id="7c3d6-116">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-116">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="7c3d6-117">-Görbe</span><span class="sxs-lookup"><span data-stu-id="7c3d6-117">-Curve</span></span>
<span data-ttu-id="7c3d6-118">A tanúsítvány kulcsának elliptikus görbe nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-118">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="7c3d6-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7c3d6-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c3d6-120">P-256</span><span class="sxs-lookup"><span data-stu-id="7c3d6-120">P-256</span></span>
- <span data-ttu-id="7c3d6-121">P-384</span><span class="sxs-lookup"><span data-stu-id="7c3d6-121">P-384</span></span>
- <span data-ttu-id="7c3d6-122">P-521</span><span class="sxs-lookup"><span data-stu-id="7c3d6-122">P-521</span></span>
- <span data-ttu-id="7c3d6-123">P-256K</span><span class="sxs-lookup"><span data-stu-id="7c3d6-123">P-256K</span></span>
- <span data-ttu-id="7c3d6-124">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="7c3d6-124">SECP256K1</span></span>

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

### <span data-ttu-id="7c3d6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c3d6-125">-DefaultProfile</span></span>
<span data-ttu-id="7c3d6-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7c3d6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c3d6-127">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="7c3d6-127">-Disabled</span></span>
<span data-ttu-id="7c3d6-128">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-128">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="7c3d6-129">-DnsName</span><span class="sxs-lookup"><span data-stu-id="7c3d6-129">-DnsName</span></span>
<span data-ttu-id="7c3d6-130">A tanúsítványban lévő DNS-neveket adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-130">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="7c3d6-131">-EKU</span><span class="sxs-lookup"><span data-stu-id="7c3d6-131">-Ekus</span></span>
<span data-ttu-id="7c3d6-132">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-132">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="7c3d6-133">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="7c3d6-133">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="7c3d6-134">Itt adhatja meg, hogy hány nap elteltével kezdődik az automatikus értesítési folyamat.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-134">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="7c3d6-135">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="7c3d6-135">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="7c3d6-136">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-136">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="7c3d6-137">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="7c3d6-137">-IssuerName</span></span>
<span data-ttu-id="7c3d6-138">A tanúsítványt megadó tanúsítvány nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-138">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="7c3d6-139">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="7c3d6-139">-KeyNotExportable</span></span>
<span data-ttu-id="7c3d6-140">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-140">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="7c3d6-141">-Méret</span><span class="sxs-lookup"><span data-stu-id="7c3d6-141">-KeySize</span></span>
<span data-ttu-id="7c3d6-142">A tanúsítvány kulcsának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-142">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="7c3d6-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7c3d6-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c3d6-144">2048</span><span class="sxs-lookup"><span data-stu-id="7c3d6-144">2048</span></span>
- <span data-ttu-id="7c3d6-145">3072</span><span class="sxs-lookup"><span data-stu-id="7c3d6-145">3072</span></span>
- <span data-ttu-id="7c3d6-146">4096</span><span class="sxs-lookup"><span data-stu-id="7c3d6-146">4096</span></span>
- <span data-ttu-id="7c3d6-147">256</span><span class="sxs-lookup"><span data-stu-id="7c3d6-147">256</span></span>
- <span data-ttu-id="7c3d6-148">384</span><span class="sxs-lookup"><span data-stu-id="7c3d6-148">384</span></span>
- <span data-ttu-id="7c3d6-149">521</span><span class="sxs-lookup"><span data-stu-id="7c3d6-149">521</span></span>

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

### <span data-ttu-id="7c3d6-150">-Típus</span><span class="sxs-lookup"><span data-stu-id="7c3d6-150">-KeyType</span></span>
<span data-ttu-id="7c3d6-151">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-151">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="7c3d6-152">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7c3d6-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c3d6-153">RSA</span><span class="sxs-lookup"><span data-stu-id="7c3d6-153">RSA</span></span>
- <span data-ttu-id="7c3d6-154">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="7c3d6-154">RSA-HSM</span></span>
- <span data-ttu-id="7c3d6-155">EK</span><span class="sxs-lookup"><span data-stu-id="7c3d6-155">EC</span></span>
- <span data-ttu-id="7c3d6-156">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="7c3d6-156">EC-HSM</span></span>

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

### <span data-ttu-id="7c3d6-157">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="7c3d6-157">-KeyUsage</span></span>
<span data-ttu-id="7c3d6-158">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-158">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="7c3d6-159">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="7c3d6-159">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="7c3d6-160">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-160">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="7c3d6-161">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="7c3d6-161">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="7c3d6-162">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-162">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="7c3d6-163">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="7c3d6-163">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="7c3d6-164">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-164">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="7c3d6-165">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="7c3d6-165">-SecretContentType</span></span>
<span data-ttu-id="7c3d6-166">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-166">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="7c3d6-167">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7c3d6-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c3d6-168">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="7c3d6-168">application/x-pkcs12</span></span>
- <span data-ttu-id="7c3d6-169">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="7c3d6-169">application/x-pem-file</span></span>

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

### <span data-ttu-id="7c3d6-170">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="7c3d6-170">-SubjectName</span></span>
<span data-ttu-id="7c3d6-171">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-171">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="7c3d6-172">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="7c3d6-172">-ValidityInMonths</span></span>
<span data-ttu-id="7c3d6-173">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-173">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="7c3d6-174">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7c3d6-174">-Confirm</span></span>
<span data-ttu-id="7c3d6-175">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c3d6-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c3d6-176">-WhatIf</span></span>
<span data-ttu-id="7c3d6-177">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c3d6-178">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c3d6-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c3d6-179">CommonParameters</span></span>
<span data-ttu-id="7c3d6-180">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c3d6-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c3d6-181">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c3d6-182">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c3d6-182">INPUTS</span></span>

### <span data-ttu-id="7c3d6-183">System. String</span><span class="sxs-lookup"><span data-stu-id="7c3d6-183">System.String</span></span>

### <span data-ttu-id="7c3d6-184">System. Collections. Generic. list ' 1 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7c3d6-184">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7c3d6-185">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7c3d6-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7c3d6-186">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7c3d6-186">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7c3d6-187">System. Collections. Generic. list ' 1 [[System. Security. kriptográfia. X509Certificates. X509KeyUsageFlags, System. Security. kriptográfia. X509Certificates, Version = 4.2.1.0, Culture = semleges, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="7c3d6-187">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="7c3d6-188">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c3d6-188">OUTPUTS</span></span>

### <span data-ttu-id="7c3d6-189">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="7c3d6-189">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="7c3d6-190">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c3d6-190">NOTES</span></span>

## <span data-ttu-id="7c3d6-191">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c3d6-191">RELATED LINKS</span></span>

[<span data-ttu-id="7c3d6-192">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="7c3d6-192">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="7c3d6-193">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="7c3d6-193">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

