---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 271da96d18628c899b10ac17185fd4c3a921d8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493677"
---
# <span data-ttu-id="38ec9-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="38ec9-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="38ec9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="38ec9-103">A tanúsítvány házirendjét hozza létre vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="38ec9-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38ec9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38ec9-104">SYNTAX</span></span>

### <span data-ttu-id="38ec9-105">ExpandedRenewPercentage (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38ec9-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38ec9-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="38ec9-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38ec9-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="38ec9-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38ec9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="38ec9-108">DESCRIPTION</span></span>
<span data-ttu-id="38ec9-109">A **set-AzureKeyVaultCertificatePolicy** parancsmag a tanúsítványok házirendjét létrehozhatja vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="38ec9-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="38ec9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="38ec9-110">EXAMPLES</span></span>

### <span data-ttu-id="38ec9-111">Példa 1: tanúsítvány-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="38ec9-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="38ec9-112">Ez a parancs beállítja a TestCert01-tanúsítvány házirendjét a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="38ec9-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="38ec9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38ec9-113">PARAMETERS</span></span>

### <span data-ttu-id="38ec9-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="38ec9-114">-CertificateTransparency</span></span>
<span data-ttu-id="38ec9-115">Azt jelzi, hogy engedélyezve van-e a hitelességi bizonyítvány vagy a tanúsítvány áttetszősége. Ha nincs megadva, az alapértelmezett érték az "igaz"</span><span class="sxs-lookup"><span data-stu-id="38ec9-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="38ec9-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="38ec9-116">-CertificateType</span></span>
<span data-ttu-id="38ec9-117">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="38ec9-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="38ec9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ec9-118">-DefaultProfile</span></span>
<span data-ttu-id="38ec9-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="38ec9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ec9-120">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="38ec9-120">-Disabled</span></span>
<span data-ttu-id="38ec9-121">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="38ec9-121">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="38ec9-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="38ec9-122">-DnsName</span></span>
<span data-ttu-id="38ec9-123">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38ec9-123">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="38ec9-124">-EKU</span><span class="sxs-lookup"><span data-stu-id="38ec9-124">-Ekus</span></span>
<span data-ttu-id="38ec9-125">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="38ec9-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="38ec9-126">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="38ec9-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="38ec9-127">A lejárat előtti napok számát adja meg az automatikus megújítás megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="38ec9-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="38ec9-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="38ec9-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="38ec9-129">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="38ec9-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="38ec9-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38ec9-130">-InputObject</span></span>
<span data-ttu-id="38ec9-131">A tanúsítvány-házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="38ec9-131">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="38ec9-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="38ec9-132">-IssuerName</span></span>
<span data-ttu-id="38ec9-133">Annak a tanúsítványnak a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38ec9-133">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="38ec9-134">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="38ec9-134">-KeyNotExportable</span></span>
<span data-ttu-id="38ec9-135">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="38ec9-135">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="38ec9-136">-Típus</span><span class="sxs-lookup"><span data-stu-id="38ec9-136">-KeyType</span></span>
<span data-ttu-id="38ec9-137">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="38ec9-137">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="38ec9-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="38ec9-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38ec9-139">RSA</span><span class="sxs-lookup"><span data-stu-id="38ec9-139">RSA</span></span>
- <span data-ttu-id="38ec9-140">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="38ec9-140">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ec9-141">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="38ec9-141">-KeyUsage</span></span>
<span data-ttu-id="38ec9-142">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="38ec9-142">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="38ec9-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38ec9-143">-Name</span></span>
<span data-ttu-id="38ec9-144">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38ec9-144">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="38ec9-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38ec9-145">-PassThru</span></span>
<span data-ttu-id="38ec9-146">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="38ec9-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="38ec9-147">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="38ec9-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="38ec9-148">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="38ec9-148">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="38ec9-149">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="38ec9-149">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="38ec9-150">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="38ec9-150">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="38ec9-151">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="38ec9-151">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="38ec9-152">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="38ec9-152">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="38ec9-153">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="38ec9-153">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="38ec9-154">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="38ec9-154">-SecretContentType</span></span>
<span data-ttu-id="38ec9-155">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="38ec9-155">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="38ec9-156">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="38ec9-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38ec9-157">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="38ec9-157">application/x-pkcs12</span></span>
- <span data-ttu-id="38ec9-158">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="38ec9-158">application/x-pem-file</span></span>

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

### <span data-ttu-id="38ec9-159">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="38ec9-159">-SubjectName</span></span>
<span data-ttu-id="38ec9-160">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38ec9-160">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="38ec9-161">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="38ec9-161">-ValidityInMonths</span></span>
<span data-ttu-id="38ec9-162">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="38ec9-162">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="38ec9-163">-VaultName</span><span class="sxs-lookup"><span data-stu-id="38ec9-163">-VaultName</span></span>
<span data-ttu-id="38ec9-164">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38ec9-164">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="38ec9-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38ec9-165">-Confirm</span></span>
<span data-ttu-id="38ec9-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38ec9-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ec9-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ec9-167">-WhatIf</span></span>
<span data-ttu-id="38ec9-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="38ec9-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ec9-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38ec9-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ec9-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ec9-170">CommonParameters</span></span>
<span data-ttu-id="38ec9-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38ec9-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ec9-172">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38ec9-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ec9-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38ec9-173">INPUTS</span></span>

### <span data-ttu-id="38ec9-174">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="38ec9-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="38ec9-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38ec9-175">OUTPUTS</span></span>

### <span data-ttu-id="38ec9-176">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="38ec9-176">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="38ec9-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38ec9-177">NOTES</span></span>

## <span data-ttu-id="38ec9-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38ec9-178">RELATED LINKS</span></span>

[<span data-ttu-id="38ec9-179">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="38ec9-179">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="38ec9-180">Új – AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="38ec9-180">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

