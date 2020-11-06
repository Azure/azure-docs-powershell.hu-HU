---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 94f8b6e136925956faf4402b583d80f6a675cca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504107"
---
# <span data-ttu-id="52168-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="52168-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="52168-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52168-102">SYNOPSIS</span></span>
<span data-ttu-id="52168-103">A tanúsítvány házirendjét hozza létre vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="52168-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52168-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52168-104">SYNTAX</span></span>

### <span data-ttu-id="52168-105">Kibontva (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52168-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52168-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="52168-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52168-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="52168-107">DESCRIPTION</span></span>
<span data-ttu-id="52168-108">A **set-AzureKeyVaultCertificatePolicy** parancsmag a tanúsítványok házirendjét létrehozhatja vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="52168-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="52168-109">Példák</span><span class="sxs-lookup"><span data-stu-id="52168-109">EXAMPLES</span></span>

### <span data-ttu-id="52168-110">Példa 1: tanúsítvány-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="52168-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="52168-111">Ez a parancs beállítja a TestCert01-tanúsítvány házirendjét a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="52168-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="52168-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52168-112">PARAMETERS</span></span>

### <span data-ttu-id="52168-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="52168-113">-CertificatePolicy</span></span>
<span data-ttu-id="52168-114">A tanúsítvány-házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="52168-114">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="52168-115">-CertificateType</span></span>
<span data-ttu-id="52168-116">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="52168-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-117">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="52168-117">-Disabled</span></span>
<span data-ttu-id="52168-118">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="52168-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-119">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="52168-119">-DnsNames</span></span>
<span data-ttu-id="52168-120">A tanúsítványban lévő DNS-neveket adja meg.</span><span class="sxs-lookup"><span data-stu-id="52168-120">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="52168-121">-Ekus</span></span>
<span data-ttu-id="52168-122">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="52168-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="52168-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="52168-124">Itt adhatja meg, hogy hány nap elteltével kezdődik az automatikus értesítési folyamat.</span><span class="sxs-lookup"><span data-stu-id="52168-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="52168-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="52168-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="52168-126">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="52168-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="52168-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="52168-127">-IssuerName</span></span>
<span data-ttu-id="52168-128">Annak a tanúsítványnak a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52168-128">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="52168-129">-KeyNotExportable</span></span>
<span data-ttu-id="52168-130">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="52168-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-131">-Típus</span><span class="sxs-lookup"><span data-stu-id="52168-131">-KeyType</span></span>
<span data-ttu-id="52168-132">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="52168-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="52168-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="52168-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52168-134">RSA</span><span class="sxs-lookup"><span data-stu-id="52168-134">RSA</span></span>
- <span data-ttu-id="52168-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="52168-135">RSA-HSM</span></span>

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

### <span data-ttu-id="52168-136">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="52168-136">-KeyUsage</span></span>
<span data-ttu-id="52168-137">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="52168-137">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="52168-138">-Name</span></span>
<span data-ttu-id="52168-139">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52168-139">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52168-140">-PassThru</span></span>
<span data-ttu-id="52168-141">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="52168-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52168-142">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="52168-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52168-143">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="52168-143">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="52168-144">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="52168-144">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-145">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="52168-145">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="52168-146">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="52168-146">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-147">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="52168-147">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="52168-148">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="52168-148">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-149">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="52168-149">-SecretContentType</span></span>
<span data-ttu-id="52168-150">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="52168-150">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="52168-151">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="52168-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52168-152">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="52168-152">application/x-pkcs12</span></span>
- <span data-ttu-id="52168-153">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="52168-153">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-154">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="52168-154">-SubjectName</span></span>
<span data-ttu-id="52168-155">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52168-155">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-156">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="52168-156">-ValidityInMonths</span></span>
<span data-ttu-id="52168-157">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="52168-157">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="52168-158">-VaultName</span></span>
<span data-ttu-id="52168-159">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="52168-159">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52168-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="52168-160">-Confirm</span></span>
<span data-ttu-id="52168-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="52168-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52168-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52168-162">-WhatIf</span></span>
<span data-ttu-id="52168-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="52168-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52168-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52168-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52168-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52168-165">-DefaultProfile</span></span>
<span data-ttu-id="52168-166">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52168-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52168-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52168-167">CommonParameters</span></span>
<span data-ttu-id="52168-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52168-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52168-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52168-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52168-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52168-170">INPUTS</span></span>

## <span data-ttu-id="52168-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52168-171">OUTPUTS</span></span>

### <span data-ttu-id="52168-172">Microsoft. Azure. Command. KeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="52168-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="52168-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52168-173">NOTES</span></span>

## <span data-ttu-id="52168-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52168-174">RELATED LINKS</span></span>

[<span data-ttu-id="52168-175">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="52168-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="52168-176">Új – AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="52168-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

