---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: b10dd0e034db53af35c930ce1c4588dee2576c75
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848846"
---
# <span data-ttu-id="825c2-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="825c2-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="825c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="825c2-102">SYNOPSIS</span></span>
<span data-ttu-id="825c2-103">A memória tanúsítvány házirend-objektumát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="825c2-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="825c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="825c2-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="825c2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="825c2-105">DESCRIPTION</span></span>
<span data-ttu-id="825c2-106">A **New-AzureKeyVaultCertificatePolicy** parancsmag létrehoz egy memória-alapú tanúsítvány házirend-objektumot az Azure Key Vault-hoz.</span><span class="sxs-lookup"><span data-stu-id="825c2-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="825c2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="825c2-107">EXAMPLES</span></span>

### <span data-ttu-id="825c2-108">Példa 1: tanúsítvány-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="825c2-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="825c2-109">Ez a parancs hat hónapig érvényes tanúsítvány-házirendet hoz létre, és a kulcsot újra felhasználja a tanúsítvány megújításához.</span><span class="sxs-lookup"><span data-stu-id="825c2-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="825c2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="825c2-110">PARAMETERS</span></span>

### <span data-ttu-id="825c2-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="825c2-111">-CertificateType</span></span>
<span data-ttu-id="825c2-112">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="825c2-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="825c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="825c2-113">-DefaultProfile</span></span>
<span data-ttu-id="825c2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="825c2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="825c2-115">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="825c2-115">-Disabled</span></span>
<span data-ttu-id="825c2-116">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="825c2-116">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="825c2-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="825c2-117">-DnsNames</span></span>
<span data-ttu-id="825c2-118">A tanúsítványban lévő DNS-neveket adja meg.</span><span class="sxs-lookup"><span data-stu-id="825c2-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="825c2-119">-EKU</span><span class="sxs-lookup"><span data-stu-id="825c2-119">-Ekus</span></span>
<span data-ttu-id="825c2-120">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="825c2-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="825c2-121">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="825c2-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="825c2-122">Itt adhatja meg, hogy hány nap elteltével kezdődik az automatikus értesítési folyamat.</span><span class="sxs-lookup"><span data-stu-id="825c2-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="825c2-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="825c2-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="825c2-124">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="825c2-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="825c2-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="825c2-125">-IssuerName</span></span>
<span data-ttu-id="825c2-126">A tanúsítványt megadó tanúsítvány nevének megadása.</span><span class="sxs-lookup"><span data-stu-id="825c2-126">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="825c2-127">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="825c2-127">-KeyNotExportable</span></span>
<span data-ttu-id="825c2-128">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="825c2-128">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="825c2-129">-Típus</span><span class="sxs-lookup"><span data-stu-id="825c2-129">-KeyType</span></span>
<span data-ttu-id="825c2-130">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="825c2-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="825c2-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="825c2-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="825c2-132">RSA</span><span class="sxs-lookup"><span data-stu-id="825c2-132">RSA</span></span>
- <span data-ttu-id="825c2-133">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="825c2-133">RSA-HSM</span></span>

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

### <span data-ttu-id="825c2-134">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="825c2-134">-KeyUsage</span></span>
<span data-ttu-id="825c2-135">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="825c2-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="825c2-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="825c2-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="825c2-137">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="825c2-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="825c2-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="825c2-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="825c2-139">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="825c2-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="825c2-140">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="825c2-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="825c2-141">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="825c2-141">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="825c2-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="825c2-142">-SecretContentType</span></span>
<span data-ttu-id="825c2-143">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="825c2-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="825c2-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="825c2-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="825c2-145">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="825c2-145">application/x-pkcs12</span></span>
- <span data-ttu-id="825c2-146">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="825c2-146">application/x-pem-file</span></span>

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

### <span data-ttu-id="825c2-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="825c2-147">-SubjectName</span></span>
<span data-ttu-id="825c2-148">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="825c2-148">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="825c2-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="825c2-149">-ValidityInMonths</span></span>
<span data-ttu-id="825c2-150">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="825c2-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="825c2-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="825c2-151">-Confirm</span></span>
<span data-ttu-id="825c2-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="825c2-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="825c2-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="825c2-153">-WhatIf</span></span>
<span data-ttu-id="825c2-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="825c2-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="825c2-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="825c2-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="825c2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="825c2-156">CommonParameters</span></span>
<span data-ttu-id="825c2-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="825c2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="825c2-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="825c2-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="825c2-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="825c2-159">INPUTS</span></span>

## <span data-ttu-id="825c2-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="825c2-160">OUTPUTS</span></span>

### <span data-ttu-id="825c2-161">Microsoft. Azure. Command. KeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="825c2-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="825c2-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="825c2-162">NOTES</span></span>

## <span data-ttu-id="825c2-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="825c2-163">RELATED LINKS</span></span>

[<span data-ttu-id="825c2-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="825c2-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="825c2-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="825c2-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

