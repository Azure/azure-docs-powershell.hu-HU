---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 5a6b88ce85b8b9296d9666955a93d1240b631634
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012542"
---
# <span data-ttu-id="8d871-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8d871-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="8d871-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d871-102">SYNOPSIS</span></span>
<span data-ttu-id="8d871-103">A tanúsítvány házirendjét hozza létre vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="8d871-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="8d871-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d871-104">SYNTAX</span></span>

### <span data-ttu-id="8d871-105">ExpandedRenewPercentage (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d871-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d871-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="8d871-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d871-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="8d871-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d871-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d871-108">DESCRIPTION</span></span>
<span data-ttu-id="8d871-109">A **set-AzKeyVaultCertificatePolicy** parancsmag a tanúsítványok házirendjét létrehozhatja vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="8d871-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="8d871-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8d871-110">EXAMPLES</span></span>

### <span data-ttu-id="8d871-111">Példa 1: tanúsítvány-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="8d871-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="8d871-112">Ez a parancs beállítja a TestCert01-tanúsítvány házirendjét a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="8d871-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="8d871-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d871-113">PARAMETERS</span></span>

### <span data-ttu-id="8d871-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="8d871-114">-CertificateTransparency</span></span>
<span data-ttu-id="8d871-115">Azt jelzi, hogy engedélyezve van-e a hitelességi bizonyítvány vagy a tanúsítvány áttetszősége. Ha nincs megadva, az alapértelmezett érték az "igaz"</span><span class="sxs-lookup"><span data-stu-id="8d871-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="8d871-116">-CertificateType</span></span>
<span data-ttu-id="8d871-117">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d871-117">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-118">-Görbe</span><span class="sxs-lookup"><span data-stu-id="8d871-118">-Curve</span></span>
<span data-ttu-id="8d871-119">A tanúsítvány kulcsának elliptikus görbe nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d871-119">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="8d871-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8d871-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8d871-121">P-256</span><span class="sxs-lookup"><span data-stu-id="8d871-121">P-256</span></span>
- <span data-ttu-id="8d871-122">P-384</span><span class="sxs-lookup"><span data-stu-id="8d871-122">P-384</span></span>
- <span data-ttu-id="8d871-123">P-521</span><span class="sxs-lookup"><span data-stu-id="8d871-123">P-521</span></span>
- <span data-ttu-id="8d871-124">P-256K</span><span class="sxs-lookup"><span data-stu-id="8d871-124">P-256K</span></span>
- <span data-ttu-id="8d871-125">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="8d871-125">SECP256K1</span></span>

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

### <span data-ttu-id="8d871-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d871-126">-DefaultProfile</span></span>
<span data-ttu-id="8d871-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8d871-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d871-128">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="8d871-128">-Disabled</span></span>
<span data-ttu-id="8d871-129">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="8d871-129">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-130">-DnsName</span><span class="sxs-lookup"><span data-stu-id="8d871-130">-DnsName</span></span>
<span data-ttu-id="8d871-131">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d871-131">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-132">-EKU</span><span class="sxs-lookup"><span data-stu-id="8d871-132">-Ekus</span></span>
<span data-ttu-id="8d871-133">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d871-133">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-134">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="8d871-134">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="8d871-135">A lejárat előtti napok számát adja meg az automatikus megújítás megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="8d871-135">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-136">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="8d871-136">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="8d871-137">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="8d871-137">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d871-138">-InputObject</span></span>
<span data-ttu-id="8d871-139">A tanúsítvány-házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d871-139">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-140">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="8d871-140">-IssuerName</span></span>
<span data-ttu-id="8d871-141">Annak a tanúsítványnak a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d871-141">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-142">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="8d871-142">-KeyNotExportable</span></span>
<span data-ttu-id="8d871-143">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="8d871-143">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-144">-Méret</span><span class="sxs-lookup"><span data-stu-id="8d871-144">-KeySize</span></span>
<span data-ttu-id="8d871-145">A tanúsítvány kulcsának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d871-145">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="8d871-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8d871-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8d871-147">2048</span><span class="sxs-lookup"><span data-stu-id="8d871-147">2048</span></span>
- <span data-ttu-id="8d871-148">3072</span><span class="sxs-lookup"><span data-stu-id="8d871-148">3072</span></span>
- <span data-ttu-id="8d871-149">4096</span><span class="sxs-lookup"><span data-stu-id="8d871-149">4096</span></span>
- <span data-ttu-id="8d871-150">256</span><span class="sxs-lookup"><span data-stu-id="8d871-150">256</span></span>
- <span data-ttu-id="8d871-151">384</span><span class="sxs-lookup"><span data-stu-id="8d871-151">384</span></span>
- <span data-ttu-id="8d871-152">521</span><span class="sxs-lookup"><span data-stu-id="8d871-152">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: 2048
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-153">-Típus</span><span class="sxs-lookup"><span data-stu-id="8d871-153">-KeyType</span></span>
<span data-ttu-id="8d871-154">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="8d871-154">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="8d871-155">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8d871-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8d871-156">RSA</span><span class="sxs-lookup"><span data-stu-id="8d871-156">RSA</span></span>
- <span data-ttu-id="8d871-157">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="8d871-157">RSA-HSM</span></span>
- <span data-ttu-id="8d871-158">EK</span><span class="sxs-lookup"><span data-stu-id="8d871-158">EC</span></span>
- <span data-ttu-id="8d871-159">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="8d871-159">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-160">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="8d871-160">-KeyUsage</span></span>
<span data-ttu-id="8d871-161">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d871-161">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-162">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d871-162">-Name</span></span>
<span data-ttu-id="8d871-163">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d871-163">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-164">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d871-164">-PassThru</span></span>
<span data-ttu-id="8d871-165">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="8d871-165">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8d871-166">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8d871-166">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-167">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="8d871-167">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="8d871-168">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="8d871-168">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-169">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="8d871-169">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="8d871-170">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="8d871-170">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-171">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="8d871-171">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="8d871-172">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="8d871-172">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-173">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="8d871-173">-SecretContentType</span></span>
<span data-ttu-id="8d871-174">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d871-174">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="8d871-175">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8d871-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8d871-176">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="8d871-176">application/x-pkcs12</span></span>
- <span data-ttu-id="8d871-177">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="8d871-177">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-178">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="8d871-178">-SubjectName</span></span>
<span data-ttu-id="8d871-179">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d871-179">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-180">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="8d871-180">-ValidityInMonths</span></span>
<span data-ttu-id="8d871-181">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="8d871-181">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-182">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8d871-182">-VaultName</span></span>
<span data-ttu-id="8d871-183">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d871-183">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d871-184">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d871-184">-Confirm</span></span>
<span data-ttu-id="8d871-185">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d871-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d871-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d871-186">-WhatIf</span></span>
<span data-ttu-id="8d871-187">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d871-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d871-188">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d871-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d871-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d871-189">CommonParameters</span></span>
<span data-ttu-id="8d871-190">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d871-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d871-191">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d871-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d871-192">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d871-192">INPUTS</span></span>

### <span data-ttu-id="8d871-193">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="8d871-193">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="8d871-194">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d871-194">OUTPUTS</span></span>

### <span data-ttu-id="8d871-195">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="8d871-195">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="8d871-196">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d871-196">NOTES</span></span>

## <span data-ttu-id="8d871-197">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d871-197">RELATED LINKS</span></span>

[<span data-ttu-id="8d871-198">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8d871-198">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="8d871-199">Új – AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8d871-199">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

