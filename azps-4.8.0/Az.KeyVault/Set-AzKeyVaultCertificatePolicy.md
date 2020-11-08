---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 963a7005e95941a644b35a57f80b558f02e2d6a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181887"
---
# <span data-ttu-id="49a00-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="49a00-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="49a00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49a00-102">SYNOPSIS</span></span>
<span data-ttu-id="49a00-103">A tanúsítvány házirendjét hozza létre vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="49a00-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="49a00-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49a00-104">SYNTAX</span></span>

### <span data-ttu-id="49a00-105">ExpandedRenewPercentage (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49a00-105">ExpandedRenewPercentage (Default)</span></span>
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

### <span data-ttu-id="49a00-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="49a00-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49a00-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="49a00-107">ExpandedRenewNumber</span></span>
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

## <span data-ttu-id="49a00-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="49a00-108">DESCRIPTION</span></span>
<span data-ttu-id="49a00-109">A **set-AzKeyVaultCertificatePolicy** parancsmag a tanúsítványok házirendjét létrehozhatja vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="49a00-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="49a00-110">Példák</span><span class="sxs-lookup"><span data-stu-id="49a00-110">EXAMPLES</span></span>

### <span data-ttu-id="49a00-111">Példa 1: tanúsítvány-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="49a00-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="49a00-112">Ez a parancs beállítja a TestCert01-tanúsítvány házirendjét a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="49a00-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="49a00-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49a00-113">PARAMETERS</span></span>

### <span data-ttu-id="49a00-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="49a00-114">-CertificateTransparency</span></span>
<span data-ttu-id="49a00-115">Azt jelzi, hogy engedélyezve van-e a hitelességi bizonyítvány vagy a tanúsítvány áttetszősége. Ha nincs megadva, az alapértelmezett érték az "igaz".</span><span class="sxs-lookup"><span data-stu-id="49a00-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="49a00-116">`-IssuerName` a tulajdonság beállításakor szükséges megadni.</span><span class="sxs-lookup"><span data-stu-id="49a00-116">`-IssuerName` needs to be specified when setting this property.</span></span>

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

### <span data-ttu-id="49a00-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="49a00-117">-CertificateType</span></span>
<span data-ttu-id="49a00-118">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a00-118">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="49a00-119">-Görbe</span><span class="sxs-lookup"><span data-stu-id="49a00-119">-Curve</span></span>
<span data-ttu-id="49a00-120">A tanúsítvány kulcsának elliptikus görbe nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a00-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="49a00-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="49a00-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49a00-122">P-256</span><span class="sxs-lookup"><span data-stu-id="49a00-122">P-256</span></span>
- <span data-ttu-id="49a00-123">P-384</span><span class="sxs-lookup"><span data-stu-id="49a00-123">P-384</span></span>
- <span data-ttu-id="49a00-124">P-521</span><span class="sxs-lookup"><span data-stu-id="49a00-124">P-521</span></span>
- <span data-ttu-id="49a00-125">P-256K</span><span class="sxs-lookup"><span data-stu-id="49a00-125">P-256K</span></span>
- <span data-ttu-id="49a00-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="49a00-126">SECP256K1</span></span>

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

### <span data-ttu-id="49a00-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a00-127">-DefaultProfile</span></span>
<span data-ttu-id="49a00-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="49a00-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49a00-129">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="49a00-129">-Disabled</span></span>
<span data-ttu-id="49a00-130">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="49a00-130">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="49a00-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="49a00-131">-DnsName</span></span>
<span data-ttu-id="49a00-132">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a00-132">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="49a00-133">-EKU</span><span class="sxs-lookup"><span data-stu-id="49a00-133">-Ekus</span></span>
<span data-ttu-id="49a00-134">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a00-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="49a00-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="49a00-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="49a00-136">A lejárat előtti napok számát adja meg az automatikus megújítás megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="49a00-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="49a00-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="49a00-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="49a00-138">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="49a00-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="49a00-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49a00-139">-InputObject</span></span>
<span data-ttu-id="49a00-140">A tanúsítvány-házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a00-140">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="49a00-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="49a00-141">-IssuerName</span></span>
<span data-ttu-id="49a00-142">Annak a tanúsítványnak a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a00-142">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="49a00-143">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="49a00-143">-KeyNotExportable</span></span>
<span data-ttu-id="49a00-144">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="49a00-144">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="49a00-145">-Méret</span><span class="sxs-lookup"><span data-stu-id="49a00-145">-KeySize</span></span>
<span data-ttu-id="49a00-146">A tanúsítvány kulcsának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a00-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="49a00-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="49a00-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49a00-148">2048</span><span class="sxs-lookup"><span data-stu-id="49a00-148">2048</span></span>
- <span data-ttu-id="49a00-149">3072</span><span class="sxs-lookup"><span data-stu-id="49a00-149">3072</span></span>
- <span data-ttu-id="49a00-150">4096</span><span class="sxs-lookup"><span data-stu-id="49a00-150">4096</span></span>
- <span data-ttu-id="49a00-151">256</span><span class="sxs-lookup"><span data-stu-id="49a00-151">256</span></span>
- <span data-ttu-id="49a00-152">384</span><span class="sxs-lookup"><span data-stu-id="49a00-152">384</span></span>
- <span data-ttu-id="49a00-153">521</span><span class="sxs-lookup"><span data-stu-id="49a00-153">521</span></span>

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

### <span data-ttu-id="49a00-154">-Típus</span><span class="sxs-lookup"><span data-stu-id="49a00-154">-KeyType</span></span>
<span data-ttu-id="49a00-155">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="49a00-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="49a00-156">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="49a00-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49a00-157">RSA</span><span class="sxs-lookup"><span data-stu-id="49a00-157">RSA</span></span>
- <span data-ttu-id="49a00-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="49a00-158">RSA-HSM</span></span>
- <span data-ttu-id="49a00-159">EK</span><span class="sxs-lookup"><span data-stu-id="49a00-159">EC</span></span>
- <span data-ttu-id="49a00-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="49a00-160">EC-HSM</span></span>

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

### <span data-ttu-id="49a00-161">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="49a00-161">-KeyUsage</span></span>
<span data-ttu-id="49a00-162">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a00-162">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="49a00-163">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49a00-163">-Name</span></span>
<span data-ttu-id="49a00-164">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a00-164">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="49a00-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49a00-165">-PassThru</span></span>
<span data-ttu-id="49a00-166">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="49a00-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="49a00-167">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="49a00-167">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49a00-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="49a00-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="49a00-169">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="49a00-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="49a00-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="49a00-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="49a00-171">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="49a00-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="49a00-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="49a00-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="49a00-173">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="49a00-173">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="49a00-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="49a00-174">-SecretContentType</span></span>
<span data-ttu-id="49a00-175">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a00-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="49a00-176">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="49a00-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49a00-177">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="49a00-177">application/x-pkcs12</span></span>
- <span data-ttu-id="49a00-178">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="49a00-178">application/x-pem-file</span></span>

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

### <span data-ttu-id="49a00-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="49a00-179">-SubjectName</span></span>
<span data-ttu-id="49a00-180">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a00-180">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="49a00-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="49a00-181">-ValidityInMonths</span></span>
<span data-ttu-id="49a00-182">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="49a00-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="49a00-183">-VaultName</span><span class="sxs-lookup"><span data-stu-id="49a00-183">-VaultName</span></span>
<span data-ttu-id="49a00-184">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a00-184">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="49a00-185">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49a00-185">-Confirm</span></span>
<span data-ttu-id="49a00-186">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49a00-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49a00-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a00-187">-WhatIf</span></span>
<span data-ttu-id="49a00-188">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49a00-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a00-189">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49a00-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49a00-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a00-190">CommonParameters</span></span>
<span data-ttu-id="49a00-191">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49a00-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a00-192">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="49a00-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a00-193">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49a00-193">INPUTS</span></span>

### <span data-ttu-id="49a00-194">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="49a00-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="49a00-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49a00-195">OUTPUTS</span></span>

### <span data-ttu-id="49a00-196">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="49a00-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="49a00-197">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49a00-197">NOTES</span></span>

## <span data-ttu-id="49a00-198">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49a00-198">RELATED LINKS</span></span>

[<span data-ttu-id="49a00-199">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="49a00-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="49a00-200">Új – AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="49a00-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

