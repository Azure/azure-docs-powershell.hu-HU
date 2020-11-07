---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: d4d7cb0a188b4c00c4ea0c07140b3360c98805aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678938"
---
# <span data-ttu-id="915e3-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="915e3-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="915e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="915e3-102">SYNOPSIS</span></span>
<span data-ttu-id="915e3-103">Hitelesítő adatok hozzáadása egy meglévő alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="915e3-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="915e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="915e3-104">SYNTAX</span></span>

### <span data-ttu-id="915e3-105">ApplicationObjectIdWithPasswordParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="915e3-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="915e3-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="915e3-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="915e3-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="915e3-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="915e3-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="915e3-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="915e3-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="915e3-109">DESCRIPTION</span></span>
<span data-ttu-id="915e3-110">Az New-AzureRmADAppCredential parancsmag használatával új hitelesítő adatokat vehet fel, illetve hitelesítő adatokat adhat meg az alkalmazásokhoz.</span><span class="sxs-lookup"><span data-stu-id="915e3-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="915e3-111">Az alkalmazás azonosítása az alkalmazásobjektum-azonosító vagy az alkalmazás azonosítójának megadásával történik.</span><span class="sxs-lookup"><span data-stu-id="915e3-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="915e3-112">Példák</span><span class="sxs-lookup"><span data-stu-id="915e3-112">EXAMPLES</span></span>

### <span data-ttu-id="915e3-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="915e3-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="915e3-114">Egy meglévő alkalmazáshoz új jelszavas hitelesítő adatok kerülnek.</span><span class="sxs-lookup"><span data-stu-id="915e3-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="915e3-115">Ebben a példában a megadott jelszót a program az alkalmazásobjektum-azonosító használatával veszi fel az alkalmazásba.</span><span class="sxs-lookup"><span data-stu-id="915e3-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="915e3-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="915e3-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="915e3-117">Egy meglévő alkalmazáshoz új kulcs-hitelesítő adatok kerülnek.</span><span class="sxs-lookup"><span data-stu-id="915e3-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="915e3-118">Ebben a példában a applicationId segítségével bekerül az alkalmazásba a megadott Base64 kódolt nyilvános X509-tanúsítvány ("SajátPr. cer").</span><span class="sxs-lookup"><span data-stu-id="915e3-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="915e3-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="915e3-119">Example 3</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="915e3-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="915e3-120">PARAMETERS</span></span>

### <span data-ttu-id="915e3-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="915e3-121">-ApplicationId</span></span>
<span data-ttu-id="915e3-122">Annak az alkalmazásnak az azonosítója, amelyhez a hitelesítő adatokat hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="915e3-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="915e3-123">-CertValue</span><span class="sxs-lookup"><span data-stu-id="915e3-123">-CertValue</span></span>
<span data-ttu-id="915e3-124">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="915e3-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="915e3-125">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="915e3-125">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="915e3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="915e3-126">-DefaultProfile</span></span>
<span data-ttu-id="915e3-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="915e3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="915e3-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="915e3-128">-EndDate</span></span>
<span data-ttu-id="915e3-129">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="915e3-129">The effective end date of the credential usage.</span></span>
<span data-ttu-id="915e3-130">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="915e3-130">The default end date value is one year from today.</span></span> <span data-ttu-id="915e3-131">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="915e3-131">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="915e3-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="915e3-132">-ObjectId</span></span>
<span data-ttu-id="915e3-133">Annak az objektumnak az azonosítója, amelyhez hozzá szeretné adni a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="915e3-133">The object id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="915e3-134">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="915e3-134">-Password</span></span>
<span data-ttu-id="915e3-135">Az alkalmazáshoz társított jelszó.</span><span class="sxs-lookup"><span data-stu-id="915e3-135">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="915e3-136">-StartDate</span><span class="sxs-lookup"><span data-stu-id="915e3-136">-StartDate</span></span>
<span data-ttu-id="915e3-137">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="915e3-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="915e3-138">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="915e3-138">The default start date value is today.</span></span>
<span data-ttu-id="915e3-139">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="915e3-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="915e3-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="915e3-140">-Confirm</span></span>
<span data-ttu-id="915e3-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="915e3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="915e3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="915e3-142">-WhatIf</span></span>
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

### <span data-ttu-id="915e3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="915e3-143">CommonParameters</span></span>
<span data-ttu-id="915e3-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="915e3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="915e3-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="915e3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="915e3-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="915e3-146">INPUTS</span></span>

### <span data-ttu-id="915e3-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="915e3-147">None</span></span>
<span data-ttu-id="915e3-148">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="915e3-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="915e3-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="915e3-149">OUTPUTS</span></span>

### <span data-ttu-id="915e3-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="915e3-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="915e3-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="915e3-151">NOTES</span></span>

## <span data-ttu-id="915e3-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="915e3-152">RELATED LINKS</span></span>

[<span data-ttu-id="915e3-153">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="915e3-153">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="915e3-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="915e3-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="915e3-155">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="915e3-155">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

