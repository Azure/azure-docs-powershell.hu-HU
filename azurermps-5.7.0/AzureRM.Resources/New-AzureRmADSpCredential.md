---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: bf2a42df42a343d9745cb55f4d72463513b44dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498856"
---
# <span data-ttu-id="9bb96-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9bb96-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="9bb96-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9bb96-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb96-103">Hitelesítő adatok hozzáadása egy meglévő szolgáltatási megbízóhoz.</span><span class="sxs-lookup"><span data-stu-id="9bb96-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bb96-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9bb96-104">SYNTAX</span></span>

### <span data-ttu-id="9bb96-105">SpObjectIdWithPasswordParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9bb96-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb96-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bb96-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb96-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bb96-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb96-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bb96-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bb96-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9bb96-109">DESCRIPTION</span></span>
<span data-ttu-id="9bb96-110">Az New-AzureRmADSpCredential parancsmag használatával új hitelesítő adatokat vehet fel, illetve hitelesítő adatokat adhat meg a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="9bb96-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="9bb96-111">A szolgáltatás megbízóját az objektum-azonosító vagy a szolgáltatás egyszerű nevének ellátásával azonosítjuk.</span><span class="sxs-lookup"><span data-stu-id="9bb96-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="9bb96-112">Példák</span><span class="sxs-lookup"><span data-stu-id="9bb96-112">EXAMPLES</span></span>

### <span data-ttu-id="9bb96-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9bb96-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $SecureStringPassword
```

<span data-ttu-id="9bb96-114">Az új jelszó-hitelesítő adatok egy meglévő szolgáltatási megbízóhoz kerülnek.</span><span class="sxs-lookup"><span data-stu-id="9bb96-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="9bb96-115">Ebben a példában a megadott jelszót a objectId segítségével kell hozzáadni a szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="9bb96-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="9bb96-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="9bb96-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="9bb96-117">Új kulcshoz tartozó hitelesítő adatok kerülnek a meglévő szolgáltatási megbízóhoz.</span><span class="sxs-lookup"><span data-stu-id="9bb96-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="9bb96-118">Ebben a példában a megadott Base64 kódolt nyilvános X509-tanúsítvány ("SajátPr. cer") hozzáadódik a szolgáltató SPN-beli használatával.</span><span class="sxs-lookup"><span data-stu-id="9bb96-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="9bb96-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="9bb96-119">Example 3</span></span>

```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="9bb96-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9bb96-120">PARAMETERS</span></span>

### <span data-ttu-id="9bb96-121">-CertValue</span><span class="sxs-lookup"><span data-stu-id="9bb96-121">-CertValue</span></span>
<span data-ttu-id="9bb96-122">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="9bb96-122">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="9bb96-123">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="9bb96-123">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb96-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb96-124">-DefaultProfile</span></span>
<span data-ttu-id="9bb96-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9bb96-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bb96-126">-EndDate</span><span class="sxs-lookup"><span data-stu-id="9bb96-126">-EndDate</span></span>
<span data-ttu-id="9bb96-127">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="9bb96-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="9bb96-128">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="9bb96-128">The default end date value is one year from today.</span></span> <span data-ttu-id="9bb96-129">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="9bb96-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="9bb96-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9bb96-130">-ObjectId</span></span>
<span data-ttu-id="9bb96-131">Annak az objektumnak az azonosítója a szolgáltatónál, akinek a hitelesítő adatait hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="9bb96-131">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb96-132">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="9bb96-132">-Password</span></span>
<span data-ttu-id="9bb96-133">Az alkalmazáshoz társított jelszó.</span><span class="sxs-lookup"><span data-stu-id="9bb96-133">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb96-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9bb96-134">-ServicePrincipalName</span></span>
<span data-ttu-id="9bb96-135">Annak a szolgáltatónak a neve (SPN), amelyhez hozzá szeretné adni a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="9bb96-135">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb96-136">-StartDate</span><span class="sxs-lookup"><span data-stu-id="9bb96-136">-StartDate</span></span>
<span data-ttu-id="9bb96-137">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="9bb96-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="9bb96-138">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="9bb96-138">The default start date value is today.</span></span> <span data-ttu-id="9bb96-139">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="9bb96-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="9bb96-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9bb96-140">-Confirm</span></span>
<span data-ttu-id="9bb96-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9bb96-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bb96-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bb96-142">-WhatIf</span></span>
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

### <span data-ttu-id="9bb96-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb96-143">CommonParameters</span></span>
<span data-ttu-id="9bb96-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9bb96-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb96-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb96-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb96-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bb96-146">INPUTS</span></span>

### <span data-ttu-id="9bb96-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="9bb96-147">None</span></span>
<span data-ttu-id="9bb96-148">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9bb96-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9bb96-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bb96-149">OUTPUTS</span></span>

### <span data-ttu-id="9bb96-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="9bb96-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="9bb96-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9bb96-151">NOTES</span></span>

## <span data-ttu-id="9bb96-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bb96-152">RELATED LINKS</span></span>

[<span data-ttu-id="9bb96-153">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9bb96-153">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="9bb96-154">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9bb96-154">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="9bb96-155">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9bb96-155">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



