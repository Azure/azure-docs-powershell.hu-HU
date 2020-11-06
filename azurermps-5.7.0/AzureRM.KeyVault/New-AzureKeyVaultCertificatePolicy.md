---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: caa0961c1b7aebd5fd2f9883831d733a0fa69f1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502568"
---
# <span data-ttu-id="3431c-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3431c-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3431c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3431c-102">SYNOPSIS</span></span>
<span data-ttu-id="3431c-103">A memória tanúsítvány házirend-objektumát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="3431c-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3431c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3431c-104">SYNTAX</span></span>

### <span data-ttu-id="3431c-105">SubjectName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3431c-105">SubjectName (Default)</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled] [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3431c-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="3431c-106">DNSNames</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3431c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3431c-107">DESCRIPTION</span></span>
<span data-ttu-id="3431c-108">A **New-AzureKeyVaultCertificatePolicy** parancsmag létrehoz egy memória-alapú tanúsítvány házirend-objektumot az Azure Key Vault-hoz.</span><span class="sxs-lookup"><span data-stu-id="3431c-108">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="3431c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3431c-109">EXAMPLES</span></span>

### <span data-ttu-id="3431c-110">Példa 1: tanúsítvány-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="3431c-110">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="3431c-111">Ez a parancs hat hónapig érvényes tanúsítvány-házirendet hoz létre, és a kulcsot újra felhasználja a tanúsítvány megújításához.</span><span class="sxs-lookup"><span data-stu-id="3431c-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="3431c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3431c-112">PARAMETERS</span></span>

### <span data-ttu-id="3431c-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="3431c-113">-CertificateType</span></span>
<span data-ttu-id="3431c-114">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3431c-114">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3431c-115">-DefaultProfile</span></span>
<span data-ttu-id="3431c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3431c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3431c-117">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="3431c-117">-Disabled</span></span>
<span data-ttu-id="3431c-118">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="3431c-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431c-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="3431c-119">-DnsName</span></span>
<span data-ttu-id="3431c-120">A tanúsítványban lévő DNS-neveket adja meg.</span><span class="sxs-lookup"><span data-stu-id="3431c-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="3431c-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="3431c-121">-Ekus</span></span>
<span data-ttu-id="3431c-122">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="3431c-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="3431c-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="3431c-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="3431c-124">Itt adhatja meg, hogy hány nap elteltével kezdődik az automatikus értesítési folyamat.</span><span class="sxs-lookup"><span data-stu-id="3431c-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431c-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="3431c-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="3431c-126">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="3431c-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431c-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="3431c-127">-IssuerName</span></span>
<span data-ttu-id="3431c-128">A tanúsítványt megadó tanúsítvány nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="3431c-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="3431c-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="3431c-129">-KeyNotExportable</span></span>
<span data-ttu-id="3431c-130">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="3431c-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431c-131">-Típus</span><span class="sxs-lookup"><span data-stu-id="3431c-131">-KeyType</span></span>
<span data-ttu-id="3431c-132">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="3431c-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="3431c-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3431c-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3431c-134">RSA</span><span class="sxs-lookup"><span data-stu-id="3431c-134">RSA</span></span>
- <span data-ttu-id="3431c-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="3431c-135">RSA-HSM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431c-136">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="3431c-136">-KeyUsage</span></span>
<span data-ttu-id="3431c-137">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="3431c-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="3431c-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="3431c-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="3431c-139">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="3431c-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431c-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="3431c-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="3431c-141">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="3431c-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431c-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="3431c-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="3431c-143">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="3431c-143">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431c-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="3431c-144">-SecretContentType</span></span>
<span data-ttu-id="3431c-145">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3431c-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="3431c-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3431c-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3431c-147">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="3431c-147">application/x-pkcs12</span></span>
- <span data-ttu-id="3431c-148">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="3431c-148">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431c-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="3431c-149">-SubjectName</span></span>
<span data-ttu-id="3431c-150">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3431c-150">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431c-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="3431c-151">-ValidityInMonths</span></span>
<span data-ttu-id="3431c-152">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="3431c-152">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431c-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3431c-153">-Confirm</span></span>
<span data-ttu-id="3431c-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3431c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3431c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3431c-155">-WhatIf</span></span>
<span data-ttu-id="3431c-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3431c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3431c-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3431c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3431c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3431c-158">CommonParameters</span></span>
<span data-ttu-id="3431c-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3431c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3431c-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3431c-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3431c-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3431c-161">INPUTS</span></span>

### <span data-ttu-id="3431c-162">Nincs</span><span class="sxs-lookup"><span data-stu-id="3431c-162">None</span></span>
<span data-ttu-id="3431c-163">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3431c-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3431c-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3431c-164">OUTPUTS</span></span>

### <span data-ttu-id="3431c-165">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="3431c-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3431c-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3431c-166">NOTES</span></span>

## <span data-ttu-id="3431c-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3431c-167">RELATED LINKS</span></span>

[<span data-ttu-id="3431c-168">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3431c-168">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="3431c-169">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3431c-169">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

