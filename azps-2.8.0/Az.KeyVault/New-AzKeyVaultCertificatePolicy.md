---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 262c539d9ff97983494de0951c9a5d47510b0d28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666185"
---
# <span data-ttu-id="a1a2a-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a1a2a-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="a1a2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a2a-103">A memória tanúsítvány házirend-objektumát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="a1a2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1a2a-104">SYNTAX</span></span>

### <span data-ttu-id="a1a2a-105">SubjectName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1a2a-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1a2a-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="a1a2a-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1a2a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1a2a-107">DESCRIPTION</span></span>
<span data-ttu-id="a1a2a-108">A **New-AzKeyVaultCertificatePolicy** parancsmag létrehoz egy memória-alapú tanúsítvány házirend-objektumot az Azure Key Vault-hoz.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="a1a2a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a1a2a-109">EXAMPLES</span></span>

### <span data-ttu-id="a1a2a-110">Példa 1: tanúsítvány-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="a1a2a-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
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

<span data-ttu-id="a1a2a-111">Ez a parancs hat hónapig érvényes tanúsítvány-házirendet hoz létre, és a kulcsot újra felhasználja a tanúsítvány megújításához.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="a1a2a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1a2a-112">PARAMETERS</span></span>

### <span data-ttu-id="a1a2a-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="a1a2a-113">-CertificateType</span></span>
<span data-ttu-id="a1a2a-114">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-114">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="a1a2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a2a-115">-DefaultProfile</span></span>
<span data-ttu-id="a1a2a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a1a2a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1a2a-117">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="a1a2a-117">-Disabled</span></span>
<span data-ttu-id="a1a2a-118">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-118">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="a1a2a-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="a1a2a-119">-DnsName</span></span>
<span data-ttu-id="a1a2a-120">A tanúsítványban lévő DNS-neveket adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="a1a2a-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="a1a2a-121">-Ekus</span></span>
<span data-ttu-id="a1a2a-122">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="a1a2a-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="a1a2a-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="a1a2a-124">Itt adhatja meg, hogy hány nap elteltével kezdődik az automatikus értesítési folyamat.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="a1a2a-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="a1a2a-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="a1a2a-126">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="a1a2a-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="a1a2a-127">-IssuerName</span></span>
<span data-ttu-id="a1a2a-128">A tanúsítványt megadó tanúsítvány nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="a1a2a-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="a1a2a-129">-KeyNotExportable</span></span>
<span data-ttu-id="a1a2a-130">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-130">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="a1a2a-131">-Méret</span><span class="sxs-lookup"><span data-stu-id="a1a2a-131">-KeySize</span></span>
<span data-ttu-id="a1a2a-132">A tanúsítvány kulcsának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-132">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="a1a2a-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a1a2a-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a1a2a-134">2048</span><span class="sxs-lookup"><span data-stu-id="a1a2a-134">2048</span></span>
- <span data-ttu-id="a1a2a-135">3072</span><span class="sxs-lookup"><span data-stu-id="a1a2a-135">3072</span></span>
- <span data-ttu-id="a1a2a-136">4096</span><span class="sxs-lookup"><span data-stu-id="a1a2a-136">4096</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a2a-137">-Típus</span><span class="sxs-lookup"><span data-stu-id="a1a2a-137">-KeyType</span></span>
<span data-ttu-id="a1a2a-138">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-138">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="a1a2a-139">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a1a2a-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a1a2a-140">RSA</span><span class="sxs-lookup"><span data-stu-id="a1a2a-140">RSA</span></span>
- <span data-ttu-id="a1a2a-141">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="a1a2a-141">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a2a-142">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="a1a2a-142">-KeyUsage</span></span>
<span data-ttu-id="a1a2a-143">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-143">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="a1a2a-144">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="a1a2a-144">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="a1a2a-145">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-145">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="a1a2a-146">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="a1a2a-146">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="a1a2a-147">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-147">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="a1a2a-148">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="a1a2a-148">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="a1a2a-149">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-149">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="a1a2a-150">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="a1a2a-150">-SecretContentType</span></span>
<span data-ttu-id="a1a2a-151">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-151">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="a1a2a-152">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a1a2a-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a1a2a-153">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="a1a2a-153">application/x-pkcs12</span></span>
- <span data-ttu-id="a1a2a-154">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="a1a2a-154">application/x-pem-file</span></span>

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

### <span data-ttu-id="a1a2a-155">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="a1a2a-155">-SubjectName</span></span>
<span data-ttu-id="a1a2a-156">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-156">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="a1a2a-157">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="a1a2a-157">-ValidityInMonths</span></span>
<span data-ttu-id="a1a2a-158">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-158">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="a1a2a-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a1a2a-159">-Confirm</span></span>
<span data-ttu-id="a1a2a-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1a2a-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1a2a-161">-WhatIf</span></span>
<span data-ttu-id="a1a2a-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1a2a-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1a2a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a2a-164">CommonParameters</span></span>
<span data-ttu-id="a1a2a-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1a2a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a2a-166">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1a2a-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a2a-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1a2a-167">INPUTS</span></span>

### <span data-ttu-id="a1a2a-168">System. String</span><span class="sxs-lookup"><span data-stu-id="a1a2a-168">System.String</span></span>

### <span data-ttu-id="a1a2a-169">System. Collections. Generic. list ' 1 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a1a2a-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a1a2a-170">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a1a2a-170">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a1a2a-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a1a2a-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a1a2a-172">System. Collections. Generic. list ' 1 [[System. Security. kriptográfia. X509Certificates. X509KeyUsageFlags, System. Security. kriptográfia. X509Certificates, Version = 4.2.1.0, Culture = semleges, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="a1a2a-172">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="a1a2a-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1a2a-173">OUTPUTS</span></span>

### <span data-ttu-id="a1a2a-174">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="a1a2a-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="a1a2a-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1a2a-175">NOTES</span></span>

## <span data-ttu-id="a1a2a-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1a2a-176">RELATED LINKS</span></span>

[<span data-ttu-id="a1a2a-177">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a1a2a-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="a1a2a-178">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a1a2a-178">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

