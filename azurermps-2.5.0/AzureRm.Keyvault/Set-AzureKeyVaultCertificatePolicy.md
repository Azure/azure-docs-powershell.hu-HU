---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 7a9356952f2ea8b4113f5df0fe364e9647e2c733
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849649"
---
# <span data-ttu-id="df6fc-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="df6fc-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="df6fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="df6fc-103">A tanúsítvány házirendjét hozza létre vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="df6fc-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df6fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df6fc-104">SYNTAX</span></span>

### <span data-ttu-id="df6fc-105">Kibontva (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df6fc-105">Expanded (Default)</span></span>
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

### <span data-ttu-id="df6fc-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="df6fc-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df6fc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="df6fc-107">DESCRIPTION</span></span>
<span data-ttu-id="df6fc-108">A **set-AzureKeyVaultCertificatePolicy** parancsmag a tanúsítványok házirendjét létrehozhatja vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="df6fc-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="df6fc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="df6fc-109">EXAMPLES</span></span>

### <span data-ttu-id="df6fc-110">Példa 1: tanúsítvány-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="df6fc-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="df6fc-111">Ez a parancs beállítja a TestCert01-tanúsítvány házirendjét a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="df6fc-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="df6fc-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df6fc-112">PARAMETERS</span></span>

### <span data-ttu-id="df6fc-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="df6fc-113">-CertificatePolicy</span></span>
<span data-ttu-id="df6fc-114">A tanúsítvány-házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="df6fc-114">Specifies the certificate policy.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="df6fc-115">-CertificateType</span></span>
<span data-ttu-id="df6fc-116">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="df6fc-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df6fc-117">-DefaultProfile</span></span>
<span data-ttu-id="df6fc-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="df6fc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df6fc-119">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="df6fc-119">-Disabled</span></span>
<span data-ttu-id="df6fc-120">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="df6fc-120">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="df6fc-121">-DnsNames</span></span>
<span data-ttu-id="df6fc-122">A tanúsítványban lévő DNS-neveket adja meg.</span><span class="sxs-lookup"><span data-stu-id="df6fc-122">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="df6fc-123">-EKU</span><span class="sxs-lookup"><span data-stu-id="df6fc-123">-Ekus</span></span>
<span data-ttu-id="df6fc-124">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="df6fc-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="df6fc-125">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="df6fc-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="df6fc-126">Itt adhatja meg, hogy hány nap elteltével kezdődik az automatikus értesítési folyamat.</span><span class="sxs-lookup"><span data-stu-id="df6fc-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="df6fc-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="df6fc-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="df6fc-128">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="df6fc-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="df6fc-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="df6fc-129">-IssuerName</span></span>
<span data-ttu-id="df6fc-130">Annak a tanúsítványnak a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df6fc-130">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-131">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="df6fc-131">-KeyNotExportable</span></span>
<span data-ttu-id="df6fc-132">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="df6fc-132">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-133">-Típus</span><span class="sxs-lookup"><span data-stu-id="df6fc-133">-KeyType</span></span>
<span data-ttu-id="df6fc-134">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="df6fc-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="df6fc-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="df6fc-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="df6fc-136">RSA</span><span class="sxs-lookup"><span data-stu-id="df6fc-136">RSA</span></span>
- <span data-ttu-id="df6fc-137">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="df6fc-137">RSA-HSM</span></span>

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

### <span data-ttu-id="df6fc-138">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="df6fc-138">-KeyUsage</span></span>
<span data-ttu-id="df6fc-139">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="df6fc-139">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="df6fc-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df6fc-140">-Name</span></span>
<span data-ttu-id="df6fc-141">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df6fc-141">Specifies the name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df6fc-142">-PassThru</span></span>
<span data-ttu-id="df6fc-143">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="df6fc-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="df6fc-144">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="df6fc-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="df6fc-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="df6fc-146">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="df6fc-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="df6fc-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="df6fc-148">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="df6fc-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-149">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="df6fc-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="df6fc-150">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="df6fc-150">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="df6fc-151">-SecretContentType</span></span>
<span data-ttu-id="df6fc-152">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="df6fc-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="df6fc-153">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="df6fc-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="df6fc-154">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="df6fc-154">application/x-pkcs12</span></span>
- <span data-ttu-id="df6fc-155">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="df6fc-155">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="df6fc-156">-SubjectName</span></span>
<span data-ttu-id="df6fc-157">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df6fc-157">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="df6fc-158">-ValidityInMonths</span></span>
<span data-ttu-id="df6fc-159">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="df6fc-159">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-160">-VaultName</span><span class="sxs-lookup"><span data-stu-id="df6fc-160">-VaultName</span></span>
<span data-ttu-id="df6fc-161">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df6fc-161">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="df6fc-162">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df6fc-162">-Confirm</span></span>
<span data-ttu-id="df6fc-163">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df6fc-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df6fc-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df6fc-164">-WhatIf</span></span>
<span data-ttu-id="df6fc-165">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df6fc-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df6fc-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df6fc-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df6fc-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6fc-167">CommonParameters</span></span>
<span data-ttu-id="df6fc-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df6fc-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6fc-169">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df6fc-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6fc-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df6fc-170">INPUTS</span></span>

## <span data-ttu-id="df6fc-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df6fc-171">OUTPUTS</span></span>

### <span data-ttu-id="df6fc-172">Microsoft. Azure. Command. KeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="df6fc-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="df6fc-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df6fc-173">NOTES</span></span>

## <span data-ttu-id="df6fc-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df6fc-174">RELATED LINKS</span></span>

[<span data-ttu-id="df6fc-175">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="df6fc-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="df6fc-176">Új – AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="df6fc-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

