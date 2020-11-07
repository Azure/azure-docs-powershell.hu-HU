---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 83eea8c8a030c5d22368bc0ede42c71e92df14a2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842129"
---
# <span data-ttu-id="abd77-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="abd77-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="abd77-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abd77-102">SYNOPSIS</span></span>
<span data-ttu-id="abd77-103">A memória tanúsítvány házirend-objektumát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="abd77-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="abd77-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abd77-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abd77-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="abd77-105">DESCRIPTION</span></span>
<span data-ttu-id="abd77-106">A **New-AzKeyVaultCertificatePolicy** parancsmag létrehoz egy memória-alapú tanúsítvány házirend-objektumot az Azure Key Vault-hoz.</span><span class="sxs-lookup"><span data-stu-id="abd77-106">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="abd77-107">Példák</span><span class="sxs-lookup"><span data-stu-id="abd77-107">EXAMPLES</span></span>

### <span data-ttu-id="abd77-108">Példa 1: tanúsítvány-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="abd77-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="abd77-109">Ez a parancs hat hónapig érvényes tanúsítvány-házirendet hoz létre, és a kulcsot újra felhasználja a tanúsítvány megújításához.</span><span class="sxs-lookup"><span data-stu-id="abd77-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="abd77-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abd77-110">PARAMETERS</span></span>

### <span data-ttu-id="abd77-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="abd77-111">-CertificateType</span></span>
<span data-ttu-id="abd77-112">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="abd77-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="abd77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd77-113">-DefaultProfile</span></span>
<span data-ttu-id="abd77-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="abd77-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd77-115">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="abd77-115">-Disabled</span></span>
<span data-ttu-id="abd77-116">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="abd77-116">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="abd77-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="abd77-117">-DnsNames</span></span>
<span data-ttu-id="abd77-118">A tanúsítványban lévő DNS-neveket adja meg.</span><span class="sxs-lookup"><span data-stu-id="abd77-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="abd77-119">-EKU</span><span class="sxs-lookup"><span data-stu-id="abd77-119">-Ekus</span></span>
<span data-ttu-id="abd77-120">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="abd77-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="abd77-121">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="abd77-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="abd77-122">Itt adhatja meg, hogy hány nap elteltével kezdődik az automatikus értesítési folyamat.</span><span class="sxs-lookup"><span data-stu-id="abd77-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="abd77-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="abd77-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="abd77-124">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="abd77-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="abd77-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="abd77-125">-IssuerName</span></span>
<span data-ttu-id="abd77-126">A tanúsítványt megadó tanúsítvány nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="abd77-126">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abd77-127">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="abd77-127">-KeyNotExportable</span></span>
<span data-ttu-id="abd77-128">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="abd77-128">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="abd77-129">-Típus</span><span class="sxs-lookup"><span data-stu-id="abd77-129">-KeyType</span></span>
<span data-ttu-id="abd77-130">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="abd77-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="abd77-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="abd77-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="abd77-132">RSA</span><span class="sxs-lookup"><span data-stu-id="abd77-132">RSA</span></span>
- <span data-ttu-id="abd77-133">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="abd77-133">RSA-HSM</span></span>

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

### <span data-ttu-id="abd77-134">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="abd77-134">-KeyUsage</span></span>
<span data-ttu-id="abd77-135">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="abd77-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="abd77-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="abd77-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="abd77-137">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="abd77-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="abd77-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="abd77-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="abd77-139">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="abd77-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="abd77-140">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="abd77-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="abd77-141">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="abd77-141">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="abd77-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="abd77-142">-SecretContentType</span></span>
<span data-ttu-id="abd77-143">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="abd77-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="abd77-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="abd77-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="abd77-145">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="abd77-145">application/x-pkcs12</span></span>
- <span data-ttu-id="abd77-146">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="abd77-146">application/x-pem-file</span></span>

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

### <span data-ttu-id="abd77-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="abd77-147">-SubjectName</span></span>
<span data-ttu-id="abd77-148">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abd77-148">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="abd77-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="abd77-149">-ValidityInMonths</span></span>
<span data-ttu-id="abd77-150">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="abd77-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="abd77-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="abd77-151">-Confirm</span></span>
<span data-ttu-id="abd77-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abd77-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abd77-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abd77-153">-WhatIf</span></span>
<span data-ttu-id="abd77-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="abd77-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abd77-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abd77-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abd77-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd77-156">CommonParameters</span></span>
<span data-ttu-id="abd77-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abd77-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd77-158">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abd77-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd77-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abd77-159">INPUTS</span></span>

### <span data-ttu-id="abd77-160">Nincs</span><span class="sxs-lookup"><span data-stu-id="abd77-160">None</span></span>
<span data-ttu-id="abd77-161">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="abd77-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="abd77-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abd77-162">OUTPUTS</span></span>

### <span data-ttu-id="abd77-163">Microsoft. Azure. Command. KeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="abd77-163">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="abd77-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abd77-164">NOTES</span></span>

## <span data-ttu-id="abd77-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abd77-165">RELATED LINKS</span></span>

[<span data-ttu-id="abd77-166">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="abd77-166">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="abd77-167">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="abd77-167">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

