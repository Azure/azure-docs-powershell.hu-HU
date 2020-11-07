---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 160c98b141dbde36786404b58c694772dc86d323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843861"
---
# <span data-ttu-id="35c43-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="35c43-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="35c43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35c43-102">SYNOPSIS</span></span>
<span data-ttu-id="35c43-103">A tanúsítvány házirendjét hozza létre vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="35c43-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="35c43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35c43-104">SYNTAX</span></span>

### <span data-ttu-id="35c43-105">Kibontva (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="35c43-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35c43-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="35c43-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35c43-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="35c43-107">DESCRIPTION</span></span>
<span data-ttu-id="35c43-108">A **set-AzKeyVaultCertificatePolicy** parancsmag a tanúsítványok házirendjét létrehozhatja vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="35c43-108">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="35c43-109">Példák</span><span class="sxs-lookup"><span data-stu-id="35c43-109">EXAMPLES</span></span>

### <span data-ttu-id="35c43-110">Példa 1: tanúsítvány-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="35c43-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="35c43-111">Ez a parancs beállítja a TestCert01-tanúsítvány házirendjét a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="35c43-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="35c43-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35c43-112">PARAMETERS</span></span>

### <span data-ttu-id="35c43-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="35c43-113">-CertificatePolicy</span></span>
<span data-ttu-id="35c43-114">A tanúsítvány-házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="35c43-114">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="35c43-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="35c43-115">-CertificateType</span></span>
<span data-ttu-id="35c43-116">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="35c43-116">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="35c43-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c43-117">-DefaultProfile</span></span>
<span data-ttu-id="35c43-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="35c43-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35c43-119">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="35c43-119">-Disabled</span></span>
<span data-ttu-id="35c43-120">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="35c43-120">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="35c43-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="35c43-121">-DnsNames</span></span>
<span data-ttu-id="35c43-122">A tanúsítványban lévő DNS-neveket adja meg.</span><span class="sxs-lookup"><span data-stu-id="35c43-122">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="35c43-123">-EKU</span><span class="sxs-lookup"><span data-stu-id="35c43-123">-Ekus</span></span>
<span data-ttu-id="35c43-124">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="35c43-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="35c43-125">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="35c43-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="35c43-126">Itt adhatja meg, hogy hány nap elteltével kezdődik az automatikus értesítési folyamat.</span><span class="sxs-lookup"><span data-stu-id="35c43-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="35c43-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="35c43-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="35c43-128">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="35c43-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="35c43-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="35c43-129">-IssuerName</span></span>
<span data-ttu-id="35c43-130">Annak a tanúsítványnak a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35c43-130">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="35c43-131">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="35c43-131">-KeyNotExportable</span></span>
<span data-ttu-id="35c43-132">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="35c43-132">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="35c43-133">-Típus</span><span class="sxs-lookup"><span data-stu-id="35c43-133">-KeyType</span></span>
<span data-ttu-id="35c43-134">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="35c43-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="35c43-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="35c43-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35c43-136">RSA</span><span class="sxs-lookup"><span data-stu-id="35c43-136">RSA</span></span>
- <span data-ttu-id="35c43-137">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="35c43-137">RSA-HSM</span></span>

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

### <span data-ttu-id="35c43-138">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="35c43-138">-KeyUsage</span></span>
<span data-ttu-id="35c43-139">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="35c43-139">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="35c43-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="35c43-140">-Name</span></span>
<span data-ttu-id="35c43-141">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35c43-141">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="35c43-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35c43-142">-PassThru</span></span>
<span data-ttu-id="35c43-143">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="35c43-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="35c43-144">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="35c43-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="35c43-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="35c43-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="35c43-146">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="35c43-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="35c43-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="35c43-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="35c43-148">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="35c43-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="35c43-149">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="35c43-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="35c43-150">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="35c43-150">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="35c43-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="35c43-151">-SecretContentType</span></span>
<span data-ttu-id="35c43-152">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="35c43-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="35c43-153">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="35c43-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35c43-154">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="35c43-154">application/x-pkcs12</span></span>
- <span data-ttu-id="35c43-155">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="35c43-155">application/x-pem-file</span></span>

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

### <span data-ttu-id="35c43-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="35c43-156">-SubjectName</span></span>
<span data-ttu-id="35c43-157">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35c43-157">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="35c43-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="35c43-158">-ValidityInMonths</span></span>
<span data-ttu-id="35c43-159">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="35c43-159">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="35c43-160">-VaultName</span><span class="sxs-lookup"><span data-stu-id="35c43-160">-VaultName</span></span>
<span data-ttu-id="35c43-161">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35c43-161">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="35c43-162">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="35c43-162">-Confirm</span></span>
<span data-ttu-id="35c43-163">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="35c43-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35c43-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35c43-164">-WhatIf</span></span>
<span data-ttu-id="35c43-165">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="35c43-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35c43-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35c43-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35c43-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c43-167">CommonParameters</span></span>
<span data-ttu-id="35c43-168">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35c43-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c43-169">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35c43-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c43-170">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35c43-170">INPUTS</span></span>

### <span data-ttu-id="35c43-171">Nincs</span><span class="sxs-lookup"><span data-stu-id="35c43-171">None</span></span>
<span data-ttu-id="35c43-172">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="35c43-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="35c43-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35c43-173">OUTPUTS</span></span>

### <span data-ttu-id="35c43-174">Microsoft. Azure. Command. KeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="35c43-174">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="35c43-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35c43-175">NOTES</span></span>

## <span data-ttu-id="35c43-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35c43-176">RELATED LINKS</span></span>

[<span data-ttu-id="35c43-177">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="35c43-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="35c43-178">Új – AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="35c43-178">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

