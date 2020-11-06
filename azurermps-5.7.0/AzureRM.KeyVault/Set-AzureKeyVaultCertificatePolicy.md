---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: e960aa211b53c79087e67e2bd86504e597a718d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504547"
---
# <span data-ttu-id="d9a0a-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d9a0a-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d9a0a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a0a-103">A tanúsítvány házirendjét hozza létre vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9a0a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9a0a-104">SYNTAX</span></span>

### <span data-ttu-id="d9a0a-105">ExpandedRenewPercentage (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d9a0a-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9a0a-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="d9a0a-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9a0a-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="d9a0a-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9a0a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9a0a-108">DESCRIPTION</span></span>
<span data-ttu-id="d9a0a-109">A **set-AzureKeyVaultCertificatePolicy** parancsmag a tanúsítványok házirendjét létrehozhatja vagy frissíti egy kulcs-boltozatban.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="d9a0a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d9a0a-110">EXAMPLES</span></span>

### <span data-ttu-id="d9a0a-111">Példa 1: tanúsítvány-házirend beállítása</span><span class="sxs-lookup"><span data-stu-id="d9a0a-111">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="d9a0a-112">Ez a parancs beállítja a TestCert01-tanúsítvány házirendjét a ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="d9a0a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9a0a-113">PARAMETERS</span></span>

### <span data-ttu-id="d9a0a-114">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="d9a0a-114">-CertificateType</span></span>
<span data-ttu-id="d9a0a-115">A leválasztó tanúsítvány típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-115">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a0a-116">-DefaultProfile</span></span>
<span data-ttu-id="d9a0a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d9a0a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9a0a-118">-Disabled (letiltva)</span><span class="sxs-lookup"><span data-stu-id="d9a0a-118">-Disabled</span></span>
<span data-ttu-id="d9a0a-119">Azt jelzi, hogy a tanúsítvány-házirend le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-119">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-120">-DnsName</span><span class="sxs-lookup"><span data-stu-id="d9a0a-120">-DnsName</span></span>
<span data-ttu-id="d9a0a-121">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-121">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-122">-EKU</span><span class="sxs-lookup"><span data-stu-id="d9a0a-122">-Ekus</span></span>
<span data-ttu-id="d9a0a-123">A tanúsítvány kibővített kulcshasználati funkcióit (EKU) adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-123">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-124">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="d9a0a-124">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="d9a0a-125">A lejárat előtti napok számát adja meg az automatikus megújítás megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-125">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="d9a0a-126">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="d9a0a-126">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="d9a0a-127">Annak az élettartamnak a százalékát adja meg, amely után az értesítés automatikus folyamata elkezdődik.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-127">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="d9a0a-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9a0a-128">-InputObject</span></span>
<span data-ttu-id="d9a0a-129">A tanúsítvány-házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-129">Specifies the certificate policy.</span></span>

```yaml
Type: PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-130">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="d9a0a-130">-IssuerName</span></span>
<span data-ttu-id="d9a0a-131">Annak a tanúsítványnak a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-131">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-132">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="d9a0a-132">-KeyNotExportable</span></span>
<span data-ttu-id="d9a0a-133">Azt jelzi, hogy a kulcs nem exportálható.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-133">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-134">-Típus</span><span class="sxs-lookup"><span data-stu-id="d9a0a-134">-KeyType</span></span>
<span data-ttu-id="d9a0a-135">Annak a kulcsnak a típusát adja meg, amely támogatja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-135">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="d9a0a-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d9a0a-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9a0a-137">RSA</span><span class="sxs-lookup"><span data-stu-id="d9a0a-137">RSA</span></span>
- <span data-ttu-id="d9a0a-138">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="d9a0a-138">RSA-HSM</span></span>

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

### <span data-ttu-id="d9a0a-139">-Kulcshasználat</span><span class="sxs-lookup"><span data-stu-id="d9a0a-139">-KeyUsage</span></span>
<span data-ttu-id="d9a0a-140">A hitelességi bizonyítványban használt kulcshasználat adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-140">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d9a0a-141">-Name</span></span>
<span data-ttu-id="d9a0a-142">A tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-142">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="d9a0a-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9a0a-143">-PassThru</span></span>
<span data-ttu-id="d9a0a-144">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d9a0a-145">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d9a0a-146">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="d9a0a-146">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="d9a0a-147">A lejárat előtti napok számát adja meg, miután megkezdődik az automatikus tanúsítvány-megújítás folyamata.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-147">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-148">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="d9a0a-148">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="d9a0a-149">Annak az élettartamnak a százalékát adja meg, amely után az automatikus folyamat megújítása megkezdődik.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-149">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-150">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="d9a0a-150">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="d9a0a-151">Azt jelzi, hogy a tanúsítvány a megújítás során újra felhasználta a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-151">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-152">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="d9a0a-152">-SecretContentType</span></span>
<span data-ttu-id="d9a0a-153">Az új kulcs boltozat titkának tartalomtípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-153">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="d9a0a-154">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d9a0a-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9a0a-155">Application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="d9a0a-155">application/x-pkcs12</span></span>
- <span data-ttu-id="d9a0a-156">Application/x-PEM-fájl</span><span class="sxs-lookup"><span data-stu-id="d9a0a-156">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-157">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="d9a0a-157">-SubjectName</span></span>
<span data-ttu-id="d9a0a-158">A tanúsítvány tulajdonosának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-158">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-159">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="d9a0a-159">-ValidityInMonths</span></span>
<span data-ttu-id="d9a0a-160">Azt adja meg, hogy hány hónapig érvényes a tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-160">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a0a-161">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d9a0a-161">-VaultName</span></span>
<span data-ttu-id="d9a0a-162">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-162">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="d9a0a-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d9a0a-163">-Confirm</span></span>
<span data-ttu-id="d9a0a-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9a0a-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9a0a-165">-WhatIf</span></span>
<span data-ttu-id="d9a0a-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9a0a-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9a0a-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a0a-168">CommonParameters</span></span>
<span data-ttu-id="d9a0a-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9a0a-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a0a-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9a0a-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a0a-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9a0a-171">INPUTS</span></span>

### <span data-ttu-id="d9a0a-172">Nincs</span><span class="sxs-lookup"><span data-stu-id="d9a0a-172">None</span></span>
<span data-ttu-id="d9a0a-173">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9a0a-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9a0a-174">OUTPUTS</span></span>

### <span data-ttu-id="d9a0a-175">Microsoft. Azure. Command. PSKeyVaultCertificatePolicy. models.</span><span class="sxs-lookup"><span data-stu-id="d9a0a-175">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d9a0a-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9a0a-176">NOTES</span></span>

## <span data-ttu-id="d9a0a-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9a0a-177">RELATED LINKS</span></span>

[<span data-ttu-id="d9a0a-178">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d9a0a-178">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="d9a0a-179">Új – AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d9a0a-179">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

