---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 963a7005e95941a644b35a57f80b558f02e2d6a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466376"
---
# <span data-ttu-id="11235-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="11235-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="11235-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11235-102">SYNOPSIS</span></span>
<span data-ttu-id="11235-103">Létrehozza vagy frissíti egy tanúsítvány házirendét egy kulcstárolóban.</span><span class="sxs-lookup"><span data-stu-id="11235-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="11235-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11235-104">SYNTAX</span></span>

### <span data-ttu-id="11235-105">ExpandedRenewPercentage (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11235-105">ExpandedRenewPercentage (Default)</span></span>
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

### <span data-ttu-id="11235-106">Érték szerint</span><span class="sxs-lookup"><span data-stu-id="11235-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11235-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="11235-107">ExpandedRenewNumber</span></span>
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

## <span data-ttu-id="11235-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11235-108">DESCRIPTION</span></span>
<span data-ttu-id="11235-109">A **Set-AzKeyVaultCertificatePolicy** parancsmag létrehozza vagy frissíti a tanúsítvány házirendet egy kulcstárolóban.</span><span class="sxs-lookup"><span data-stu-id="11235-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="11235-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11235-110">EXAMPLES</span></span>

### <span data-ttu-id="11235-111">1. példa: Tanúsítvány-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="11235-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="11235-112">Ez a parancs beállítja a TestCert01 tanúsítvány házirendet a ContosoKV01 kulcstárolóban.</span><span class="sxs-lookup"><span data-stu-id="11235-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="11235-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11235-113">PARAMETERS</span></span>

### <span data-ttu-id="11235-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="11235-114">-CertificateTransparency</span></span>
<span data-ttu-id="11235-115">Azt jelzi, hogy engedélyezve van-e a tanúsítvány áttetszőség ehhez a tanúsítványhoz/kibocsátóhoz; ha nincs megadva, az alapértelmezett érték "igaz".</span><span class="sxs-lookup"><span data-stu-id="11235-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="11235-116">`-IssuerName` tulajdonság beállításakor meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="11235-116">`-IssuerName` needs to be specified when setting this property.</span></span>

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

### <span data-ttu-id="11235-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="11235-117">-CertificateType</span></span>
<span data-ttu-id="11235-118">A kibocsátó tanúsítványának típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="11235-118">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="11235-119">-Curve</span><span class="sxs-lookup"><span data-stu-id="11235-119">-Curve</span></span>
<span data-ttu-id="11235-120">A tanúsítvány kulcsának három ponttal megadott görbeneve.</span><span class="sxs-lookup"><span data-stu-id="11235-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="11235-121">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="11235-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11235-122">P-256</span><span class="sxs-lookup"><span data-stu-id="11235-122">P-256</span></span>
- <span data-ttu-id="11235-123">P-384</span><span class="sxs-lookup"><span data-stu-id="11235-123">P-384</span></span>
- <span data-ttu-id="11235-124">P-521</span><span class="sxs-lookup"><span data-stu-id="11235-124">P-521</span></span>
- <span data-ttu-id="11235-125">P-256K</span><span class="sxs-lookup"><span data-stu-id="11235-125">P-256K</span></span>
- <span data-ttu-id="11235-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="11235-126">SECP256K1</span></span>

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

### <span data-ttu-id="11235-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11235-127">-DefaultProfile</span></span>
<span data-ttu-id="11235-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="11235-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11235-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="11235-129">-Disabled</span></span>
<span data-ttu-id="11235-130">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="11235-130">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="11235-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="11235-131">-DnsName</span></span>
<span data-ttu-id="11235-132">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11235-132">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="11235-133">-Ekus</span><span class="sxs-lookup"><span data-stu-id="11235-133">-Ekus</span></span>
<span data-ttu-id="11235-134">A tanúsítványban megadott továbbfejlesztett kulcshasználatot (EKUs) adja meg.</span><span class="sxs-lookup"><span data-stu-id="11235-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="11235-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="11235-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="11235-136">Azt adja meg, hogy hány nappal a lejárat előtt induljon el az automatikus megújítás.</span><span class="sxs-lookup"><span data-stu-id="11235-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="11235-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="11235-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="11235-138">Azt adja meg, hogy az értesítés automatikus eljárása hány százaléka után indul el.</span><span class="sxs-lookup"><span data-stu-id="11235-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="11235-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11235-139">-InputObject</span></span>
<span data-ttu-id="11235-140">A tanúsítvány-házirendet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="11235-140">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="11235-141">-KibocsátóNeve</span><span class="sxs-lookup"><span data-stu-id="11235-141">-IssuerName</span></span>
<span data-ttu-id="11235-142">A tanúsítvány kibocsátójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11235-142">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="11235-143">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="11235-143">-KeyNotExportable</span></span>
<span data-ttu-id="11235-144">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="11235-144">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="11235-145">-KeySize</span><span class="sxs-lookup"><span data-stu-id="11235-145">-KeySize</span></span>
<span data-ttu-id="11235-146">A tanúsítvány kulcsméretét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="11235-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="11235-147">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="11235-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11235-148">2048</span><span class="sxs-lookup"><span data-stu-id="11235-148">2048</span></span>
- <span data-ttu-id="11235-149">3072</span><span class="sxs-lookup"><span data-stu-id="11235-149">3072</span></span>
- <span data-ttu-id="11235-150">4096</span><span class="sxs-lookup"><span data-stu-id="11235-150">4096</span></span>
- <span data-ttu-id="11235-151">256</span><span class="sxs-lookup"><span data-stu-id="11235-151">256</span></span>
- <span data-ttu-id="11235-152">384</span><span class="sxs-lookup"><span data-stu-id="11235-152">384</span></span>
- <span data-ttu-id="11235-153">521</span><span class="sxs-lookup"><span data-stu-id="11235-153">521</span></span>

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

### <span data-ttu-id="11235-154">-KeyType</span><span class="sxs-lookup"><span data-stu-id="11235-154">-KeyType</span></span>
<span data-ttu-id="11235-155">A tanúsítványt visszaő kulcs típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="11235-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="11235-156">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="11235-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11235-157">RSA</span><span class="sxs-lookup"><span data-stu-id="11235-157">RSA</span></span>
- <span data-ttu-id="11235-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="11235-158">RSA-HSM</span></span>
- <span data-ttu-id="11235-159">EC</span><span class="sxs-lookup"><span data-stu-id="11235-159">EC</span></span>
- <span data-ttu-id="11235-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="11235-160">EC-HSM</span></span>

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

### <span data-ttu-id="11235-161">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="11235-161">-KeyUsage</span></span>
<span data-ttu-id="11235-162">A tanúsítvány kulcshasználati kulcsát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="11235-162">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="11235-163">-Name</span><span class="sxs-lookup"><span data-stu-id="11235-163">-Name</span></span>
<span data-ttu-id="11235-164">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11235-164">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="11235-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11235-165">-PassThru</span></span>
<span data-ttu-id="11235-166">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="11235-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="11235-167">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="11235-167">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="11235-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="11235-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="11235-169">Azt adja meg, hogy hány nappal a lejárat előtt induljon el a tanúsítvány automatikus megújítási folyamata.</span><span class="sxs-lookup"><span data-stu-id="11235-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="11235-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="11235-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="11235-171">Meghatározza, hogy a tanúsítvány automatikus megújítási eljárása hány százaléka után indul el.</span><span class="sxs-lookup"><span data-stu-id="11235-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="11235-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="11235-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="11235-173">Azt jelzi, hogy a tanúsítvány újra felhasználja a kulcsot a megújítás során.</span><span class="sxs-lookup"><span data-stu-id="11235-173">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="11235-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="11235-174">-SecretContentType</span></span>
<span data-ttu-id="11235-175">Az új kulcstár-titkos kulcs tartalomtípusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="11235-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="11235-176">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="11235-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11235-177">alkalmazás/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="11235-177">application/x-pkcs12</span></span>
- <span data-ttu-id="11235-178">application/x-pem-file</span><span class="sxs-lookup"><span data-stu-id="11235-178">application/x-pem-file</span></span>

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

### <span data-ttu-id="11235-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="11235-179">-SubjectName</span></span>
<span data-ttu-id="11235-180">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11235-180">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="11235-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="11235-181">-ValidityInMonths</span></span>
<span data-ttu-id="11235-182">Azt adja meg, hogy a tanúsítvány hány hónapig érvényes.</span><span class="sxs-lookup"><span data-stu-id="11235-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="11235-183">-VaultName</span><span class="sxs-lookup"><span data-stu-id="11235-183">-VaultName</span></span>
<span data-ttu-id="11235-184">Egy kulcstár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11235-184">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="11235-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11235-185">-Confirm</span></span>
<span data-ttu-id="11235-186">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="11235-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11235-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11235-187">-WhatIf</span></span>
<span data-ttu-id="11235-188">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="11235-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11235-189">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11235-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11235-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11235-190">CommonParameters</span></span>
<span data-ttu-id="11235-191">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11235-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11235-192">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11235-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11235-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11235-193">INPUTS</span></span>

### <span data-ttu-id="11235-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="11235-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="11235-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11235-195">OUTPUTS</span></span>

### <span data-ttu-id="11235-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="11235-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="11235-197">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11235-197">NOTES</span></span>

## <span data-ttu-id="11235-198">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11235-198">RELATED LINKS</span></span>

[<span data-ttu-id="11235-199">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="11235-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="11235-200">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="11235-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

