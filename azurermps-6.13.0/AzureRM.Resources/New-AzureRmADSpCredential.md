---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: a0fdd053c4ef3b1522fd6b03b8e58a4327fdfd44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499423"
---
# <span data-ttu-id="a94d3-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a94d3-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="a94d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a94d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a94d3-103">Hitelesítő adatok hozzáadása egy meglévő szolgáltatási megbízóhoz.</span><span class="sxs-lookup"><span data-stu-id="a94d3-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a94d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a94d3-104">SYNTAX</span></span>

### <span data-ttu-id="a94d3-105">SpObjectIdWithPasswordParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a94d3-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <Guid> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a94d3-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a94d3-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a94d3-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a94d3-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a94d3-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="a94d3-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a94d3-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a94d3-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a94d3-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="a94d3-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a94d3-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="a94d3-111">DESCRIPTION</span></span>
<span data-ttu-id="a94d3-112">Az New-AzureRmADSpCredential parancsmag használatával új hitelesítő adatokat vehet fel, illetve hitelesítő adatokat adhat meg a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="a94d3-112">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="a94d3-113">A szolgáltatás megbízóját az objektum-azonosító vagy a szolgáltatás egyszerű nevének ellátásával azonosítjuk.</span><span class="sxs-lookup"><span data-stu-id="a94d3-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="a94d3-114">Példák</span><span class="sxs-lookup"><span data-stu-id="a94d3-114">EXAMPLES</span></span>

### <span data-ttu-id="a94d3-115">Példa 1 – új szolgáltatás-fő hitelesítő adatok létrehozása a generált jelszavak használatával</span><span class="sxs-lookup"><span data-stu-id="a94d3-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="a94d3-116">Az új jelszó-hitelesítő adatok a meglévő, a "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú szolgáltatóhoz kerülnek.</span><span class="sxs-lookup"><span data-stu-id="a94d3-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="a94d3-117">2. példa – új szolgáltatás-fő hitelesítő adatok létrehozása tanúsítvány használatával</span><span class="sxs-lookup"><span data-stu-id="a94d3-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="a94d3-118">A megadott Base64-kódolt nyilvános X509 tanúsítvány ("SajátPr. cer") hozzáadódik a meglévő szolgáltatásnevet az SPN-lel.</span><span class="sxs-lookup"><span data-stu-id="a94d3-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="a94d3-119">Példa 3 – az új szolgáltatás elsődleges hitelesítő adatainak létrehozása a csővezetékek segítségével</span><span class="sxs-lookup"><span data-stu-id="a94d3-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzureRmADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="a94d3-120">Megkapja a "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú szolgáltatásnevet, valamint a New-AzureRmADSpCredential csöveket, amelyekkel létrehozhatja az új szolgáltatás-fő hitelesítő adatait a szolgáltatónál egy generált jelszóval.</span><span class="sxs-lookup"><span data-stu-id="a94d3-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzureRmADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="a94d3-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a94d3-121">PARAMETERS</span></span>

### <span data-ttu-id="a94d3-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="a94d3-122">-CertValue</span></span>
<span data-ttu-id="a94d3-123">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="a94d3-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="a94d3-124">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="a94d3-124">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94d3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a94d3-125">-DefaultProfile</span></span>
<span data-ttu-id="a94d3-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a94d3-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a94d3-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a94d3-127">-EndDate</span></span>
<span data-ttu-id="a94d3-128">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="a94d3-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="a94d3-129">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="a94d3-129">The default end date value is one year from today.</span></span> <span data-ttu-id="a94d3-130">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="a94d3-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94d3-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a94d3-131">-ObjectId</span></span>
<span data-ttu-id="a94d3-132">Annak az objektumnak az azonosítója a szolgáltatónál, akinek a hitelesítő adatait hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="a94d3-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94d3-133">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="a94d3-133">-Password</span></span>
<span data-ttu-id="a94d3-134">Az alkalmazáshoz társított jelszó.</span><span class="sxs-lookup"><span data-stu-id="a94d3-134">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94d3-135">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a94d3-135">-ServicePrincipalName</span></span>
<span data-ttu-id="a94d3-136">Annak a szolgáltatónak a neve (SPN), amelyhez hozzá szeretné adni a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="a94d3-136">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94d3-137">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="a94d3-137">-ServicePrincipalObject</span></span>
<span data-ttu-id="a94d3-138">A Service Principal objektum a hitelesítő adatok hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="a94d3-138">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a94d3-139">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a94d3-139">-StartDate</span></span>
<span data-ttu-id="a94d3-140">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="a94d3-140">The effective start date of the credential usage.</span></span>
<span data-ttu-id="a94d3-141">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="a94d3-141">The default start date value is today.</span></span> <span data-ttu-id="a94d3-142">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="a94d3-142">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94d3-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a94d3-143">-Confirm</span></span>
<span data-ttu-id="a94d3-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a94d3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a94d3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a94d3-145">-WhatIf</span></span>
<span data-ttu-id="a94d3-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a94d3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a94d3-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a94d3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a94d3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94d3-148">CommonParameters</span></span>
<span data-ttu-id="a94d3-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a94d3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94d3-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a94d3-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94d3-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a94d3-151">INPUTS</span></span>

### <span data-ttu-id="a94d3-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a94d3-152">System.Guid</span></span>

### <span data-ttu-id="a94d3-153">System. String</span><span class="sxs-lookup"><span data-stu-id="a94d3-153">System.String</span></span>

### <span data-ttu-id="a94d3-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a94d3-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="a94d3-155">Paraméterek: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a94d3-155">Parameters: ServicePrincipalObject (ByValue)</span></span>

### <span data-ttu-id="a94d3-156">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a94d3-156">System.Security.SecureString</span></span>

### <span data-ttu-id="a94d3-157">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="a94d3-157">System.DateTime</span></span>

## <span data-ttu-id="a94d3-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a94d3-158">OUTPUTS</span></span>

### <span data-ttu-id="a94d3-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="a94d3-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="a94d3-160">Microsoft. Azure. Command. Resources. modellek. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="a94d3-160">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="a94d3-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a94d3-161">NOTES</span></span>

## <span data-ttu-id="a94d3-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a94d3-162">RELATED LINKS</span></span>

[<span data-ttu-id="a94d3-163">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a94d3-163">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="a94d3-164">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a94d3-164">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="a94d3-165">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a94d3-165">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



